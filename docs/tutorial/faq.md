---
layout: en
title: FAQ
parent: Developer's Guide
nav_order: 3
---
Each project has a default FAQ (frequently answered questions) module.  

<!-- The beta version only allows one FAQ for each project. -->

## FAQ window  

Click `FAQ` in the left navigation pane.  In the FAQ window, you can add, modify, and delete questions.

![faq-01.png](/assets/images/tutorial/faq/faq-01.png)

## Add a new question

Click the `+Add` button on the upper right corner to pop up the question addition interface.

![faq-02.png](/assets/images/tutorial/faq/faq-02.png)

## Fill in question/answer information
Please fill multiple examples for the same question, which is required for RASA Training. Please make sure: 

- Each question can only be listed once,
- Each question shall have multiple examples: They are the same question, but asked differently. 

![faq-03.png](/assets/images/tutorial/faq/faq-03.png)

## Created successfully

![faq-04.png](/assets/images/tutorial/faq/faq-04.png)

## Tips

1. Can the answers to questions related to the knowledge base be optimized?
> Knowledge base Q&A is based on LLM’s generation and summary capabilities, and the content of the answer is somewhat unpredictable and singular (text type reply).
>
> You can create related questions as a FAQ, and fill in the answers to the FAQ with text, pictures, attachments and other types of answers.

step:

- Find user input in statistics

![img.png](/assets/images/quick_start/kb/kb-14.png)

- Create FAQ

Here the PromptAI logo is added based on the web reply.

![img_1.png](/assets/images/quick_start/kb/kb-15.png)

- Release and run

Enter a similar question and the question will be answered by FAQ.

![img_2.png](/assets/images/quick_start/kb/kb-16.png)
