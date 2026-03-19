cd ~/aruco_ws
colcon build --packages-select gstream_node
source install/setup.bash
ros2 run gstream_node gstream_node
