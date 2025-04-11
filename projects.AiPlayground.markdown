---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default
permalink: /aiplayground/

---
# [AiPlayground](https://github.com/tomtom-reed/AiPlayground)
A skeleton implementation of the OpenAI Assistants API in C# designed to be easily modifiable to enterprise needs.

To explain the rationale behind this project, this library is NOT necessary for creating assistants in the first place, as the UI is almost inarguably easier to use. The issue with [platform.openai.com](https://platform.openai.com/docs/overview) is that it opens the possibility of changing things in production without a proper audit trail and notification system, which should terrify you.

What this library does is enable in-channel auditing, logging, and persistance. **None of that is included in this codebase** but it is a skeleton to build on top of. There is no license on this code so feel free to copy-paste it at your own peril. I have included documentation where appropriate: more to follow.

The necessary components of responsibly using AI in production (in my opinion) is to:

### Save details of created assistants
You MUST know at minimum when and by whom the assistant was created and modified. Ideally the system should have an email watchlist which should be notified when any assistant is modified. As of time of writing, platform.openai.com does NOT have either of those IMO mandatory features, so they can only be added by implementing the Assistants API in code as this project does.

### Save details of completions
Persistant output (output that would be used multiple times) may become outdated due to changes in business requirements *even if the data used in the prompt did not change*. One example could be new legal regulations that require the output to use certain language or disclaimers. This means that your persistant storage of these completions should store metadata about its creation that can be used to filter the completions for later deprecation or regeneration. Minimally this should include assistant name and assistant version (or last modified date) alongside whatever identifies the prompt used. 

### Save details of prompts
For reasons previously mentioned, prompts should also be versioned. The details of how to do this are left to your particular implementation, as prompts can be complicated. If you look at the code you may notice that it is possible to provide very complex data to the initialMessage, including multi-channel files, and that threads can be used multiple times to create a conversation with context about previous messages. A reader who has gotten this far should probably be able to know what and why is needed to create a proper audit trail for their implementation. 

# Development Process
Visual Studio Code running in WSL Ubuntu. 

At time of writing, the code is functional but incomplete. Use the unit tests as an entry point. You will need an API key from platform.openai.com placed in the **OPENAI_API_KEY** env variable. 