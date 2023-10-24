## 为什么需要autogen

在使用langchain & code interpreter 过程中，对性能和准确率和性能都有着更高的要求。

Autogen在这两方面来看，都有一定的提升。

根据autogen的论文和自己体验确实能得到一些答案。

**性能对比：**
<img width="1440" alt="Performance" src="https://github.com/huqianghui/autogen_experiments/assets/7360524/7660c70d-45e7-47af-afd2-35a329241fa9">

**正确率对比**
<img width="1440" alt="Correctness" src="https://github.com/huqianghui/autogen_experiments/assets/7360524/c3ffae37-b6c0-4280-b476-0daeab5a8675">

## AutoGen是什么

AutoGen is a framework that enables the development of LLM applications using multiple agents that can converse with each other to solve tasks. AutoGen agents are customizable, conversable, and seamlessly allow human participation. They can operate in various modes that employ combinations of LLMs, human inputs, and tools.

![AutoGen Overview](https://github.com/microsoft/autogen/blob/main/website/static/img/autogen_agentchat.png)

- AutoGen enables building next-gen LLM applications based on **multi-agent conversations** with minimal effort. It simplifies the orchestration, automation, and optimization of a complex LLM workflow. It maximizes the performance of LLM models and overcomes their weaknesses.
- It supports **diverse conversation patterns** for complex workflows. With customizable and conversable agents, developers can use AutoGen to build a wide range of conversation patterns concerning conversation autonomy,
  the number of agents, and agent conversation topology.
- It provides a collection of working systems with different complexities. These systems span a **wide range of applications** from various domains and complexities. This demonstrates how AutoGen can easily support diverse conversation patterns.
- AutoGen provides a drop-in replacement of `openai.Completion` or `openai.ChatCompletion` as an **enhanced inference API**. It allows easy performance tuning, utilities like API unification and caching, and advanced usage patterns, such as error handling, multi-config inference, context programming, etc.

AutoGen is powered by collaborative [research studies](https://microsoft.github.io/autogen/docs/Research) from Microsoft, Penn State University, and the University of Washington.

## Autogen与其他多agent的框架对比
<img width="1440" alt="multi_frameworks_compare" src="https://github.com/huqianghui/autogen_experiments/assets/7360524/8ebf1272-209f-481b-9ed5-9554bb5fd0d0">

AutoGen的主要原因是：

1. 利用多个 agent 的协作来提高编码的效率和安全性。通过多角色和多轮来完善内容。
   
2. 活地定义 agent 的行为和交互模式，通过自然语言或编程语言来控制对话流程。各个角色定位更加清晰。
   
3. 使用不同的 LLMs 来实现不同的功能，例如生成代码，执行代码，验证代码，解释结果等。这些功能内置的，通过多轮还强化内容。
   
4. 轻松地扩展和重用现有的 agent，通过注册自定义的回复函数来定制 agent 的行为。

## Autogen默认system prompt
<img width="1440" alt="SystemPrompt" src="https://github.com/huqianghui/autogen_experiments/assets/7360524/7392ff52-b06c-436a-808b-99658dbab60b">

从这个prompt可以看到不同类型指令，完成一个比较好的结果。

## Autogen未来发展方向

<img width="1440" alt="Futurework" src="https://github.com/huqianghui/autogen_experiments/assets/7360524/fc18110e-83ad-45bd-b9c5-f2ffe4fa3290">



