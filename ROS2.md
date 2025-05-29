ros2 pkg create my_python_pkg --build-type ament_python --dependencies rclpy std_msgs # Python
ros2 pkg create my_cpp_pkg --build-type ament_cmake --dependencies rclcpp std_msgs # C++

colcon build
