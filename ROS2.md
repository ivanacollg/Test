For ROS2 intall
```pip install 'numpy<2'```

```
sudo apt install python3.12-venv
python3 -m venv ~/ros2_venv
source ~/ros2_venv/bin/activate
pip install rclpy dt_apriltags opencv-python numpy scipy matplotlib
```

Add ROS to bash
```
source /opt/ros/jazzy/setup.bash
```

Add ws environment to your virtual environment file add the following line to ```~/ros2_venv/bin/activate```
```
source /opt/ros/jazzy/setup.bash
source /home/ivana/code/aqua_ws/install/setup.bash
```

Create pkg and build
```
ros2 pkg create my_python_pkg --build-type ament_python --dependencies rclpy std_msgs # Python
ros2 pkg create my_cpp_pkg --build-type ament_cmake --dependencies rclcpp std_msgs # C++

colcon build

source install/setup.bash
```
