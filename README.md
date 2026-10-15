# OpenHUTB


该社区提供一个包含人车代理（学术研究）、模拟器（技术开发包括数据驱动、机理仿真、界面渲染）、现实场景（艺术增强）的 [模拟器](https://openhutb.github.io) ，代理包括[感知](https://openhutb.github.io/doc/algorithms/perception/) （连接）、[规划](https://openhutb.github.io/doc/algorithms/planning/) （符号）、[控制](https://openhutb.github.io/doc/algorithms/control/) （行为）；模拟器包括Python与C++的接口（正向创建、反向构建）、LibCarla、虚幻引擎插件；现实场景包括 [静态场景孪生](https://openhutb.github.io/doc/adv_digital_twin/) 、[动态场景孪生](https://github.com/OpenHUTB/traffic_twin/) 。
人车模拟器的技术架构入下图所示：

<a href ="https://github.com/OpenHUTB/.github/blob/master/fig/repositories.md">
<img src="https://github.com/OpenHUTB/.github/blob/master/profile/repositories.png?raw=true" width="40%" >
</a>


<!--所有项目关系的思维导图。-->
<!-- 使用markmap进行编辑并生成svg：https://markmap.js.org/repl -->
<!-- 在profile/markmap.md中保存图的数据 -->
<!-- svg图片预览：https://raw.githack.com/ -->

## 社区项目之间的关系

```mermaid
graph LR
    A[人的模型 <a href='https://github.com/OpenHUTB/opensim-core'>OpenSim</a>] --> B[多体物理 <a href='https://github.com/OpenHUTB/chrono'>chrono</a>]
    B --> C[<b>人车模拟器 <a href='https://github.com/OpenHUTB/hutb'>hutb</a> </b>]
    A --> F[<a href='https://github.com/MyoHub/myoconverter'>格式转换</a> <a href='https://github.com/OpenHUTB/mujoco_plugin'>mujoco_plugin</a> ]
    F --> C
    C --> D[文档 <a href='https://github.com/OpenHUTB/doc'>doc</a>]
    D --> H[无人机文档 <a href='https://github.com/OpenHUTB/air_doc'>air_doc</a>]
    D --> I[神经原理 <a href='https://github.com/OpenHUTB/neuro'>neuro</a>]
    I --> J[规划 <a href='https://github.com/OpenHUTB/PFC'>PFC</a>]
    I --> K[控制原理 <a href='https://github.com/OpenHUTB/move'>move</a>]
    K --> A
    L[模拟引擎 <a href='https://github.com/OpenHUTB/engine'>engine</a>] --> C
    L --> M[引擎文档 <a href='https://github.com/OpenHUTB/cpp'>engine_doc</a>]
    M --> S[C++ 文档 <a href='https://github.com/OpenHUTB/cpp'>cpp</a>]
    D --> M
    L --> N[无人机模拟器 <a href='https://github.com/OpenHUTB/air'>air</a>]
    N --> C
    N --> H
    D --> R[<a href='https://github.com/OpenHUTB/.github/blob/master/README.md#%E5%BA%94%E7%94%A8%E5%88%97%E8%A1%A8'>应用列表</a>]
    D --> Q[<a href='https://github.com/OpenHUTB/.github/blob/master/README.md#%E5%B7%A5%E5%85%B7%E5%88%97%E8%A1%A8'>工具列表</a>]


    style I fill:#e1f5fe
    style C fill:#ccffcc
    style D fill:#fff3e0
    style Q fill:#f3e5f5
    style R fill:#F5DEB3
```



### 应用列表

```mermaid
graph LR

    A --> F[人的移动 <a href='https://github.com/OpenHUTB/locomotion'>locomotion</a>]
    F --> L[人的模拟 <a href='https://github.com/OpenHUTB/carla-pedestrians'>carla-pedestrians</a>]

    A --> G[自动驾驶测试 <a href='https://github.com/OpenHUTB/platform'>platform</a>]
    G --> H[强化学习 <a href='https://github.com/OpenHUTB/carla_rl'>carla_rl</a>]
    H --> K[<a href='https://github.com/OpenHUTB/Carla_Autonomous_Driving'>Carla_Autonomous_Driving</a>]
    H --> I[模仿学习 <a href='https://github.com/OpenHUTB/carla-roach'>carla-roach</a>]
    H --> J[多视角 <a href='https://github.com/OpenHUTB/CILv2_multiview'>CILv2_multiview</a>]
    G --> M[安全场景生成 <a href='https://github.com/OpenHUTB/ChatScene'>ChatScene</a>]

    A[应用列表] --> B[智慧交通 <a href='https://github.com/OpenHUTB/intelligent_traffic/'>intelligent_traffic</a>]
    B --> C[交通孪生 <a href='https://github.com/OpenHUTB/traffic_twin/'>traffic_twin</a>]
    C --> N[轨迹跟踪 <a href='https://github.com/OpenHUTB/Self_Driving_Car_Trajectory_Tracking'>Trajectory_Tracking</a>]
    B --> D[模拟端 <a href='https://github.com/OpenHUTB/driving/'>driving</a> ]
    O --> E[交通大模型 <a href='https://github.com/OpenHUTB/traffic_llm'>traffic_llm</a>]
    O --> P[VSCode插件 <a href='https://github.com/OpenHUTB/vsc'>vsc</a>]
    B --> O[<a href='https://github.com/OpenHUTB/mcp'>mcp</a>]

    style A fill:#F5DEB3
```


### 工具列表

```mermaid
graph LR
    A[工具列表 <a href='https://github.com/OpenHUTB/chrono'>.github</a>] --> B[<a href='https://github.com/OpenHUTB/latex'>latex</a> 模板]
    B --> C[课程设计 <a href='https://github.com/OpenHUTB/course'>course</a>]
    B --> D[研究生论文 <a href='https://github.com/OpenHUTB/master'>master</a>]
    B --> E[本科毕设 <a href='https://github.com/OpenHUTB/undergraduate'>undergraduate</a>]
    E --> M[<a href='https://github.com/OpenHUTB/powerpoint2pdf'>sim</a>]
    D --> N[<a href='https://github.com/OpenHUTB/emotion'>emotion</a>]
    G --> F[<a href='https://github.com/OpenHUTB/powerpoint2pdf'>powerpoint2pdf</a>]
    A --> G[工具脚本 <a href='https://github.com/OpenHUTB/utils'>utils</a>]
    G --> O[文档生成 <a href='https://github.com/OpenHUTB/mkdocs'>mkdocs</a>]
    G --> H[<a href='https://github.com/OpenHUTB/matlab'>matlab</a>]
    H --> I[<a href='https://github.com/OpenHUTB/matlab_exe_unpack'>matlab_exe_unpack</a>]
    H --> J[<a href='https://github.com/OpenHUTB/matlab_pfile_unpack'>matlab_pfile_unpack</a>]
    A --> K[<a href='https://github.com/OpenHUTB/ros'>ros</a>]
    K --> L[<a href='https://github.com/OpenHUTB/ros-bridge'>ros-bridge</a>]

    style A fill:#f3e5f5
```

## 我的开源参与计划

我想先把社区里几篇经常会用到的说明读明白，再找出照着操作时容易卡住的地方。当前更适合从文档入手：一次处理一个具体问题，把出现位置、修改理由和检查结果说清楚。

### 先把入口走通

链接写得像是正确的，不代表点开后就能到达目标。阅读发布指南时，我会核对邮箱显示文字和实际收件地址是否一致；遇到软件下载链接，也会确认页面对应的产品。对于失效或指向错误的入口，先记录问题，再单独提交修正。

### 再把排查顺序理清

环境配置出问题时，直接给出一个大范围的操作，往往看不出原因。我会先区分本机能否访问、端口是否发布、其他设备能否连接，再整理成简短步骤。修改说明时写清楚命令在哪里运行、结果应该看什么，涉及网络规则时只调整需要的端口。

### 遇到概念问题，查清再改

参考文献条目的 key 需要唯一，与同一篇文献能否多次引用，是两个不同的问题。这类表述我会结合示例和原始说明核对，避免把有条件的处理方法写成通用结论。修改后同时检查正文、示例和总结，防止前后说法不一致。

每次提交前，我会查看最终差异，确认没有混入其他页面的修改，并打开文档网页核对链接、代码和列表。参与审核时也会实际查看改动指向的内容；发现问题就说明位置和原因，能确认通过的再给出通过意见。后续会继续跟进讨论，把收到的建议补进对应修改。

本轮记录：

- 邮箱入口：[问题 #251](https://github.com/OpenHUTB/.github/issues/251)、[修改 #250](https://github.com/OpenHUTB/.github/pull/250)。
- GitLab 访问排查：[问题 #252](https://github.com/OpenHUTB/.github/issues/252)、[修改 #253](https://github.com/OpenHUTB/.github/pull/253)。
- 参考文献说明：[问题 #254](https://github.com/OpenHUTB/.github/issues/254)、[修改 #255](https://github.com/OpenHUTB/.github/pull/255)。















