---
layout: en
title: Project Overview
parent: Developer's Guide
nav_order: 2
---
Click `Overview`, the designer can review the modules in the project.  Clicking these modules will bring the designer to the corresponding module such as FAQ and Flows. 
## Project

Click the current project `Hello world` in the overview window, and then click the pop-up `Edit Node` to edit the project settings.

![project_create0.png](/assets/images/project_create0.png)

In the project settings, you could choose what to display below the first welcome message. You can display faq or a subset of flows as buttons so that the user can click one of the buttons to enter.  Certainly, a user can speak about her need; the bot will enter the corresponding flow based on her utterance. 

## FAQ
Click `FAQ` in the overview diagram, and then click the pop-up `Edit Node` to visit the FAQ page.
![project_overview1.png](/assets/images/project_overview1.png)

## Flows
Click a `Flow`. Then click the pop-up `Edit Node` to visit the dialog flow diagram you selected.
![project_overview2.png](/assets/images/project_overview2.png)

### First Message
The `First Message` option allows you to configure the first message of each flow. It means that when we reach this flow during our conversation, the system sends the first message to the user.

## Fallback
Click `Fallback` of the project overview.  Then click the pop-up `Edit Node`, where you can edit the fallback actions that the bot will take if it does not understand the user utterance.  If none of the action returns a response, the default text message will be sent to the user. 
![project_overview3.png](/assets/images/project_overview3.png)

### Buttons for fallback
When triggering a fallback, you can choose to display buttons for flows or FAQs to guide the user for the next step in the conversation.