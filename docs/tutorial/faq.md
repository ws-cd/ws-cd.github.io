---
layout: en
title: FAQ
parent: Developer's Guide
nav_order: 3
---
Each project has a default FAQ (frequently answered questions) module.  The beta version only allows one FAQ for each project. 

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

## Training options
When you train your model, we provide two training options:
- ChatGPT/GPT4: It employes ChatGPT/GPT4 to do querestion comparison and retrieve answer.  This is an approach we recommend as the designer need not provide many similar questions.
- Customized BERT model: It can be trained and deployed locally to best protect privacy and has performance between RASA FAQ and ChatGPT. For this option, please contact us [info@promptai.us](mailto:info@promptai.us).
