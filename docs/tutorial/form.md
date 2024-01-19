---
layout: en
title: Form
parent: Developer's Guide
nav_order: 7
---
In PromptDialog, Form is a component that collects a set of information from the user. The information will be stored in slots. In the following example, the bot collects the information of fruit type and quantity from the user, and confirm with the user after completion. This information collection conversation can be implemented by form with two required slots: fruit_type and fruit_quantity. 

```text
Bot : Hello!
      What can i do for you?
User: Hi there! I'd like to order some fruits

# Collect the type and quantity of fruit ordered by the user through the Form
Bot : Perfect! What kinds of fruits would you like to order?
User: I'd like some apples, please
Bot : Great! And how much apples would you like to order?
User: Let's go with 5 apples

Bot : Perfect! I have your order 5 apples.
User: Thanks
Bot : You are welcome! I'll prepare your order with 5 apples, fell free to ask!
```
There are other similar scenarios that can be handled by Form:
- Check the weather: Collect the location and time to check the weather conditions in real time.
- Book air tickets: Book air tickets by obtaining the user's travel time and departure airport.
- ...


## How to use Form?
Next, we will introduce how to create the example of user-ordered fruit mentioned above.

### Create `Fruit`Dialog flow
![img.png](/assets/images/form_fruit_create_flow.jpg)

Next, we create a `Bot` node to say hello and a `User` node to show the intent to buy fruit
![img_1.png](img_1.png)

## Create fruit form
Click the `User` node and select `Form` in the pop-up menu
![img.png](img.png)
The name of the Form can be set according to the function, here we fill in `Fruit order`
![img_3.png](img_3.png)

Three pieces of information need to be completed after creating `fruit order`
![img_4.png](img_4.png)

|  Name        | Required | Desc                                                   |
|--------------|----------|--------------------------------------------------------|
| Slots        |    Yes   | slots that need to be collected                        |
| Functions   |    No    | Possible problems filling the form or exiting the form |
| Abort      |    No    | Possible problems filling the form or exiting the form |
| Complete      |    Yes   | After the form runs successfully                       |
  
## Slots
We need to collect `fruit_type` and `fruit_quantity` from users through Slots, and then explain in detail how to add `fruit_type`

Click on the `Slots` node and select `Add Slot` from the pop-up menu
![img_5.png](img_5.png)

In the pop-up Slot window, we need to pay attention to the input `Slot Name` and `Slot Question`, here fill in the name of the Slot `fruit_type` (enter the name and press Enter to create) and fill a sentence to prompt the user to enter the information in the question.

![img_6.png](img_6.png)

So far, the `fruit_type` slot has been created.
![img_7.png](img_7.png)

Add `fruit_quantity` slot like this:
![img_9.png](img_9.png)

## Abort
During the ordering process, the user may exit the conversation
- Actually, I've changed my mind. I won't buy any fruits today. (Exit From, stop order)

## Complete
The `Complete` node handles the completion of the collection form, here we confirm the order to the user
![img_10.png](img_10.png)

## The complete flow diagram is as follows:
![img_11.png](img_11.png)
![img_12.png](img_12.png)
![img_13.png](img_13.png)

---

# FAQ

## Can I fill multiple slots in one sentence?
Yes, we support fill multiple slots in one sentence.
Example: 
```text
Bot : Hello!
      What can i do for you?
User: Hi there! I'd like to order some fruits

Bot : Perfect! What kinds of fruits would you like to order?
# quantity and fruit type in one sentence
User: Let's go with 5 apples

Bot : Perfect! I have your order 5 apples.
User: Thanks
Bot : You are welcome! I'll prepare your order with 5 apples, fell free to ask!
```