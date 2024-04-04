---
layout: en
title: IT Helpdesk 
parent: Quick Start
nav_order: 2
---
# IT Helpdesk

基于[Web Knowledge Base](/docs/quick_start/knowledge_base/) 拓展实现IT Helpdesk功能。

*IT Helpdesk: 收集用户的email和问题并自动生成工单*

功能清单：
- 可主动获取到登录用户的`name`和`email`
- 用户登录后，打开Chatbot框可展示`name`
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

## Fallback
当用户输入问题无法匹配到任何问题时，用户可选择提交工单。

### Fallback连接到Service Flow
1、依次点击`Overview-Fallback-Buttons for fallbacks-Add`为 fallback 添加Service Flow按钮

![img.png](/assets/images/quick_start/flow-03.png)

2、修改Service Flow直接进入提交工单From
![img_1.png](/assets/images/quick_start/flow-04.png)
