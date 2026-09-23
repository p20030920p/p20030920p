<h2>QuanQuan 🤖</h2>

Robotics: ROS 2, autonomous navigation, LiDAR point clouds, multi-robot coordination.

## Work

### SVOR — training-free snow removal for spinning LiDAR

![Snow points removed frame by frame](assets/snowclear-desnow.gif)

Point-wise snow removal for spinning LiDAR, no training and no learned weights. 16 scenes / 1 620
frames of WADS: **F1 92.8**; on the same 101 frames it matches CRFOR (RA-L 2023) at **≈ 1 900×** its
speed (9 ms vs 17 132 ms per frame), CPU only on a thin-and-light laptop (MateBook 14, i5-1240P,
`OMP_NUM_THREADS=2`). ROS-free C++17 core, byte-exact regression gate. Paper in preparation.

### [Sim2Real-AlgoBench](https://github.com/p20030920p/Sim2Real-AlgoBench) — three-wheeled omnidirectional autonomy

![Autonomous run: Gazebo on the left, the navigation stack in RViz on the right](assets/sim2real.gif)

One start signal, then AMCL, Nav2 search, green-marker detection and the finish-pad approach — a
competition task run end to end, and completed on the real vehicle. Seven interchangeable global
planners behind one Nav2 plugin interface; every run writes a JSON report.

### [miku-arm-ros2](https://github.com/p20030920p/miku-arm-ros2) — 6-axis arm control

![Simulation: a recorded teach path replayed](assets/miku-arm.gif)

![The real arm on the bench following a goal dragged in RViz](assets/miku-arm-real.gif)

ROS 2 driver and control stack for a 6-axis Damiao-motor arm: KDL IK, MIT-mode teaching with gravity
compensation, MoveIt 2, and a protocol-level simulator that runs the real driver binary against a
virtual board — **13 checks pass with no hardware**. Simulation above, the real arm below.

<details>
<summary>中文</summary>

机器人方向：ROS 2、自主导航、LiDAR 点云、多机器人调度。

## 项目

### SVOR —— 旋转式 LiDAR 免训练去雪

![逐帧剔除雪点](assets/snowclear-desnow.gif)

逐点去雪，无需训练与学习权重。WADS 16 场景 / 1 620 帧 **F1 92.8**；同一批 101 帧上与 CRFOR（RA-L 2023）
精度相当、速度快 **≈ 1 900 倍**（9 ms vs 17 132 ms 每帧），纯 CPU、轻薄本（MateBook 14，i5-1240P，
`OMP_NUM_THREADS=2`）。核心不依赖 ROS，带逐字节回归门禁。论文投稿中。

### [Sim2Real-AlgoBench](https://github.com/p20030920p/Sim2Real-AlgoBench) —— 三轮全向自主导航

![自主运行：左 Gazebo，右 RViz](assets/sim2real.gif)

一次启动信号后 AMCL 定位、Nav2 搜索、绿标识别、驶入终点区——比赛任务端到端跑通，并在实车上完赛。
七种全局规划器挂在同一个 Nav2 插件接口后，每次运行写出 JSON 报告。

### [miku-arm-ros2](https://github.com/p20030920p/miku-arm-ros2) —— 六轴机械臂控制

![仿真：示教轨迹回放](assets/miku-arm.gif)

![实机：跟随 RViz 中拖动的目标](assets/miku-arm-real.gif)

六轴达妙电机机械臂的 ROS 2 驱动与控制栈：KDL 逆解、MIT 示教与重力补偿、MoveIt 2；协议级仿真器让真实
驱动二进制对接虚拟驱动板，**13 项检查无需硬件**。上为仿真，下为实机。

</details>
