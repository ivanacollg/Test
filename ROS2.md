sudo apt install python3.12-venv
python3 -m venv ~/ros2_venv
source ~/ros2_venv/bin/activate
pip install rclpy dt_apriltags opencv-python numpy scipy matplotlib

source /opt/ros/jazzy/setup.bash

ros2 pkg create my_python_pkg --build-type ament_python --dependencies rclpy std_msgs # Python
ros2 pkg create my_cpp_pkg --build-type ament_cmake --dependencies rclcpp std_msgs # C++

colcon build
