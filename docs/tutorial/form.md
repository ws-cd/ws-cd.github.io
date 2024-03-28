---
layout: en
title: Form
parent: Developer's Guide
nav_order: 7
---
In PromptDialog, Form is a component that collects a set of information from the user. The information will be stored in slots. In the following example, the bot collects the information of email and problem from the user, and confirm with the user after completion. This information collection conversation can be implemented by form with two required slots: `email` and `problem`. 

```text
Bot : Hello! Welcome to help center.
      What can i do for you?
User: Hi there! I'm having an issue with my account.

# Collect the email and problem through the Form
Bot : What is the problem description for the issue?
User: I can't check my balance
Bot : What is your email address to lookup for creating the incident?
User: This is my email address example@example.com

Bot : Successfully opened up incident INC0010005 for you. Someone will reach out soon.
Bot : The ticket link: https://example.com/ticket/INC0010005
```
There are other similar scenarios that can be handled by Form:
- Check the weather: Collect the location and time to check the weather conditions in real time.
- Book air tickets: Book air tickets by obtaining the user's travel time and departure airport.
- ...


## How to use Form?
Next, we will introduce how to create the example of IT helpdesk mentioned above.

### Create Incident Dialog flow
![form-01.png](/assets/images/tutorial/form/form-01.png)

Next, we create a `User` node to start collect information
![form-02.png](/assets/images/tutorial/form/form-02.png)

## Create Incident Form
Click the `User` node and select `Form` in the pop-up menu and click `Add GPT Form Node`.There are two input fields:
- Name       : The name of the Form can be set according to the function, here we fill in `Incident`.
- Description: The Prompt used by GPT tells GPT what the form need to do.

![form-03.png](/assets/images/tutorial/form/form-03.png)

Four pieces of information need to be completed after creating `Incident`
![form-04.png](/assets/images/tutorial/form/form-04.png)

|  Name        | Required | Desc                                                   |
|--------------|----------|--------------------------------------------------------|
| Slots        |    Yes   | Slots that need to be collected                        |
| Functions   |    No    | - |
| Abort      |    No    | After the from is interrupted  |
| Complete      |    Yes   | After the form runs successfully                       |
  
## Slots
We need to collect `email` and `problem` from users through Slots, and then explain in detail how to add `email`

Click on the `Slots` node and select `Add Slot` from the pop-up menu
![form-05.png](/assets/images/tutorial/form/form-05.png)

In the pop-up Slot window, we need to pay attention to the input `Slot Name`、`Slot Question` and `Description`
- Slot Name     : Fill in the name of the Slot `email` (enter the name and press Enter to create)
- Slot Question : A sentence to prompt the user to enter the information in the question.
- Description   : The Prompt used by GPT tells GPT how to extract Slot from user input.

More details [Slots Config](/docs/tutorial/slot_config/)

![form-06.png](/assets/images/tutorial/form/form-06.png)

So far, the `email` slot has been created.
![form-07.png](/assets/images/tutorial/form/form-07.png)

Add `problem` slot like this:
![form-08.png](/assets/images/tutorial/form/form-08.png)

## Functions
The function provides methods to validate and change slots during the form collection process. If you need to check the quantity, 
logic or validity of slots while filling out a form, such as limiting the number of people to no more than 6 people during a restaurant reservation form, 
or wanting the fruit names entered by users to be converted into scientific names during a fruit purchase process... 
If you wish to modify a slot, you can use the function feature. Define a function and describe its purpose in the description. 
Then, specify the involved slot names in the param section. GPT will automatically check and call these functions during the form execution process.

## Abort
During the ordering process, the user may exit the conversation
- Actually, I've changed my mind. I won't buy any fruits today. (Exit From, stop collect information)

## Complete
The `Complete` node handles the completion of the collection form
![form-09.png](/assets/images/tutorial/form/form-09.png)

## The complete flow diagram is as follows:
![form-10.png](/assets/images/tutorial/form/form-10.png)
![form-11.png](/assets/images/tutorial/form/form-11.png)

## Test Run
![form-12.png](/assets/images/tutorial/form/form-12.png)
---

# FAQ

## Can I fill multiple slots in one sentence?
Yes, we support fill multiple slots in one sentence.
Example: 
```text
Bot : Hello!
      What can i do for you?
User: Hi there! I'm having an issue with my account.

Bot :  What is the problem description for the issue?
# problem and email in one reply
User: I cannot check my balance, if I can check my balance again, please send an email to example@example.com

Bot : Successfully opened up incident INC0010005 for you. Someone will reach out soon.
Bot : The ticket link: https://example.com/ticket/INC0010005
```
