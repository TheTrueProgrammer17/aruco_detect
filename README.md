## 🚀 Running the ROS Node

After cloning and building the workspace, you can run the vision node with:

```bash
# Build the workspace
cd ~/aruco_ws
colcon build --packages-select gstream_node
source install/setup.bash

# Run the node
ros2 run gstream_node gstream_node
