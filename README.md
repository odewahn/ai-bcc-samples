# Write the Back Cover Copy for an EPUB

This is a prompter project that will write the back cover copy for an EPUB you provide. It assumes that there is a file called `preface*` and `toc*` in the EPUB that it can use to generate notes.

First, it uses the Preface and Table of Contents from the EPUB to "take notes" about the key points:

https://github.com/odewahn/ai-bcc-samples/blob/main/prompts/take-notes-preface.md

https://github.com/odewahn/ai-bcc-samples/blob/main/prompts/take-notes-toc.md

Here's a sample of the notes it took on Cloud Native Java:

https://github.com/odewahn/ai-bcc-samples/blob/main/examples/notes-cn-java-2e.md

Then it uses these notes to write the BCC:

https://github.com/odewahn/ai-bcc-samples/blob/main/prompts/write-back-cover-copy.md

# Examples

- AI Enabled SDLC -- https://github.com/odewahn/ai-bcc-samples/blob/main/examples/bcc-ai-enabled-sdlc.md

- Cloud Native Java, 2e -- https://github.com/odewahn/ai-bcc-samples/blob/main/examples/bcc-cn-java-2e.md

- Hands on LLMs -- https://github.com/odewahn/ai-bcc-samples/blob/main/examples/bcc-hands-on-llm.md
