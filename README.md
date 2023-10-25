## 为什么需要autogen

在使用langchain & code interpreter 过程中，对性能和准确率和性能都有着更高的要求。

而Autogen在这两方面来看，都有一定的提升,而且在中间过程可以接受人的反馈。

<img width="720" alt="autogen" src="https://github.com/huqianghui/autogen_experiments/assets/7360524/8f2797f2-56f0-4e10-beda-39dd063eb49c">

下面根据autogen的论文和实际测试样例，做一些说明。

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

## 使用相同命令下，不同的表现

**query the books table, group by column "authors" of top 5 in bar picture**

这里有一个authors是为null，python代码会出现异常。
Autogen能检测到后。优化方向有随机性，1）对数据做过滤清洗最后剩下四条,2）对null用""处理，都得到最终结果。

<img width="1440" alt="sql_null" src="https://github.com/huqianghui/autogen_experiments/assets/7360524/d201fac7-57df-4f71-97a2-33fa911b202b">
<img width="1440" alt="sql_null2" src="https://github.com/huqianghui/autogen_experiments/assets/7360524/63bb43fe-5982-4678-8b1c-c423f90399f7">
<img width="1440" alt="Screenshot 2023-10-24 at 13 52 54" src="https://github.com/huqianghui/autogen_experiments/assets/7360524/ff2e3f07-e574-4477-86d0-ffb4531e475f">

## Autogen默认system prompt
<img width="1440" alt="SystemPrompt" src="https://github.com/huqianghui/autogen_experiments/assets/7360524/7392ff52-b06c-436a-808b-99658dbab60b">

从这个prompt可以看到不同类型指令，完成一个比较好的结果。

## Autogen未来发展方向

<img width="1440" alt="Futurework" src="https://github.com/huqianghui/autogen_experiments/assets/7360524/fc18110e-83ad-45bd-b9c5-f2ffe4fa3290">

## 通过chainlit快速搭建一个WebUI 应用
<img width="1440" alt="Screenshot 2023-10-24 at 22 44 58" src="https://github.com/huqianghui/autogen_experiments/assets/7360524/7325cfab-3372-439d-ae1b-6b1481a6bbf3">


