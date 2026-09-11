<h2> I'm QuanQuan 🤖</h2>
<p><em>Robotics learner — autonomous navigation, LiDAR point clouds, and multi-robot coordination. Mostly on ROS 2 Jazzy, with ROS 1 Noetic behind it.</em></p>
<img width="28%" align="right" alt="RViz costmap from Sim2Real-AlgoBench: the competition map with inflated obstacle layers and the planned path to the finish pad" src="./assets/sim2real-rviz.png">

<div align="left">

<i>Let's Connect:</i><br>

<a href="https://github.com/p20030920p" target="_blank"><img src="https://img.shields.io/badge/GitHub-p20030920p-181717?style=flat-square&logo=github&logoColor=white" alt="GitHub"></a>

</div>

**Languages and Tools:**

<img width="480" src="https://skillicons.dev/icons?i=cpp,python,matlab,ros,opencv,linux,git,bash,cmake,vscode&theme=dark" alt="C++, Python, MATLAB, ROS, OpenCV, Linux, Git, Bash, CMake, VS Code">

## Work

### [Sim2Real-AlgoBench](https://github.com/p20030920p/Sim2Real-AlgoBench) — three-wheeled omnidirectional autonomy benchmark

One fixed task, one fixed interface contract, one fixed metric set, evaluated twice: in simulation and on a physical robot. The robot gets one start signal, searches a known map for a green A4 marker on a wall, drives onto the yellow finish pad in front of it, and holds still for three seconds. No goal pose is published by hand — detection ends the run, not geometry.

- **Chassis** — three-wheeled omnidirectional drive, URDF/Xacro, LiDAR, camera, `ros2_control`
- **Localization** — SLAM Toolbox mapping, Nav2 Map Saver, AMCL against a prior grid map
- **Planning** — safe search viewpoints from the free-space connected component, then Theta\* any-angle global planning
- **Control** — MPPI `Omni`, with `/cmd_vel` arbitration that guarantees a single publisher
- **Worlds** — a nominal world and a stress world with moving obstacles, low traction, rough ground, and varying illumination

*ROS 2 Jazzy · Gazebo Sim 8 · C++17 / Python*

### [FleetFlow](https://github.com/p20030920p/FleetFlow) — multi-AGV material transport in a textile mill

Ten AGVs move material barrels between carding, drawing and roving machines in a Gazebo factory, driven by a priority task scheduler and a per-robot `move_base` navigation stack. A live control centre reports fleet positions, machine states and per-process completion, and the repository ships a batch-experiment pipeline that turns runs into CSV data, reports and LaTeX tables.

*ROS 1 Noetic · Gazebo 11 · Python 3*

### SnowClear — training-free snow-point detection and removal for spinning LiDAR

*Private repository.* Point-wise removal of snowfall noise at frame rate, on CPU only: no training, no GPU, no learned weights. One raw frame in; a de-snowed cloud plus the snow indices out, kept in the coordinate and index space of the original input cloud. Around 10 ms per frame in a Release build, with byte-for-byte regression reproducibility.

*ROS 2 Jazzy · C++17 · PCL*

### SLAM — mapping and navigation stack

*Private repository.* ROS 2 Jazzy + Gazebo Harmonic + `ros2_control` + SLAM Toolbox + a custom Nav2 A\* global planner, with a three-layer `ros2_control` architecture and scripted smoke tests.

### Earlier work

- **Snow_point** — the ROS 1 Noetic line of SnowClear: real-time, training-free, CPU-only LiDAR snow detection and removal.
- **Omnidirectional robot competition simulation** — three-wheeled omnidirectional chassis in Gazebo Classic 11 with SLAM, AMCL, `move_base`, DWA, green A4 detection, and an autonomous mission state machine. Validated in simulation; physical deployment still needs drive, odometry, and camera calibration work.

## Other repositories

