# ROS2-Turtlesim

A beginner-friendly project for installing and running the **turtlesim** simulation in ROS2 Humble on **Ubuntu 22.04** and using Vuirtual Machine.

---

## 🎯 Project Goal
Learn how to:
- Set up ROS2 Humble on a virtual machine (Ubuntu 22.04).
- Understand and control nodes in a ROS2 system.
- Publish velocity commands to move the turtle.
- Use services to teleport, reset, or clear the environment.
- Work in a real terminal-based robotics environment.

---

## 🧱 What We Did
We created a virtualized ROS2 environment using **VirtualBox** and **Ubuntu 22.04**, then:
- Installed ROS2 Humble with all dependencies.
- Ran the **turtlesim_node** to launch the turtle GUI.
- Used terminal commands to:
  - Move the turtle with velocity topics.
  - Teleport it using services.
  - Listen to its pose via topics.
  - Control it manually with the keyboard.

---

## 🛠️ Tools & Technologies
- 🐢 ROS2 Humble
- 💻 Ubuntu 22.04 (via VirtualBox)
- 🔑 Terminal CLI
- 🧠 ROS2 Core Concepts: Topics, Nodes, Services

---

## 🚦 How It Works

### 1. Launch the turtle simulator
```bash
ros2 run turtlesim turtlesim_node
```

### 2. Control the turtle with the keyboard
```bash
ros2 run turtlesim turtle_teleop_key
```

### 3. View active topics
```bash
ros2 topic list
```

### 4. Echo the turtle’s pose
```bash
ros2 topic echo /turtle1/pose
```

### 5. Send a velocity command
```bash
ros2 topic pub /turtle1/cmd_vel geometry_msgs/msg/Twist "{linear: {x: 2.0}, angular: {z: 1.5}}"
```

### 6. Call the teleport service
```bash
ros2 service call /turtle1/teleport_absolute turtlesim/srv/TeleportAbsolute "{x: 4.0, y: 2.0, theta: 1.0}"
```

---

## 💡 Tips
- You must source ROS2 in each new terminal:
```bash
source /opt/ros/humble/setup.bash
```

- To reset the simulator:
```bash
ros2 service call /clear std_srvs/srv/Empty
```

---

## 🚀 Setup Guide
1. Install **VirtualBox** & **Ubuntu 22.04**.
2. Inside Ubuntu, install ROS2:
```bash
sudo apt update && sudo apt install curl gnupg2 lsb-release
```
3. Follow the official ROS2 Humble installation steps:  
   🔗 [ROS2 Humble Installation Guide](https://docs.ros.org/en/humble/Installation/Ubuntu-Install-Debs.html)
4. Run **turtlesim** as shown above.

---

## 📸 Project Preview


https://github.com/user-attachments/assets/342ed430-505b-43d9-ab67-aeba3708df67


---

## 👤 Author
**Ahmed Jamjoom**  
📅 *1 Aug 2025*
