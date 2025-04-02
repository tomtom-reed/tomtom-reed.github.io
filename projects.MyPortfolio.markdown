---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default
permalink: /thiswebsite/

---
# [This Website](https://github.com/tomtom-reed/tomtom-reed.github.io)
Jekyll static site generator with Github Pages. The backend uses Ruby automation to build markdown configuration into static frontend code, then Github has been configured to serve the page as executable HTML instead of viewable code - resulting in the website you are now visiting. 

The frontend folder `/docs` is generated before upload, meaning there is no post-push build process. In enterprise environments this would be integrated with Jenkins or Github Actions to facilitate collaboration and better version control, but for a single-user codebase that process is unnecessary. Sacrifices are occasionally necessary for agility, but only so long as the sacrifice won't have much greater long-term costs. That lesson was dearly learned. 

# Development Process
Visual Studio Code running in WSL Ubuntu. 

Ruby Gems and Markdown are the primary code aspects. There are also some OpenAI-augmented text blocks on here; see if you can spot them. I didn't hide them very well. 