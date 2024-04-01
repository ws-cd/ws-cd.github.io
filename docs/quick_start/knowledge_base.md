---
layout: en
title: Quick Start: Web Knowledge Base
nav_order: 1
show: false
---
# 基于Web与FAQ快速构建企业知识库
欢迎使用PromptAI！此快速入门指南将指导您如何通过URL和FAQ构建企业知识库。

本文使用PromptAI[帮助文档](https://doc.promptai.us/docs/about/) 作为Web来源，同时添加一些常用的FAQ。
构建完成后可通过 PromptAI 提供的ChatBot直接进行对话。 当前过程非常容易，操作过程仅需少许输入与点击操作

## 准备工作
1、注册与登录

如果您暂时没用PromptAI账号，请[点击注册](https://app.promptai.us/register) 通过邮件注册。如您已有账号， [点击登录](https://app.promptai.us/login) 进行登录。

  
## 构建与管理知识库
1、创建项目
登录系统后，在右上角点击进行"Create Project"进行项目创建。

这里我们输入必要的信息：
- 名称: PromptAI Helper
- 描述：PromptAI documents chatbot
- 欢迎语：Welcome to using PromptAI ! I can answer your related questions.

![img.png](img.png)

2、添加URL Web知识库
进入项目后，依次点击："Knowledge Base" - "Web" 进入 Web 知识库管理界面

![img_1.png](img_1.png)

点击"Add"可进入Web添加界面,在URL中输入PromptAI帮助文档的首页：https://doc.promptai.us/docs/about/
![img_2.png](img_2.png)

PromptAI帮助文档由多个页面构成，所以我们需要解析其他帮助页面。点击"Parse"按钮可进行解析，在下方可看到解析后的页面地址。

过滤：
- 使用"Filer"通过关键字对链接筛选
- URL 左侧的选择框


这里我们默认使用全选，点击右下角"OK"即可。
![img_3.png](img_3.png)

接下来系统将自动解析页面，进行知识库初始化。
![img_4.png](img_4.png)


初始化完成后，所有的 URL 状态变为"complete"
![img_6.png](img_6.png)

3、添加FAQ知识库
点击左侧："FAQ" 进入FAQ管理界面
![img_5.png](img_5.png)

这里我们添加第一个FAQ来回答 "Who are you?" 这个问题.

- User Question: 用户可能会询问的问题
- Bot  Response: 期望的会放大

点击右上角保存即可。
![img_7.png](img_7.png)

*更多 FAQ示例请访问[FAQ](/docs/tutorial/faq/)*

## 发布与对话
经过简单的两个步骤，我们完成了知识库的构建：
- 添加并解析PromptAI 文档：https://doc.promptai.us/docs/about/
- 添加FAQ：Who are you?

### 发布
接下来进行最后的发布流程：依次点击："Project Tool" - "Release" 进入发布管理界面
![img_9.png](img_9.png)

接下来点击"Faq"将 Faq 选中，最后点击"Click to release"上方的图标进行发布。

![img_11.png](img_11.png)

数秒后发布成功并弹出对话框：
![img_12.png](img_12.png)

### 对话

接下来我们试试对话效果
- 询问: who are yor?
- 询问： What PromptAI can do?

![img_13.png](img_13.png)

For now, 我们的 PromptAI Helper 构建已完成。仅需少数几步输入与点击即可完成知识库的构建。
## 报表

PromptAI对用户提供了报表功能，用户可以查看项目的使用情况，包括访问量、问答量、TopN等。
![img_14.png](img_14.png)


## 使用建议
不仅支持URL，PromptAI还支持Text和File其他两种类型的知识库。三种不同类型的知识库可结合起来一起工作，提供更好的服务使用体验。

## 常见问题解答

1、知识库相关问题回答可否优化？
> 知识库问答基于LLM的生成总结能力，回答的内容有一定不可预测性及单一性（text类型回复）。
> 
> 可将相关的问题创建为一个FAQ，在FAQ的回答中填入文本、图片及附件等类型的回答。
