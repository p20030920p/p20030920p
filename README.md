<h2>QuanQuan 🤖</h2>

Robotics: ROS 2, autonomous navigation, LiDAR point clouds, multi-robot coordination.

## Work

### SnowClear — training-free snow removal for spinning LiDAR

![Snow points removed frame by frame](assets/snowclear-desnow.gif)

Point-wise snow detection and removal for spinning LiDAR. About 10 ms per frame on CPU, no training,
no learned weights.

### [Sim2Real-AlgoBench](https://github.com/p20030920p/Sim2Real-AlgoBench) — three-wheeled omnidirectional autonomy

![Autonomous run: Gazebo on the left, the navigation stack in RViz on the right](assets/sim2real.gif)

One start signal then full autonomy for a three-wheeled omnidirectional robot in ROS 2 Jazzy with
Gazebo: AMCL on a saved map, Nav2 planning and following search viewpoints, green-marker detection
and the finish-pad approach. The clip is Gazebo next to RViz, so both what the robot did and what the
navigation stack planned are visible. Nominal and stress worlds included.

### [FleetFlow-ROS2](https://github.com/p20030920p/FleetFlow-ROS2) — multi-AGV material transport

![Fleet simulation and production board](assets/fleetflow.gif)

Scheduling, traffic control and a live production board for a multi-AGV textile mill, ROS 2 Jazzy
with Gazebo.

### [miku-arm-ros2](https://github.com/p20030920p/miku-arm-ros2) — 6-axis arm control

![Arm demo](assets/miku-arm.gif)

ROS 2 driver and control stack for a 6-axis Damiao-motor arm, with a camera and ArUco-based picking.

<h2>我是 QuanQuan 🤖</h2>

机器人方向：ROS 2、自主导航、LiDAR 点云、多机器人调度。

## 项目

### SnowClear —— 旋转式 LiDAR 免训练去雪

![逐帧剔除雪点](assets/snowclear-desnow.gif)

逐点检测并去除雪点。纯 CPU 约 10 ms/帧，无需训练，无学习权重。

### [Sim2Real-AlgoBench](https://github.com/p20030920p/Sim2Real-AlgoBench) —— 三轮全向机器人自主性

![自主运行：左为 Gazebo，右为 RViz 中的导航栈](assets/sim2real.gif)

一次启动信号后全自主：AMCL 在已有地图上定位、Nav2 规划并跟随搜索视点、识别绿色标志并驶入终点区。
录像左为 Gazebo、右为 RViz，机器人做了什么与导航栈规划了什么同时可见。含标称世界与压力世界。

### [FleetFlow-ROS2](https://github.com/p20030920p/FleetFlow-ROS2) —— 多 AGV 物料搬运

![车队仿真与生产看板](assets/fleetflow.gif)

纺织厂多 AGV 的调度、交通管制与实时生产看板，ROS 2 Jazzy + Gazebo。

### [miku-arm-ros2](https://github.com/p20030920p/miku-arm-ros2) —— 六轴机械臂控制

![机械臂演示](assets/miku-arm.gif)

六轴达妙电机机械臂的 ROS 2 驱动与控制栈，含相机与 ArUco 抓取。
