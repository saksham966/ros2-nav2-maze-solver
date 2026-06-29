# ros2-nav2-maze-solver
# 🤖 ROS 2 Nav2 Maze Solver Bot

An autonomous maze-solving robot built using **ROS 2 Navigation Stack (Nav2)** and **TurtleBot3** in **Gazebo**. The robot autonomously plans and follows collision-free paths to user-defined goals while navigating through a custom maze environment.

![ROS2](https://img.shields.io/badge/ROS2-Humble-blue)
![Nav2](https://img.shields.io/badge/Nav2-Autonomous%20Navigation-success)
![Gazebo](https://img.shields.io/badge/Simulation-Gazebo-orange)
![Ubuntu](https://img.shields.io/badge/Ubuntu-22.04-E95420)
![Python](https://img.shields.io/badge/Python-3.x-yellow)

---

# 📌 Project Overview

This project demonstrates autonomous navigation using the **ROS 2 Navigation Stack (Nav2)**. A TurtleBot3 robot navigates through a **custom maze environment** in Gazebo by planning and executing collision-free paths toward user-defined goals.

The navigation pipeline integrates:

- Global Path Planning
- Local Path Planning
- Costmaps
- Recovery Behaviors
- Localization
- Obstacle Avoidance
- Goal-driven Navigation

The project showcases the complete Nav2 workflow, from environment simulation to autonomous robot navigation.

---

# 🎯 Features

- ✅ Autonomous Maze Navigation
- ✅ Goal-based Navigation
- ✅ Global Path Planning
- ✅ Local Path Planning
- ✅ Obstacle Avoidance
- ✅ Static Costmap
- ✅ Local Costmap
- ✅ Recovery Behaviors
- ✅ TurtleBot3 Simulation
- ✅ Custom Gazebo World
- ✅ RViz Visualization
- ✅ ROS 2 Humble Compatible

---

# 🏗️ System Architecture

```
                 User Goal (RViz)

                       │
                       ▼

              Behavior Tree Navigator

                       │
                       ▼

              Planner Server (Nav2)

                       │
                       ▼

            Global Path Generation

                       │
                       ▼

            Controller Server (Nav2)

                       │
                       ▼

           Velocity Command Generation

                       │
                       ▼

                 TurtleBot3 Robot

                       │
                       ▼

          Gazebo Simulation Environment

                       │
                       ▼

      Costmaps + Obstacle Detection Update

                       │
                       └───────────────┐
                                       │
                                       ▼
                             Path Replanning
```

---

# ⚙️ Navigation Pipeline

```
2D Goal Pose (RViz)
        │
        ▼
Behavior Tree
        │
        ▼
Planner Server
        │
        ▼
Global Planner
        │
        ▼
Path Generation
        │
        ▼
Controller Server
        │
        ▼
Velocity Commands
        │
        ▼
Robot Motion
        │
        ▼
Obstacle Detection
        │
        ▼
Costmap Update
        │
        ▼
Goal Reached
```

---

# 📂 Repository Structure

```
ros2-nav2-maze-solver/

├── launch/
│   ├── maze.launch.py
│   └── navigation.launch.py
│
├── worlds/
│   └── train_maze.sdf
│
├── maps/
│   ├── my_map.yaml
│   └── my_map.pgm
│
├── config/
│   └── nav2_params.yaml
│
├── rviz/
│   └── navigation.rviz
│
├── images/
│   ├── gazebo.png
│   ├── rviz.png
│   ├── architecture.png
│   └── demo.gif
│
├── README.md
├── LICENSE
└── .gitignore
```

---

# 🛠️ Tech Stack

| Technology | Purpose |
|------------|----------|
| ROS 2 Humble | Robotics Framework |
| Nav2 | Autonomous Navigation |
| Gazebo | Robot Simulation |
| RViz2 | Visualization |
| TurtleBot3 | Mobile Robot |
| Python | Launch Files |
| Ubuntu 22.04 | Operating System |

---

# 📋 Prerequisites

- Ubuntu 22.04
- ROS 2 Humble
- TurtleBot3 Packages
- Navigation2 (Nav2)
- Gazebo
- RViz2
- Colcon
- Python 3

---

# 🚀 Installation

Clone the repository

```bash
git clone https://github.com/<YOUR_USERNAME>/ros2-nav2-maze-solver.git

cd ros2-nav2-maze-solver
```

Build the workspace

```bash
colcon build
```

Source the workspace

```bash
source install/setup.bash
```

---

# ▶️ Running the Project

Launch the custom Gazebo world

```bash
ros2 launch my_maze_sim maze.launch.py
```

Launch Navigation2

```bash
ros2 launch turtlebot3_navigation2 navigation2.launch.py \
use_sim_time:=True \
map:=maps/my_map.yaml
```

Open RViz

```bash
rviz2
```

Use the **2D Goal Pose** tool to select a destination inside the maze. The robot will autonomously navigate to the target while avoiding obstacles.

---

# 📊 Results

| Feature | Status |
|----------|--------|
| Autonomous Navigation | ✅ |
| Goal Reached | ✅ |
| Collision Free | ✅ |
| Obstacle Avoidance | ✅ |
| Custom Maze | ✅ |
| Gazebo Simulation | ✅ |

---



# 🧠 Skills Demonstrated

- ROS 2 Development
- Navigation2 (Nav2)
- Autonomous Navigation
- Mobile Robotics
- Path Planning
- Robot Localization
- Costmap Configuration
- Gazebo Simulation
- RViz Visualization
- Linux
- Robotics Software Development

---

# 🔮 Future Improvements

- SLAM-based Autonomous Exploration
- Dynamic Obstacle Avoidance
- Multi-goal Navigation
- Frontier Exploration
- Real Robot Deployment
- Multi-Robot Navigation
- AI-based Path Optimization

---

# 📚 References

- ROS 2 Documentation
- Navigation2 Documentation
- TurtleBot3 Documentation
- Gazebo Documentation

---

# 👨‍💻 Author

**Saksham Badal**

Robotics | ROS 2 | Autonomous Navigation | AI | Computer Vision | Quantum Computing

GitHub: https://github.com/saksham966

---

# ⭐ If you found this project helpful

Give the repository a ⭐ and feel free to fork it!

