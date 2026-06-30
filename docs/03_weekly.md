# Week 3 — 2026.6.30

**Attended this week's meeting:** Yes

**Progress this week**

- run the demo case for the carter
- solve the carter_mini_base problem
- learn the diff_drive_control
- /clock 仿真时钟正常输出
- /odom 50Hz 里程计连续更新、坐标系正确
- /scan 10Hz 激光时序对齐仿真时间
- TF 树 map→odom→carter_mini_base→lidar_link 完整

**Challenges & blockers**

- 唯一剩余根源：slam_toolbox 插值模式机制缺陷
- do_interpolate: true 模式下，SLAM 每次收到激光，都要拿激光时间戳去 TF 缓存插值查询 odom 变换；
- 即便时序完全对齐，激光与 TF 的时间戳仍存在微小错位，偶尔找不到前后成对变换，持续打印警告

**Next steps**
  
- figure out the computational graph and examine the clock problem

**Hours spent (optional):** 5d (5h per day)

**Links (optional):** Null
