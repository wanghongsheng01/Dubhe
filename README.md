# Dubhe
Dubhe is an open-source deep learning framework.
## OneFlow 系统架构
* Python 端<br>
启动 编译 运行
构建逻辑图（Job）
计算图执行引擎
发送控制指令 输入 处理输出

* 编译期 Compiler<br>
编译期 Compiler 将用户定义的逻辑上的计算图（Job）进行编译，产出实际上的物理计算图（Plan）

* 运行期 Runtime<br>
运行期 Runtime 根据 Plan 创建真正的执行图（计算图执行引擎）——由 Actor 组成的去中心化流式计算图。每个 Actor 各司其职，有的 Actor 负责接收 Python 端的控制信号，有的 Actor 负责加载数据，有的 Actor 负责初始化模型，计算，更新，存储，传输，...,有的 Actor 负责返还给 Python 端数据，数据在计算图中流动，实现模型训练。

## Oneflow 框架引擎总体架构图
![image](https://user-images.githubusercontent.com/31394900/122934181-e3348f00-d3a1-11eb-87a3-b613e882938d.png)


