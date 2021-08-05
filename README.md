# PYNQ_PID_Demo
> 基于PYNQ的PID可视化

![demo](/img.png)

如何用最简单的外设实现有趣好玩的应用呢？本项目基于PYNQ-Z2平台开发PID的可视化交互程序。模型演示信号的输出跟踪矩形信号时的效果，用户既可以像在普通PC上用鼠标进行交互，也可以采用板载的开关与按键实现初始位置、P、I、D等参数的自由调节，从而呈现直观感性的效果，加深对PID经典控制算法的理解。

程序采用协程监测外设中断，在低计算资源占用的情况下达到快速，伪实时响应的目的。通过将线程阻塞使得cell的输出不关闭，以达到交互刷新输出的目的。目前PID算法以及被控对象的实现均在PS端完成，计划将其迁移至PL端实现。
