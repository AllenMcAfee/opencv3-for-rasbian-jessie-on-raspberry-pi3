# opencv-raspbian Jessie
#opencv for raspbian jessie(pixel) on the raspberry pi3
#i dont take credit for this one, i just forgot where i got it. 
#sinistergenius.com
#Cheers :)

Always good practice to update everything before you install stuff:
sudo apt-get update
sudo apt-get upgrade
sudo rpi-update
We need to install some packages that allow OpenCV to process images:
sudo apt-get install libtiff5-dev libjasper-dev libpng12-dev
If you get an error about libjpeg-dev try installing this first:

sudo apt-get install libjpeg-dev

We need to install some packages that allow OpenCV to process videos:
sudo apt-get install libavcodec-dev libavformat-dev libswscale-dev libv4l-dev

We need to install the GTK library for some GUI stuff like viewing images.
sudo apt-get install libgtk2.0-dev

We need to install some other packages for various operations in OpenCV:
sudo apt-get install libatlas-base-dev gfortran

We need to install pip if you haven't done so in the past:
wget https://bootstrap.pypa.io/get-pip.py
sudo python get-pip.py

Now we can install NumPy - a python library for maths stuff - needed for maths stuff.
sudo pip install numpy

Download and install the file from this repo called "latest-OpenCV.deb".
wget "https://github.com/jabelone/OpenCV-for-Pi/raw/master/latest-OpenCV.deb"
sudo dpkg -i latest-OpenCV.deb

Test it installed correctly by doing the following: Open a python shell
python
Run the following commands, it should return the same version you installed.

import cv2
cv2.__version__
