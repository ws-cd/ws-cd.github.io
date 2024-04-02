---
layout: en
title: Automatic Fill Slots
parent: Advanced Control
nav_order: 4
---
# Automatic Fill Slots via Web 
当 Project 发布后通过Web link部署在Web端时，可配合[Slot default value](/docs/tutorial/slot_config/#default-value) 实现读取已登录用户信息，并填充到Slot中。

基于[IT Helpdesk From](/docs/tutorial/form/)实现获取用户信息，并填充到Slot中。

### 实现效果

1、欢迎语种包含`name`

2、收集反馈信息时无需重复询问`mail`

3、结束时输出`name`和 `mail`

### 步骤
1、在变量中配置从Local storage种读取当前登录用户的`name`和`email`。
2、部署的 Web页面在Local storage种写入`name`和`email`。
3、在欢迎语及需要用到的地方引用`name`和`email`

## 实现
1、配置需要填充的系统变量: 在`Project View-Slots`中创建`name`和`email`并完成默认值配置

![img_3.png](/assets/images/addvanced_control/fill_slot/fill-slot-02.png)
![img_4.png](/assets/images/addvanced_control/fill_slot/fill-slot-03.png)

2、修改欢迎语，展示用户名称
> Hello {name}, I am your intelligent assistant. What can I do for you?
![img_5.png](/assets/images/addvanced_control/fill_slot/fill-slot-04.png)

3、输出`name`和`email`
![img_6.png](/assets/images/addvanced_control/fill_slot/fill-slot-05.png)


保存后重新发布。
注：插槽变量和系统变量读取位置是一样的，两个读同一个位置的变量不冲突

## 测试
创建会话后，欢迎语中出现了配置的`name`: PromptAI-User

![img_7.png](/assets/images/addvanced_control/fill_slot/fill-slot-06.png)


