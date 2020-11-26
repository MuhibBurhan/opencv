sudo apt-get -y purge wolfram-engine

sudo apt-get -y purge libreoffice*

sudo apt-get -y clean

sudo apt-get -y autoremove

echo "OpenCV installation by learnOpenCV.com"
cvVersion="masrer"


rm -rf opencv/build
rm -rf opencv_contrib/build

mkdir installation
mkdir installation/OpenCV-"$cvVersion"

cwd=$(pwd)

sudo apt -y update

sudo apt -y upgrade

sudo apt-get -y remove x264 libx264-dev
## Install dependencies
sudo apt-get -y install build-essential checkinstall cmake pkg-config yasm

sudo apt-get -y install git gfortran

sudo apt-get -y install libjpeg8-dev libjasper-dev libpng12-dev

 
sudo apt-get -y install libtiff5-dev

 
sudo apt-get -y install libtiff-dev

sudo apt-get -y install libavcodec-dev libavformat-dev libswscale-dev libdc1394-22-dev

sudo apt-get -y install libxine2-dev libv4l-dev

cd /usr/include/linux

sudo ln -s -f ../libv4l1-videodev.h videodev.h

cd $cwd
sudo apt-get -y install libgstreamer0.10-dev libgstreamer-plugins-base0.10-dev
sudo apt-get -y install libgtk2.0-dev libtbb-dev qt5-default
sudo apt-get -y install libatlas-base-dev
sudo apt-get -y install libmp3lame-dev libtheora-dev
sudo apt-get -y install libvorbis-dev libxvidcore-dev libx264-dev
sudo apt-get -y install libopencore-amrnb-dev libopencore-amrwb-dev
sudo apt-get -y install libavresample-dev
sudo apt-get -y install x264 v4l-utils
# Optional dependencies
sudo apt-get -y install libprotobuf-dev protobuf-compiler
sudo apt-get -y install libgoogle-glog-dev libgflags-dev
sudo apt-get -y install libgphoto2-dev libeigen3-dev libhdf5-dev doxygen

sudo apt-get -y install python3-dev python3-pip

sudo -H pip3 install -U pip numpy

sudo apt-get -y install python3-testresources

cd $cwd
