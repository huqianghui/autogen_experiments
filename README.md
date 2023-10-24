# AutoGen

<!-- <p align="center">
    <img src="https://github.com/microsoft/autogen/blob/main/website/static/img/flaml.svg"  width=200>
    <br>
</p> -->

:fire: autogen has graduated from [FLAML](https://github.com/microsoft/FLAML) into a new project.

<!-- :fire: Heads-up: We're preparing to migrate [autogen](https://microsoft.github.io/FLAML/docs/Use-Cases/Autogen) into a dedicated Github repository. Alongside this move, we'll also launch a dedicated Discord server and a website for comprehensive documentation.

:fire: FLAML is highlighted in OpenAI's [cookbook](https://github.com/openai/openai-cookbook#related-resources-from-around-the-web).

:fire: [autogen](https://microsoft.github.io/autogen/) is released with support for ChatGPT and GPT-4, based on [Cost-Effective Hyperparameter Optimization for Large Language Model Generation Inference](https://arxiv.org/abs/2303.04673).

:fire: FLAML supports Code-First AutoML & Tuning – Private Preview in [Microsoft Fabric Data Science](https://learn.microsoft.com/en-us/fabric/data-science/). -->

## What is AutoGen

AutoGen is a framework that enables the development of LLM applications using multiple agents that can converse with each other to solve tasks. AutoGen agents are customizable, conversable, and seamlessly allow human participation. They can operate in various modes that employ combinations of LLMs, human inputs, and tools.

![AutoGen Overview](https://github.com/microsoft/autogen/blob/main/website/static/img/autogen_agentchat.png)

- AutoGen enables building next-gen LLM applications based on **multi-agent conversations** with minimal effort. It simplifies the orchestration, automation, and optimization of a complex LLM workflow. It maximizes the performance of LLM models and overcomes their weaknesses.
- It supports **diverse conversation patterns** for complex workflows. With customizable and conversable agents, developers can use AutoGen to build a wide range of conversation patterns concerning conversation autonomy,
  the number of agents, and agent conversation topology.
- It provides a collection of working systems with different complexities. These systems span a **wide range of applications** from various domains and complexities. This demonstrates how AutoGen can easily support diverse conversation patterns.
- AutoGen provides a drop-in replacement of `openai.Completion` or `openai.ChatCompletion` as an **enhanced inference API**. It allows easy performance tuning, utilities like API unification and caching, and advanced usage patterns, such as error handling, multi-config inference, context programming, etc.

AutoGen is powered by collaborative [research studies](https://microsoft.github.io/autogen/docs/Research) from Microsoft, Penn State University, and the University of Washington.
