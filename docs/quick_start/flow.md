---
layout: en
title: IT Helpdesk 
parent: Quick Start
nav_order: 2
---
# IT Helpdesk

基于[Web Knowledge Base](/docs/quick_start/knowledge_base/) 拓展实现IT Helpdesk功能。

*IT Helpdesk: 收集用户的email和问题并自动生成工单，当出现Fallback时，用户可一键提交工单*

功能清单：
- 可主动获取到登录用户的`name`和`email`
- 用户登录后，打开Chatbot框可展示`name`
- Fallback文本可关联Service Flow创建工单
- 创建工单时无需重复获取用户的`email`

## 创建Service Flow
Service flow 可收集用户问题，并自动生成工单。
![img.png](/assets/images/quick_start/flow-01.png)

具体实现：
- [文本教程](/docs/tutorial/form/)
- [视频教程](/docs/example/form/)

## 自动加载用户名
使用[Slot default value](/docs/tutorial/slot_config/#default-value) 读取已登录用户信息填充到Slot中。

![fill-slot-06.png](/assets/images/quick_start/flow-02.png)

当用户打开对话框时可展示当前用户的用户名。

具体实现
- [文本教程](/docs/advance_control/fill_slots/)

填充结果：
- name : PromptAI-User
- email: info@promptai.us

## Fallback
当用户输入问题无法匹配到任何问题时，用户可选择提交工单。

### Fallback连接到Service Flow
1、依次点击`Overview-Fallback-Buttons for fallbacks-Add`为 fallback 添加Service Flow按钮

![img.png](/assets/images/quick_start/flow-03.png)

2、修改Service Flow直接进入提交工单From
![img_1.png](/assets/images/quick_start/flow-04.png)

3、修改Bot节点，展示`name`和`email`
![img.png](/assets/images/quick_start/flow-05.png)

## 对话
实现效果：
- 1、主动获取到登录用户的`name`和`email`
- 2、登录用户在欢迎语中展示`name`：PromptAI-User
- 3、点击Fallback下方的`Service`按钮可直接提交工单
- 4、提交工单是未重复询问`email`, 提交后展示自动填充的`info@promptai.us`

<table>
  <tr>
    <td><img src="/assets/images/quick_start/flow-06.png" alt=""></td>
    <td><img src="/assets/images/quick_start/flow-07.png" alt=""></td>
  </tr>
  <tr>
     <td><img src="/assets/images/quick_start/flow-08.png" alt=""></td>
  </tr>
</table>