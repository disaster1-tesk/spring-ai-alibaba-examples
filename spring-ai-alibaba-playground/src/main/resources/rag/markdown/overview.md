---
title: Spring AI Alibaba 概览
keywords: [什么是 Spring AI Alibaba, Spring AI Alibab简介, Spring AI简介]
description: "Spring AI Alibaba 是一款以 Spring AI 为基础，深度集成百炼平台，支持 ChatBot、工作流、多智能体应用开发模式的 AI 框架。"
---
## 什么是 Spring AI Alibaba
<font style="color:rgb(53, 56, 65);">Spring AI Alibaba（SAA） 是一款以 Spring AI 为基础，深度集成百炼平台，支持 ChatBot、工作流、多智能体应用开发模式的 AI 框架。</font>

![spring ai alibaba architecture.png](/img/user/ai/overview/1.0.0/spring-ai-alibaba-architecture.png)

<font style="color:rgb(53, 56, 65);">在 1.0 版本中，</font><font style="color:#080808;background-color:#ffffff;">Spring AI Alibaba 提供以下核心能力，让开发者可以快速构建自己的 Agent、Workflow 或 Multi-agent 应用。</font>

1. **<font style="color:rgb(23, 26, 29);">Graph 多智能体框架。</font>**<font style="color:rgb(23, 26, 29);">基于 Spring AI Alibaba Graph 开发者可快速构建工作流、多智能体应用，无需关心流程编排、上下文记忆管理等底层实现。通过 Graph 与低代码、自规划智能体结合，为开发者提供从低代码、高代码到零代码构建智能体的更灵活选择。</font>
2. **<font style="color:rgb(23, 26, 29);">通过 AI 生态集成，解决企业智能体落地过程中关心的痛点问题。</font>**<font style="color:rgb(23, 26, 29);">Spring AI Alibaba 支持与百炼平台深度集成，提供模型接入、RAG知识库解决方案；支持 ARMS、Langfuse 等可观测产品无缝接入；支持企业级的 MCP 集成，包括 Nacos MCP Registry 分布式注册与发现、自动 Router 路由等。</font>
3. **<font style="color:rgb(53, 56, 65);">探索具备自主规划能力的通用智能体产品与平台。</font>**<font style="color:rgb(53, 56, 65);">社区发布了基于 Spring AI Alibaba 框架实现的 JManus 智能体，除了对标 OpenManus 的通用智能体能力外，我们的目标是基于 JManus 探索自主规划在智能体开发方向的应用，</font><font style="color:rgb(23, 26, 29);">为开发者提供从低代码、高代码到零代码构建智能体的更灵活选择</font><font style="color:rgb(23, 26, 29);">。</font>

### 与 Spring AI 的联系和区别
Spring AI 是 Spring 官方社区维护的开源框架，最初于 2024 年 5 月发布首个 Milestone 版本，在 2025 年 5 月正式发布首个 1.0 GA 版本。Spring AI 侧重 AI 能力构建的底层原子能力抽象以及与 Spring Boot 生态的无缝集成，如模型通信（ChatModel）、提示词（Prompt）、检索增强生成（RAG）、记忆（ChatMemory）、工具（Tool）、模型上下文协议（MCP）等，帮助 Java 开发者快速构建 AI 应用。

<font style="color:rgb(53, 56, 65);">自 2024 年 9 月正式开源以来，Spring AI Alibaba 一直与 Spring AI 社区有深度沟通合作，期间发布了多个 Milestone 版本并与很多企业客户建立的深度合作关系。在交流过程中，我们看到了低代码开发模式的优势与限制，随着业务复杂度提升客户从聊天机器人、单智能体到对多智能体架构方案的诉求，也看到了智能体开发从简单 Demo 走向生产上线过程中遇到的困难。</font>

## 快速开始
### 开发第一个 Spring AI Alibaba 应用
在 Spring Boot 工程中添加以下依赖，就可以开始您的 AI 智能体开发之旅了。

