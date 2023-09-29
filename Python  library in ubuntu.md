# 📷 OpenCV Installation Guide 📷

**Source**: [How to install OpenCV for Python on Ubuntu 22.04, 20.04 or others](https://linux.how2shout.com/how-to-install-opencv-for-python-on-ubuntu-22-04-20-04-or-others/)

## Step 1: Update Ubuntu Packages

```bash
sudo apt update
sudo apt upgrade
```

## Step 2: Install Required Dependencies

```bash
sudo apt install python3-dev python3-pip python3-numpy build-essential libgtk-3-dev libavcodec-dev libavformat-dev libswscale-dev libv4l-dev libxvidcore-dev libx264-dev libjpeg-dev libpng-dev libtiff-dev gfortran openexr libatlas-base-dev
```

## Step 3: Install OpenCV for Python on Ubuntu 

```bash
pip3 install opencv-python
```

## Step 4: Verify the Installation

```bash
python3
```

- Check OpenCV version.
  
```python
import cv2
print(cv2.__version__)
```

## Step 5: Install Extra OpenCV Packages (Optional)

```bash
pip3 install opencv-contrib-python
```
