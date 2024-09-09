# Write the Back Cover Copy for an EPUB

This is a prompter project that will write the back cover copy for an EPUB you provide. It assumes that there is a file called `preface*` and `toc*` in the EPUB that it can use to generate notes.

## Examples

- [AI Enabled SDLC](examples/bcc-ai-enabled-sdlc.md)

- Cloud Native Java, 2e -- https://github.com/odewahn/ai-bcc-samples/blob/main/examples/bcc-cn-java-2e.md

- Hands on LLMs -- https://github.com/odewahn/ai-bcc-samples/blob/main/examples/bcc-hands-on-llm.md

## How it works

First, it uses the Preface and Table of Contents from the EPUB to "take notes" about the key points:

https://github.com/odewahn/ai-bcc-samples/blob/main/prompts/take-notes-preface.md

https://github.com/odewahn/ai-bcc-samples/blob/main/prompts/take-notes-toc.md

Here's a sample of the notes it took on Cloud Native Java:

https://github.com/odewahn/ai-bcc-samples/blob/main/examples/notes-cn-java-2e.md

Then it uses these notes to write the BCC:

https://github.com/odewahn/ai-bcc-samples/blob/main/prompts/write-back-cover-copy.md

These are all used in the `go.prompter` script to generate the final BCC.

```bash
init
load --fn=source/cn-java-2e.epub
transform --transformation=html2md
# Take notes on the preface
prompt --task=prompts/take-notes-preface.md --globals=metadata.yaml --where="block_tag like 'preface%'"
# Take notes on the table of contents
prompt --task=prompts/take-notes-toc.md --globals=metadata.yaml --where="block_tag like 'toc%'"
# Write the prompt notes out to a file
squash --fn=source/notes.md
# Load the notes back in.  This is something of an ugly hack
load --fn=source/notes.md
# Now ask for the full analysis
prompt --task=prompts/write-back-cover-copy.md --persona=prompts/persona-marketing.md --globals=metadata.yaml --prompt_tag=bcc
# Write it out
squash --where="prompt_tag='bcc'" --fn=source/bcc.md
# load it back in
load --fn=source/bcc.md
prompt --task=prompts/convert-to-narrative.md --persona=prompts/persona-reader.md --prompt_tag=narrative
transfer-prompts --where="prompt_tag='narrative'"
```