```xml
	<dependencyManagement>
		<dependencies>
			<dependency>
				<groupId>com.alibaba.cloud.ai</groupId>
				<artifactId>spring-ai-alibaba-bom</artifactId>
				<version>1.0.0.2</version>
				<type>pom</type>
				<scope>import</scope>
			</dependency>
		</dependencies>
	</dependencyManagement>

<dependencies>
  <dependency>
    <groupId>com.alibaba.cloud.ai</groupId>
    <artifactId>spring-ai-alibaba-starter-dashscope</artifactId>
  </dependency>
</dependencies>
```

您可以参考我们发布在官网的 [快速开始](./get-started/chatbot/) 了解如何开发 Chatbot、智能体或工作流等应用，总的来说，根据不同场景，您可以选择使用 `ChatClient` 或 `Spring Ai Alibaba Graph` 两个核心组件来开发 AI 应用。

### 体验官方 Playground 示例
Spring AI Alibaba 官方社区开发了一个**包含完整 “前端UI+后端实现” 的智能体 Playground 示例**，示例使用 Spring AI Alibaba 开发，可以体验聊天机器人、多轮对话、图片生成、多模态、工具调用、MCP集成、RAG知识库等所有框架核心能力。

整体运行后的界面效果如下所示：

![spring ai alibaba playground.png](/img/user/ai/overview/1.0.0/playground.png)

