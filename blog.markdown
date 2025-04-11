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

<!-- 
TODO: update the blog. AI is more limited than the prophecies, making it more analogous to industrial era factories than magical human replacements. The word "luddite" has started to be more fitting as we discover more and more limitations. 

But "Mid" does not mean useless. AI is still very useful, you just need someone who knows how to use it 1) with accuracy/safety, 2) all the capabilities, and 3) what it CANNOT be used for. 

Fine-Tuning, Pruning, Batch Processing, and Output Formatting are not things that business leaders know necessarily. Having an evangelist unlocks more use cases. 
Fine-tuning: specific details. Highly specialized output, reasons to use different GPTs for different problems. 
Pruning: Lobotomize your own GPT to make it faster and cheaper for problems that do not require generalist AIs. Potentially even real-time. Beware of over-fitting!
Batch Processing: about half the price for problems that do not require real-time processing. 
Output Formatting: can request output in specific JSON formats, making it possible to get multiple very specific responses (numbers, sentences, dates) in a single prompt.

https://www.sltrib.com/opinion/commentary/2025/04/03/opinion-tech-fantasy-that-powers/



Wait, is it possible to prune OpenAI models? Or do we need to use something like LLMStudio? 
Ah right, it is called "Distillation" in OpenAI.  -->




# On Luddites
The Luddite movement of the 19th century was based on the fear that machinery would replace humans. While this was true in the short run, in the long run machinery simply became another means by which humans became more productive. One great fear around the advent of LLMs is that this time it was different and that there would be no more need for humans. The most ardent prophets and doomsayers proclaimed that wide swaths of humanity would not merely be unemployed, but unemployable. As we discover more and more about the limitations of LLMs, these prophecies have been shown to be premature. 

This is not necessarily to say that AI has failed. To be entirely fair, functionally every technology going back to the [industrial revolution](https://www.lhistoire.fr/english-version/the-steam-engine-beyond-the-myth#:~:text=Technicians%20and%20engineers,of%20the%20buildings) has failed to live up to its respective promise. LLMs have, like every tool humanity has ever created, [a proper use](https://liblab.com/blog/automating-common-tasks-with-llms#:~:text=Tasks%20that%20are%20highly%20repetitive,best%20left%20to%20human%20experts). 
* Repetition: The task must be performed many times.
* Description: The task's description does not change between iterations, only the data on which the task operates. 
* Simple: Has a definite answer which requires limited reasoning or judgment to reach.

Problems that fit into this problem space can be __extremely__ efficient when properly automated. Unfortunately, they can also be extremely *in*efficient when improperly implemented, or even outright dangerous with improper isolation and auditing. 