| Repository | Language |
| --- | --- |
| [Mobile-Manupulator-Simulation-Test](https://github.com/p20030920p/Mobile-Manupulator-Simulation-Test) | Python |
| [Multi-RobotScheduling](https://github.com/p20030920p/Multi-RobotScheduling) | Python |
| [Factor_Simulation](https://github.com/p20030920p/Factor_Simulation) | Python |
| [Multy_Robot](https://github.com/p20030920p/Multy_Robot) | — |
| [RAS_CBS](https://github.com/p20030920p/RAS_CBS) | — |
| [RoboticManipulatorTest](https://github.com/p20030920p/RoboticManipulatorTest) | MATLAB |
| [ITMO-Summer-School-08.2025](https://github.com/p20030920p/ITMO-Summer-School-08.2025) | MATLAB |
| [Choose_wang](https://github.com/p20030920p/Choose_wang) | HTML |

## Working together

Open to collaboration on open-source robotics, point cloud processing, and multi-robot simulation and scheduling. Right now I'm working through point cloud acquisition, filtering, registration and feature extraction, multi-robot scheduling, and connecting large models to robot systems.

---

<h2> 我是 QuanQuan 🤖</h2>
<p><em>机器人技术学习者 —— 自主导航、LiDAR 点云处理与多机器人协同调度。主要用 ROS 2 Jazzy，也做过 ROS 1 Noetic。</em></p>

<div align="left">

<i>联系我：</i><br>

<a href="https://github.com/p20030920p" target="_blank"><img src="https://img.shields.io/badge/GitHub-p20030920p-181717?style=flat-square&logo=github&logoColor=white" alt="GitHub"></a>

</div>

## 项目

### [Sim2Real-AlgoBench](https://github.com/p20030920p/Sim2Real-AlgoBench) —— 三轮全向机器人自主性基准

一个固定任务、一份固定接口契约、一套固定指标，评测两次：仿真一次，实车一次。机器人只收到一次启动信号，在已知地图里自主搜索墙上的绿色 A4 标记，驶入标记前的黄色终点垫并静止 3 秒。全程不手工下发目标点 —— 结束一次运行的是检测结果，而不是几何位置。

- **底盘** —— 三轮全向驱动、URDF/Xacro、LiDAR、相机、`ros2_control`
- **定位** —— SLAM Toolbox 建图、Nav2 Map Saver、在先验栅格地图上做 AMCL 定位
- **规划** —— 从起始位姿的自由空间连通域生成安全搜索视点，再用 Theta\* 做任意角全局规划
- **控制** —— MPPI `Omni` 局部控制，`/cmd_vel` 仲裁保证只有一个发布者
- **世界** —— 标称世界，以及带移动障碍、低附着区、粗糙地面与光照变化的压力世界

*ROS 2 Jazzy · Gazebo Sim 8 · C++17 / Python*

### [FleetFlow](https://github.com/p20030920p/FleetFlow) —— 纺织厂多 AGV 物料搬运仿真

10 台 AGV 在 Gazebo 工厂里于梳棉、拉伸、粗纱机器之间搬运物料桶，由优先级任务调度器分配运输任务，每台车跑独立的 `move_base` 导航栈。控制中心实时显示车队位置、机器状态与各工序完成度；仓库里还带一套批量实验流水线，把运行结果产出成 CSV、分析报告与 LaTeX 表格。

*ROS 1 Noetic · Gazebo 11 · Python 3*

### SnowClear —— 旋转式 LiDAR 的免训练雪点检测与去除

*私有仓库。* 逐点去除降雪噪声，帧率级速度，纯 CPU：不训练、不用 GPU、没有任何学习权重。输入一帧原始点云，输出去雪后的点云与被判为雪点的索引，且索引仍在原始输入点云的坐标系与索引空间中。Release 构建下约 10 ms/帧，逐字节回归可复现。

*ROS 2 Jazzy · C++17 · PCL*

### SLAM —— 建图导航全栈

*私有仓库。* ROS 2 Jazzy + Gazebo Harmonic + `ros2_control` + Slam Toolbox + 自定义 Nav2 A\* 全局规划器，配三层 `ros2_control` 架构与脚本化冒烟测试。

### 早前工作

- **Snow_point** —— SnowClear 的 ROS 1 Noetic 版本：实时、免训练、CPU-only 的 LiDAR 雪点检测与去除。
- **全向机器人竞赛仿真** —— Gazebo Classic 11 中的三轮全向底盘，含激光建图、AMCL、`move_base`、DWA、绿色 A4 识别与自动任务状态机。仿真已验证；装到实车仍需完成底盘驱动、里程计与相机内参标定。

## 合作

欢迎在开源机器人、点云处理、多机器人仿真与调度方向上合作。目前在推进点云采集/滤波/配准/特征提取、多机器人调度，以及大模型与机器人系统的结合。