您可以[本地部署 Playground 示例](https://github.com/springaialibaba/spring-ai-alibaba-examples/tree/main/spring-ai-alibaba-playground)并通过浏览器访问体验，或者拷贝源码并按照自己的业务需求调整，以这种方式快速搭建一套自己的 AI 应用。



更多示例如果想通过源码示例学习更多 Spring AI Alibaba 框架用法，请参考我们的官方示例仓库：

[https://github.com/springaialibaba/spring-ai-alibaba-examples](https://github.com/springaialibaba/spring-ai-alibaba-examples)

## 开启 Spring AI Alibaba 1.0 之旅
### 支持 Spring AI 所有核心功能
Spring AI Alibaba 基于 Spring AI 构建，因此 Spring AI Alibaba 继承了 Spring AI 的所有原子能力抽象，并在此基础上扩充丰富了模型、向量存储、记忆、RAG 等核心组件适配，让其能够接入阿里云的 AI 生态。

关于 Spring AI 1.0 GA 版本，Spring AI 官方博客给出了具体说明，包括框架的一些核心设计理念与具体功能使用方式。以下是我们基于官方博客给出的解读版本，欢迎按需查阅：

+ Spring AI 核心功能详解
    - [提示（Prompt）](https://java2ai.com/blog/spring-ai-100-ga-released/?spm=5176.29160081.0.0.2856aa5c2PwbQU#%E6%8F%90%E7%A4%BAprompt)
    - [模型增强（The Augmented LLM）](https://java2ai.com/blog/spring-ai-100-ga-released/?spm=5176.29160081.0.0.2856aa5c2PwbQU#%E6%A8%A1%E5%9E%8B%E5%A2%9E%E5%BC%BAthe-augmented-llm)
    - [顾问（Advisors）](https://java2ai.com/blog/spring-ai-100-ga-released/?spm=5176.29160081.0.0.2856aa5c2PwbQU#%E9%A1%BE%E9%97%AEadvisors)
    - [检索（Retrieval）](https://java2ai.com/blog/spring-ai-100-ga-released/?spm=5176.29160081.0.0.2856aa5c2PwbQU#%E6%A3%80%E7%B4%A2retrieval)
    - [记忆（ChatMemory）](https://java2ai.com/blog/spring-ai-100-ga-released/?spm=5176.29160081.0.0.2856aa5c2PwbQU#%E8%AE%B0%E5%BF%86chatmemory)
    - [工具（Tool）](https://java2ai.com/blog/spring-ai-100-ga-released/?spm=5176.29160081.0.0.2856aa5c2PwbQU#%E5%B7%A5%E5%85%B7tool)
    - [评估（Evaluation）](https://java2ai.com/blog/spring-ai-100-ga-released/?spm=5176.29160081.0.0.2856aa5c2PwbQU#%E8%AF%84%E4%BC%B0evaluation)
    - [可观测性（Observability）](https://java2ai.com/blog/spring-ai-100-ga-released/?spm=5176.29160081.0.0.2856aa5c2PwbQU#%E5%8F%AF%E8%A7%82%E6%B5%8B%E6%80%A7observability)
    - [模型上下文协议（MCP）](https://java2ai.com/blog/spring-ai-100-ga-released/?spm=5176.29160081.0.0.2856aa5c2PwbQU#%E6%A8%A1%E5%9E%8B%E4%B8%8A%E4%B8%8B%E6%96%87%E5%8D%8F%E8%AE%AEmcp)
        * [MCP 客户端](https://java2ai.com/blog/spring-ai-100-ga-released/?spm=5176.29160081.0.0.2856aa5c2PwbQU#mcp-%E5%AE%A2%E6%88%B7%E7%AB%AF)
        * [MCP 服务器](https://java2ai.com/blog/spring-ai-100-ga-released/?spm=5176.29160081.0.0.2856aa5c2PwbQU#mcp-%E6%9C%8D%E5%8A%A1%E5%99%A8)
    - [MCP 和安全](https://java2ai.com/blog/spring-ai-100-ga-released/?spm=5176.29160081.0.0.2856aa5c2PwbQU#mcp-%E5%92%8C%E5%AE%89%E5%85%A8)

关于 Spring AI Alibaba 与阿里云 AI 生态的适配，请参考官网文档。

### Spring AI Alibaba Graph 多智能体框架
Spring AI Alibaba Graph 是社区核心实现之一，也是整个框架在设计理念上区别于 Spring AI 只做底层原子抽象的地方，Spring AI Alibaba 期望帮助开发者更容易的构建智能体应用。基于 Graph 开发者可以构建工作流、多智能体应用。Spring AI Alibaba Graph 在设计理念上借鉴 Langgraph，因此在一定程度上可以理解为是 Java 版的 Langgraph 实现，社区在此基础上增加了大量预置 Node、简化了 State 定义过程等，让开发者更容易编写对等低代码平台的工作流、多智能体等。



Spring AI Alibaba Graph 核心能力：

+ 支持 Multi-agent，内置 ReAct Agent、Supervisor 等常规智能体模式
+ 支持工作流，内置工作流节点，与主流低代码平台对齐
+ 原生支持 Streaming
+ Human-in-the-loop，通过人类确认节点，支持修改状态、恢复执行
+ 支持记忆与持久存储
+ 支持流程快照
+ 支持嵌套分支、并行分支
+ PlantUML、Mermaid 可视化导出



关于 Graph 的具体使用方式，请关注官网文档更新。在下文中我们会介绍官方发布的基于 Spring AI Alibaba 实现的通用智能体平台，您可以把这些官方智能体实现当作 Graph 的最佳应用实践。

### 企业级 AI 应用生态集成
在 Agent 生产落地过程中，用户需要解决智能体效果评估、MCP 工具集成、Prompt 管理、Token 上下文、可视化 Tracing等各种问题，Spring AI Alibaba 通过与 Nacos3、Higress AI 网关、阿里云 ARMS、阿里云向量检索数据库、百炼智能体平台等深度集成，提供全面的智能体企业级生产解决方案，加速智能体从 Demo 走向生产落地。

![spring ai alibaba ecosystem.png](/img/user/ai/overview/1.0.0/spring-ai-alibaba-ecosystem.png)

1. **企业级 MCP 部署与代理方案**

Spring AI Alibaba MCP 通过集成 Nacos MCP Registry，支持 MCP Server 分布式部署与负载均衡调用。对于存量 Spring Cloud、Dubbo 等应用，支持零代码改造实现 API 到 MCP 服务发布，开发者可通过 Spring AI Alibaba MCP 开发自己的 MCP Server 服务代理，即可支持 Nacos 中心 MCP 元数据的自动加载。

2. **AI 网关集成提升模型调用稳定性与灵活性**

如果您使用 Higress 作为后端模型代理，则可以通过 OpenAI 标准接口接入 Higress AI 模型代理服务，只需要使用`spring-ai-starter-model-openai`就可以了。

如果您有存量的 API 服务，需要在无需修改代码的情况下，可以使用 Higress 作为 API 到 MCP 服务的代理方案。

3. **降低企业数据整合成本，提升 AI 数据应用效果**

**a. 百炼 RAG 知识库**

<font style="color:rgb(53, 56, 65);">百炼是一款可视化 AI 智能体应用开发平台，它提供 RAG 知识库管理能力。简单来讲，您可以将私有数据上传到百炼平台，借助百炼平台数据解析、切片、向量化等能力实现数据向量化预处理，处理后的数据可用于后续 Spring AI Alibaba 智能体应用检索，借用百炼平台强大的数据处理效果。</font>

**b. 百炼析言 ChatBI，从自然语言到 SQL 自动生成**

Spring AI Alibaba Nl2sql 模块可基于大模型的 ChatBI 技术，帮助用户轻松实现自然语言交互的数据分析，理解用户的数据库 schema，帮助用户自动生成 SQL 查询语句。无论是简单的条件过滤还是复杂的聚合统计、多表关联，都能准确生成对应的 SQL 语句。

4. **可观测与效果评估，加速智能体从 Demo 走向生产落地**

Spring AI 在多个关键节点都做了 SDK 默认埋点，用来记录运行过程中的 metrics 与 tracing 信息，这包括模型调用、向量检索、工具调用等关键环节的调用情况。Spring AI tracing 信息兼容 OpenTelemetry，因此理论上可接入市面上主流的开源平台入 Langfuse，或者阿里云 ARMS。

## 从聊天机器人、工作流到多智能体
### 聊天机器人（ChatBot）
AI 应用开发不止是无状态大模型的 API 调用过程，由于大模型预训练的特性，AI 应用还需要具备领域数据检索(RAG)、会话记忆（Memory）、工具调用（Tool）等集成能力，这些对外集成统称为模型增强模式（The Augmented LLM），它允许开发者将自己的数据和外部 API 直接带入模型的推理过程。

<img src="/img/user/ai/overview/1.0.0/chatbot.png" alt="chatbot" style="max-width: 500px; height: auto;" />

> 此图出自 Anthropic《Building Effective AI Agents》文章

ChatClient 是 Spring AI 中最核心的组件，开发者可以使用 ChatClient 开发自己的聊天机器人或智能体应用，ChatClient 支持模型增强模式，为模型调用挂载 Retrieval、Tools、Memory 等外部数据与服务。



```java
Flux<String> response = chatClient.prompt(query)
        .tools(toolCallbacks)
        .advisors(new QuestionAnswerAdvisor())
        .stream()
        .content();
```



<font style="color:rgb(38, 38, 38);">我们这里把 ChatClient 开发的 AI 应用叫做单智能体应用，这可能是我们最理想的智能体开发模式，它足够简单直接，即把所有的工具、上下文信息等给到模型，由模型持续决策、迭代直到最终完成任务解答。然而，事情远没有那么简单，模型的能力还远未达到我们想要的效果，当我们给模型的上下文、工具过多时，整体效果就会变差，有时事情的走向会严重偏离我们的预期。因此，我们考虑把复杂的问题拆解开来，当前有两种常用模式：</font>**<font style="color:rgb(38, 38, 38);">工作流和多智能体</font>**<font style="color:rgb(38, 38, 38);">。</font>

### 工作流（Workflow）
**<font style="color:rgb(38, 38, 38);">工作流</font>**<font style="color:rgb(38, 38, 38);">是以相对固化的模式来人为的拆解任务，将一个大的任务拆解为一个固化的有多个分支的流程。工作流的优势是确定性强，模型作为流程中的一个节点起到的更多是一个分类决策的职责，因此它更适合意图识别等类别属性强的应用场景。工作流也有明显的劣势，它要求开发人员对业务流程有深刻的理解，整个流程是由人绘制的，模型在其中更多的只是内容生成、总结、分类识别的作用，并不能最大化利用模型的推理能力，因此很多人诟病这种模式是不够智能的。</font>

<font style="color:rgb(38, 38, 38);"></font>

<font style="color:rgb(38, 38, 38);">用 Spring AI Alibaba Graph 可以轻松开发工作流，声明不同的节点，并将节点串联成一个流程图。</font>


![spring ai alibaba workflow](/img/user/ai/overview/1.0.0/workflow.png)



<font style="color:rgb(38, 38, 38);">值得注意的是，Spring AI Alibaba Graph 中提供大量预置节点，这些节点可以对标到市面上主流的如 Dify、百炼等低代码平台，典型节点包括 LlmNode（大模型节点）、QuestionClassifierNode（问题分类节点）、ToolNode（工具节点）等，为用户免去重复开发定义负担，只需要专注流程串联。</font>

<font style="color:rgb(38, 38, 38);"></font>

如以上是一个可视化绘制的“用户评价分类系统”工作流，对应 Spring AI Alibaba Graph 代码如下所示：


```java
StateGraph stateGraph = new StateGraph("Consumer Service Workflow Demo", stateFactory)
			.addNode("feedback_classifier", node_async(feedbackClassifier))
			.addNode("specific_question_classifier", node_async(specificQuestionClassifier))
			.addNode("recorder", node_async(new RecordingNode()))

			.addEdge(START, "feedback_classifier")
			.addConditionalEdges("feedback_classifier",edge_async(new CustomerServiceController.FeedbackQuestionDispatcher()),Map.of("positive", "recorder", "negative", "specific_question_classifier"))
			.addConditionalEdges("specific_question_classifier",edge_async(new CustomerServiceController.SpecificQuestionDispatcher()),Map.of("after-sale", "recorder", "transportation", "recorder", "quality", "recorder", "others","recorder"))
			.addEdge("recorder", END);
```

### 多智能体（Multi-agent）
复杂任务拆解的另一种解决方案是**多智能体**，相比于工作流，多智能体虽也遵循特定的流程，但是在整个决策、执行流程上具备更多的自主性和灵活性。多个子智能体间通过通信协作完成，最终完成任务解答，在业界，有多种常见的多智能体通信模型，如下图是几个典型示例：

<img src="/img/user/ai/overview/1.0.0/multi-agent.png" alt="multi-agent" style="max-width: 500px; height: auto;" />

> 图片出自 Langchain 官方博客

Spring AI Alibaba Graph 可用来开发各种多智能体模式。官方社区目前发布了几款基于 Spring AI Alibaba Graph 开发的智能体产品，包括通用智能体 JManus、DeepResearch 智能体、AgentScope 等。

## 打造下一代通用智能体平台
Spring AI Alibaba 定位以 `ChatClient`、`Graph` 抽象为核心的智能体框架以及围绕框架的生态集成，用来帮助用户开发快速构建企业级 AI 智能体。

随着通用智能体模式的快速发展，社区也在基于 Spring AI Alibaba 探索具备自主规划能力的智能体产品与平台，目前已经发布了 JManus、DeepResearch 两款产品，通过 JManus 等智能体产品，一方面探索智能体在解决日常生活、工作效率等开放性问题方面的无限空间；另一方面，社区也在智能体开发平台、深度搜索等垂直领域持续探索，期望在低代码平台、高代码框架之外，为开发者带来面向自然语言的零代码智能体研发体验。

### JManus 智能体平台
在我们最开始发布 JManus 之时，给它的定位是一款完全以 Java 语言为核心、彻底开源的 OpenManus 复刻实现，基于 Spring AI Alibaba 实现的通用 AI Agent 产品，包含一个设计良好的前端 UI 交互界面。


随着我们对于通用智能体等方向的深度探索，我们对于 JManus 通用智能体的终端产品定位也进行了调整。Manus 的横空出世，让通用智能体自动规划、执行规划的能力给了人们无限想象空间，它非常擅长解决开放性问题，在日常生活、工作等场景都能有广泛的应用。但在实践中人们也开始认识到，基于当前以及未来相当长的时间内模型能力，完全依赖通用智能体的自动规划模式很难解决一些确定性极强的企业场景问题。企业级业务场景的典型特点是确定性，我们需要定制化的工具、子agent，需要稳定而又确定性强的规划与流程，为此，我们期望 JManus 能成为一个智能体开发平台，让用户能以最直观、低成本的方式构建自己垂直领域的智能体实现。

![spring ai alibaba jmanus](/img/user/ai/overview/1.0.0/jmanus.png)

当前，Jmanus 具备以下核心能力：

+ **<font style="color:#3b3b3b;background-color:#f8f8f8;">完整实现了 OpenManus 多智能体产品</font>**<font style="color:#3b3b3b;background-color:#f8f8f8;">
</font><font style="color:#3b3b3b;background-color:#f8f8f8;">JManus 完整兑现了 OpenManus 产品能力，用户可以基于 UI 界面使用产品功能，JManus 可以基于自动规划模式帮助用户完成问题解答。</font>
+ **<font style="color:#3b3b3b;background-color:#f8f8f8;">无缝支持 MCP（Model Context Protocol）工具集成</font>**<font style="color:#3b3b3b;background-color:#f8f8f8;">
</font><font style="color:#3b3b3b;background-color:#f8f8f8;">这意味着 Agent 不仅可以调用本地或云端的大语言模型，还能与各类外部服务、API、数据库等进行深度交互，极大拓展了应用场景和能力边界。</font>
+ **<font style="color:#3b3b3b;background-color:#f8f8f8;">原生支持 PLAN-ACT 模式</font>**<font style="color:#3b3b3b;background-color:#f8f8f8;">
</font><font style="color:#3b3b3b;background-color:#f8f8f8;">能够让 Agent 具备复杂推理、分步执行和动态调整的能力，适用于多轮对话、复杂决策、自动化流程等高阶 AI 应用场景。</font>
+ **<font style="color:#3b3b3b;background-color:#f8f8f8;">支持通过 UI 界面配置 Agent</font>**<font style="color:#3b3b3b;background-color:#f8f8f8;">
</font><font style="color:#3b3b3b;background-color:#f8f8f8;">开发者和运维人员无需修改底层代码，只需在直观的Web管理界面上进行简单操作，就能灵活调整Agent的参数、模型和工具，还可以调整任务规划，大大提升了易用性和运维效率。</font>
+ **<font style="color:#3b3b3b;background-color:#f8f8f8;">自动生成基于 SAA 的智能体工程</font>**

<font style="color:#3b3b3b;background-color:#f8f8f8;">用户通过自然语言与 JManus 交互，生成规划并沉淀为特定垂直方向的固化解决方案。如果您不想将运行态限定在平台之上，我们正在探索与低代码平台、框架脚手架的深度整合，支持规划转换为具备对等能力的 Spring AI Alibaba 工程。</font>

<font style="color:#3b3b3b;background-color:#f8f8f8;"></font>

<font style="background-color:#f8f8f8;">JManus 智能体平台还在持续开发建设中，请关注</font>[<font style="background-color:#f8f8f8;"> 官方仓库源码</font>](https://github.com/alibaba/spring-ai-alibaba/tree/main/spring-ai-alibaba-jmanus/)<font style="background-color:#f8f8f8;"> 及后续发布动态。</font>

### DeepResearch 智能体
<font style="color:rgb(31, 35, 40);">DeepResearch 是一款基于 Spring AI Alibaba Graph 开发的 Deep Research 智能体, 包含完整的前端 Web UI（开发中） 和后端实现，DeepResearch 支持一系列精心设计的工具如 Web Search（网络查询）、Crawling（爬虫）、Python 脚本引擎等，可以借助大模型与工具能力，帮助用户完成各类深度调研报告。</font>

<font style="color:rgb(31, 35, 40);"></font>

<font style="color:rgb(31, 35, 40);">以下是 DeepResearch 多智能体应用架构：</font>


<img src="/img/user/ai/overview/1.0.0/deepresearch.png" alt="architecture" style="max-width: 740px; height: 508px" />



