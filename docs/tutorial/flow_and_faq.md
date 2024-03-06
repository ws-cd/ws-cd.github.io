---
layout: en
title: Dialog Flow + FAQ
parent: Developer's Guide
nav_order: 5
---
A typical application often has a dialog flow and FAQ mixed together: When a user is filling a form, she might ask a few questions.  By default, PromptDialog can interleave these two processes together.  During the stage of debugging and releasing, the designer can select both modules and compile them together.  
![flow_and_faq0.png](/assets/images/flow_and_faq0.png)

We combine a dialog flow with FAQ and train them together:
![flow_and_faq1.png](/assets/images/flow_and_faq1.png)

When the bot runs,  it follows the dialog flow.  Meanwhile, it can answer questions in FAQ.
![flow_and_faq2.png](/assets/images/flow_and_faq2.png)
