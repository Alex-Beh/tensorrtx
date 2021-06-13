
# Yolov5 TensorRT inteference with usb camera
- Adapted the opencv cv::VideoCapture code with usb camera on from [USBCamera](https://github.com/lxuejiao/USBCamera)
- Resolution of the video : 640 x 480

## How to build
```shell
mkdir build
cd build 
cmake ..
make
./usb_camera
```

## Notice
- capture.open("/dev/video1") need to use your own camera device path.
- check usb camera device
    ```shell
    cd /dev
    ls | grep video

    #see video0 detail info
    udevadm info --query=all --name=/dev/video0
    ```