---
layout: en
title: Slots Config
parent: Developer's Guide
nav_order: 18
---
Slots support configuring with Slot Type、Enum and Default value.

![slot-config-01.png](/assets/images/tutorial/slot_config/slot-config-01.png)

| Settings | Explain | Scope | Remark |
|------|:-----|:---------|------|
|  Slot Type   | Type of data, optional values: string, number, boolean and array     |    Form slots      |      |
|  Enum    | Optional value when filling Slot  |    Form slots        |   For example pizza size, 6, 7 or 8 inches   |
|  Default Value    | Automatically fill slots when start a chat   |          | For example, username, you can use this slot directly during the conversation without asking the user.      |

## Slot Type
After specifying the type for Slot, variables can be better extracted
- String: String, such as email address, various names, user opinions and other text-type data.
- Number: Numbers, such as quantity, weight, currency, age and other numeric data
- Boolean: Boolean value, such as yes or no, this type of data can be selected in scenarios with only two choices.
- Array: Array, a scene with multiple similar selections.

## Enum
Slot optional values

Steps:
1. Enable Enum
2. Click the green Add button to add

![slot-config-02.png](/assets/images/tutorial/slot_config/slot-config-02.png)

## Default value
Automatically fill slots when start a chat

- Set Value: Set a fixed value, no need to read it from the website.
- Local Story: Read the specified key from Local Storage
- Session Story: Read the specified key from Session Storage
- Custom Script: Run a custom JavaScript code and fill the return value into the slot

![slot-config-03.png](/assets/images/tutorial/slot_config/slot-config-03.png)
