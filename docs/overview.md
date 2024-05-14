---
layout: en
title: Overview
nav_order: 1
has_children: false
---
PromptAI provides an all-in-one devops platform of building, running and deploying a chatbot.  It supports both on premises and cloud design and deployment.

* [Design bots on cloud, run on cloud](https://www.promptai.us/en/pricing/on-cloud/)
* [Design bots locally, run locally](https://www.promptai.us/en/pricing/premises/)

PromptAI emphasizes the protection of user data. Your data is stored in secure cloud AWS/US servers and is subject to strict encryption and access controls. You can also run PromptAI locally, keeping the design and conversations on your own machine 

<!-- PromptAI提供专业的对话机器人设计体验，旨在简化构建过程，使其简单高效。我们提供直观的流图设计工具，让您轻松创建对话机器人。PromptAI包含丰富的预制功能，包括文档、网页链接、文件转换成对话内容等。我们支持简单的问答交互，简单信息的收集，以及复杂多信息的收集。您可以控制丰富的富文本回复内容，并支持Webhook调用、对话历史记录、以及发布为Web内嵌对话机器人和移动端对话机器人。此外，我们还提供预制变量设置，以帮助您快速高效地设计和部署您的对话机器人。 -->

PromptAI provides an intuitive conversation design tool for fast bot creation. It enable webhook calls, conversation history, as well as publishing as a web-embedded chatbot and a mobile chatbot. You have full control over response content.
<!-- ## 快速开始  -->
## Get Start
<!-- 以下是在云版本中创建第一个对话机器人的例子。（更多例子在[这里](/docs/examples/)可以查看） -->
Here is an example of creating the first PromptAI chatbot. 
<!-- Here is an example of creating the first chatbot in the cloud version. (Local version examples or more examples can be found [here](/docs/example/)) -->

<!-- 1. 创建第一个项目 -->
1. Create the first project.
![overview0.png](/assets/images/overview/get-start-01.png)
<!-- 2. 点击完善第一个Bot节点 -->
2. Create the first dialog flow.
![overview1.png](/assets/images/overview/get-start-02.png)
<!-- 3. 点击完善第一个Bot节点  -->
3. Click to complete the flow.
![overview2.png](/assets/images/overview/get-start-03.png)
<!-- 4. 创建一个User节点。 -->
4. Add a user (intent) node where a user may encounter an IT issue.
![overview3.png](/assets/images/overview/get-start-04.png)
<!-- 5. 创建一个Bot节点。 -->
5. Add a form node to collect the user's email address and his issue.
![overview4.png](/assets/images/overview/get-start-05.png)
![overview4.png](/assets/images/overview/get-start-06.png)
<!-- 6. 至此，我们完成了第一个简单的对话流图，现在我们点击右上角“Debug Run”开始调试运行。 -->
6. Add a bot completion node.
![overview4.png](/assets/images/overview/get-start-07.png)
7. At this point, we completed the first dialogue flow. Now, let's click the "Debug Run" button on the upper right corner to start debugging.
![overview5.png](/assets/images/overview/get-start-08.png)
<!-- 7. 等待链接完成，测试我们的流图。 // TODO 这不能正常对话，稍后更新 -->
7. Wait for the connection to complete and test your flow.
![overview6.png](/assets/images/overview/get-start-09.png)

<!-- ## 快速发布 -->
## Publish
<!-- 选择我们刚刚测试运行好的流图，进行发布。发布之后，我们可以看见web内嵌链接，和移动端链接。更多发布相关内容请看这里。 -->
Select the flow that you just tested, then proceed with publishing. After publishing, you can see the web-embedded link and the mobile link. For more information on publishing, please refer to [this section](/docs/tutorial/release/release_project).
![overview7.png](/assets/images/overview/get-start-10.png)

<!-- ## 对话历史和Dashboard -->
## Conversation History and Dashboard
<!-- 对话历史纪录了，当前项目的所有对话信息。 -->
The conversation history records the conversation information for the current project.
![overview8.png](/assets/images/overview/get-start-11.png)
![overview9.png](/assets/images/overview/get-start-12.png)
