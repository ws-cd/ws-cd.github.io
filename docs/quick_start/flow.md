---
layout: en
title: IT Helpdesk 
parent: Quick Start
nav_order: 2
---
# IT Helpdesk

Based on [Web Knowledge Base](/docs/quick_start/knowledge_base/), expand and implement IT Helpdesk functions.

*IT Helpdesk: Collects users’ emails and questions and automatically generates tickets. When a Fallback occurs, users can easily submit a ticket*

Feature list:
- Can automatically obtain the `name` and `email` of the user logged in 
- After the user logs in, open the Chatbot box to display `name`
- Fallback text can be associated with Service Flow to create tickets
- No need to repeatedly obtain the user's `email` when creating a ticket

## Create Service Flow

Service flow collects user questions and automatically generates tickets.

![img.png](/assets/images/quick_start/flow/flow-01.png)

Implementation:
- [Text tutorial](/docs/tutorial/form/)
- [Video Tutorial](/docs/example/form/)

## Automatically load username
Use [Slot default value](/docs/tutorial/slot_config/#default-value) to read the logged in user information and fill it into the Slot.

![fill-slot-06.png](/assets/images/quick_start/flow/flow-02.png)

Displays the current user's username when the user opens the dialog box.

Implementation
- [Text tutorial](/docs/advance_control/fill_slots/)

Slot values:
- name : PromptAI-User
- email: info@promptai.us

## Fallback

When the user inputs a question that cannot match any question, the user can choose to submit a ticket.

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