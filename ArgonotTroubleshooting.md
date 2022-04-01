# Troubleshooting  Argonot
- CMake Error at /opt/ros/melodic/share/cv_bridge/cmake/cv_bridgeConfig.cmake:113 (message):
  Project 'cv_bridge' specifies '/usr/include/opencv' as an include dir,
  which is not found.  It does neither exist as an absolute directory nor in
  '${{prefix}}//usr/include/opencv'.

change the file:

/opt/ros/melodic/share/cv_bridge/cmake/cv_bridgeConfig.cmake
change this line:

set(_include_dirs "include;/usr/include;/usr/include/opencv")
to

set(_include_dirs "include;/usr/include;/usr/include/opencv4"

- /home/rov2/rov_ws/src/Argonaut/sonar_oculus/src/sonar.cpp:24:10: fatal error: cv.h: No such file or directory
 #include <cv.h>
change for #include <opencv2/opencv.hpp>

- highgui.h: No such file or directory #include <highgui.h>
change for #include "opencv2/highgui/highgui.hpp"

- ‘CV_IMWRITE_JPEG_QUALITY’ was not declared in this scope
  params[0] = CV_IMWRITE_JPEG_QUALITY;
change for cv::IMWRITE_JPEG_QUALITY

# BRUCE INSTALL
https://github.com/borglab/gtsam
