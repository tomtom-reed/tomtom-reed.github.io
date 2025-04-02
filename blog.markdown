---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default
permalink: /blog/

---
# Why You Need an AI Evangelist
Imagine for a moment that you are an investment fund manager. A large part of your role is to read all documents relevant to your fund's portfolio both for your own knowledge and to summarize them for the benefit of your investors. The second half of that is perfectly suited for AI automation:
* Repetition: The task must be performed many times.
* Process: Each time the task is performed it can be described in the same way.
* Simple: Requires few calculations and little extrapolation. 
* Output Format: The desired output fits into the same format every time.

It is common to simply implement AI as quickly as possible. After all, if it works then extra time is just extra money being wasted. I disagree with this approach. If output is prioritized over proper training, then consider the costs in human time that would need to be spent reading and correcting the naive output before presenting it to clients. This is especially true in scenarios such as data summaries, as the entire purpose of a summary is what data is being prioritized in the extraction. Proper training of a model, despite the upfront costs, will save enormous amounts of human time and client goodwill in the relatively short long-run. 

AI is not magic. It is a tool that has certain capabilities, many of which are still poorly understood. If the product team lacks understanding of what AI is capable of then the products they design will be inefficient at best and counterproductive at worst. The difference between Fine-Tuning and RAG or the importance of Evaluations are indeed important technical concerns, but it is the rare product owner who understands why Pruning is so valuable. After all, what would the purpose be of making a model _less_ powerful? To even ask that question in the first place requires surmounting an unknown unknown. This is not even to mention the importance of proper logging and auditing; if your prompts and models lack proper version control or an audit trail then you could accidentally cripple your own implementation and never know why. 

This is why the role of an AI Evangelist is important on every team. Every team needs someone who 1) knows when something is a good candidate for AI automation, 2) knows the tools that should be used to best fulfill that need, 3) can communicate to the business team the opportunities and requirements of new products, and 4) knows how to avoid tech and product debt which could become crippling in the long run. 

In my experience, few teams recognize this need. 

[Back](/)