---
layout: en
title: IT Helpdesk 
parent: Quick Start
nav_order: 2
---
# IT Helpdesk
We can expand [the Website Asssitant](/docs/quick_start/knowledge_base/) to include a few IT Helpdesk functions.  For example,
- Automatically display user's name
- Submit a ticket if it is not able to answer a user question (Fallback)
- No need to repeatedly obtain the user's `email` when creating a ticket

## Create a Flow
The flow asks for the user' email address and his question and then generates a ticket.

![img.png](/assets/images/quick_start/flow/flow-01.png)

Implementation:
- [Text tutorial](/docs/tutorial/form/)
- [Video Tutorial](/docs/example/form/)

## Automatically load user's name
用户登录系统后，可将用户的姓名和邮箱通过key-Value的方式设置到Session Storage或Local Storage中。 
PromptAI可从这两个地方获取到用户的姓名和邮箱，并在Flow中使用他们。

步骤：
1、用户登录系统后，将用户的姓名和邮箱写入Local Storage
```text
name : PromptAI-User
email: info@promptai.us
```

2、在[Slot default value](/docs/tutorial/slot_config/#default-value) 分别设置`name` 和 `email`

这里key使用,需要与第一步写入Local Storage的 key保持一致。

<table>
  <tr>
    <td><img src="/assets/images/quick_start/flow/flow-09.png" alt=""></td>
    <td><img src="/assets/images/quick_start/flow/flow-10.png" alt=""></td>
  </tr>
</table>


Use [Slot default value](/docs/tutorial/slot_config/#default-value) to load user information.
Slot values:
- name : PromptAI-User
- email: info@promptai.us

![fill-slot-06.png](/assets/images/quick_start/flow/flow-02.png)

Implementation
- [Text tutorial](/docs/advance_control/fill_slots/)

## Fallback
When a user inputs a question that cannot get answered confidently, the user can choose to submit a ticket.

### Fallback connects to Service Flow
1. Click `Overview-Fallback-Buttons for fallbacks-Add` to add Service Flow button to fallback.

![img.png](/assets/images/quick_start/flow/flow-03.png)

2. Modify Service Flow and go directly to submit tickets From
![img_1.png](/assets/images/quick_start/flow/flow-04.png)

3. Modify the Bot node to display `name` and `email`
![img.png](/assets/images/quick_start/flow/flow-05.png)

## Run
Realization effect:
- 1. Automatically obtain the `name` and `email` of the logged in user
- 2. The logged-in user displays `name` in the welcome message: PromptAI-User
- 3. Click the `Service` button below Fallback to submit a ticket directly
- 4. Submitting a ticket does not ask for `email` repeatedly. After submission, the automatically filled `info@promptai.us` is displayed.

<table>
  <tr>
    <td><img src="/assets/images/quick_start/flow/flow-06.png" alt=""></td>
    <td><img src="/assets/images/quick_start/flow/flow-07.png" alt=""></td>
  </tr>
  <tr>
     <td><img src="/assets/images/quick_start/flow/flow-08.png" alt=""></td>
  </tr>
</table>
