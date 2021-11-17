# Install Ubuntu
Creat ubuntu image on flashdrive and start up using that USB drive

# Install gcc 
sudo apt update
sudo apt install build-essential
gcc --version
sudo apt install cmake

# Install Nvidia drivers
Download drivers from Nvidia wesite using computer specs
sudo sh NVIDIA....run

# Install CUDA 
nvidia-smi

# Install CuDNN
nvcc -V

# Install Git
sudo apt install git
git --version
git config --global user.email "youremail@yourdomain.com"
git config --global user.email "youremail@yourdomain.com"
git config --list

# Install Python
sudo apt-get -y install python3-dev python3-pip 
pip3 --version
sudo apt install python-pip
pip --version
sudo pip install numpy scipy matplotlib scikit-image scikit-learn ipython

# Install OpenCV
sudo apt-get -y install libjpeg8-dev libjasper1 libpng-dev
sudo apt-get -y install libtiff-dev
sudo apt-get -y install libavcodec-dev libavformat-dev libswscale-dev libdc1394-22-dev
sudo apt-get -y install libxine2-dev libv4l-dev
sudo apt -y install libgstreamer1.0-dev libgstreamer-plugins-base1.0-dev
sudo apt-get -y install qt5-default libgtk2.0-dev libtbb-dev
sudo apt-get -y install libatlas-base-dev
sudo apt-get -y install libfaac-dev libmp3lame-dev libtheora-dev
sudo apt-get -y install libvorbis-dev libxvidcore-dev
sudo apt-get -y install libopencore-amrnb-dev libopencore-amrwb-dev
sudo apt-get -y install x264 v4l-utils
sudo apt-get -y install libprotobuf-dev protobuf-compiler
sudo apt-get -y install libgoogle-glog-dev libgflags-dev
sudo apt-get -y install libgphoto2-dev libeigen3-dev libhdf5-dev doxygen

git clone https://github.com/opencv/opencv.git
	cd opencv 
	git checkout 4.0.0 
	cd ..

	git clone https://github.com/opencv/opencv_contrib.git
	cd opencv_contrib
	git checkout 4.0.0
	cd ..

	cd opencv
	mkdir build
	cd build

# If needed 
	#  sudo update-alternatives --install /usr/bin/gcc gcc /usr/bin/g++-6 6
	#  sudo update-alternatives --install /usr/bin/gcc gcc /usr/bin/gcc-6 6

	# Last tested on 30/12/19
	cmake -D CMAKE_BUILD_TYPE=RELEASE \
	      -D CMAKE_INSTALL_PREFIX=/usr/local \
	      -D ENABLE_PRECOMPILED_HEADERS=OFF \
	      -D INSTALL_C_EXAMPLES=ON \
	      -D INSTALL_PYTHON_EXAMPLES=ON \
	      -D WITH_TBB=ON \
	      -D WITH_V4L=ON \
	      -D OPENCV_PYTHON3_INSTALL_PATH=/usr/lib/python3.6/ \
	      -D WITH_QT=ON \
	      -D WITH_OPENGL=ON \
	      -D OPENCV_EXTRA_MODULES_PATH=../../opencv_contrib/modules \
	      -D BUILD_EXAMPLES=ON \
	      -D WITH_CUDA=ON \
	      -D WITH_CUBLAS=ON \
	      -D CUDA_GENERATION=Auto \
	      -D CUDA_NVCC_FLAGS="-D_FORCE_INLINES" \
	      -D ENABLE_FAST_MATH=1 \
	      -D CUDA_FAST_MATH=1 \
	      -D WITH_NVCUVID=1 \
	      -D WITH_CUFFT=ON \
	      -D WITH_EIGEN=ON \
	      -D WITH_IPP=ON \
	      -D BUILD_opencv_cudacodec=OFF \
	      -D CMAKE_C_COMPILER=gcc-6 \
	      -D CMAKE_CXX_COMPILER=g++-6 \
	      -D OPENCV_GENERATE_PKGCONFIG=ON ..

	make -j($nproc)
	sudo make install 
	sudo ldconfig


# Install VSCode

# Install OpenCV

# Intsall Sportify



