
---

## 🚀 Quick Start 

```bash
# 1. Create a ROS2 workspace
mkdir -p ~/aruco_ws/src
cd ~/aruco_ws/src

# 2. Clone this repository
git clone https://github.com/TheTrueProgrammer17/aruco_detect.git

# 3. Install dependencies
pip install opencv-contrib-python==4.8.1.78 numpy==1.26.4
sudo apt install ros-humble-cv-bridge ros-humble-rqt-image-view

# 4. Build the workspace
cd ~/aruco_ws
colcon build --packages-select gstream_node

# 5. Source the setup file
source install/setup.bash

# 6. Run the node
ros2 run gstream_node gstream_node

aruco_detect/
 └── gstream_node/                ← package root
      ├── package.xml             ← ROS package manifest
      ├── setup.py                ← Python build/install config
      ├── setup.cfg               ← colcon/ament config
      └── gstream_node/           ← Python module
           ├── __init__.py
           └── gstream_process.py ← your ROS-integrated node
