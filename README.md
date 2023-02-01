# Obstacle-detection-using-yolo

**YOLO (You Only Look Once)** is a very powerful and a fast algorithm in object detection.

We are going to use YOLO v3, Yolo v4, Yolo v4 tiny models for our coding purpose in this repository. All codes will be written on google colab.

**Step 1: Enabling GPU within your notebook**
You will want to enable GPU acceleration within your Colab notebook so that your YOLOv4 system will be able to process detections over 100 times faster than CPU.

**Step 2: Cloning and Building Darknet**
The following command will clone darknet from AlexeyAB's famous repository, adjust the Makefile to enable OPENCV and GPU for darknet and then build darknet.

''
!git clone https://github.com/AlexeyAB/darknet
''

Do not worry about any warnings when you run the '!make' cell!

change makefile to have GPU and OPENCV enabled and verify the **CUDA** version.

After complete setup for darknet we will move on step3.

**Step 3: Download pretrained weights for yolov3, yolov4,yolov4 tiny models.**

By using following command we can download pretrained weights.

"!wget https://github.com/AlexeyAB/darknet/releases/download/darknet_yolo_v3_optimal/yolov4.weights" - for Yolov4.

"!wget https://pjreddie.com/media/files/yolov3.weights
!chmod a+x ./darknet" -  for Yolov3.

"%cd /content/darknet

!wget https://github.com/AlexeyAB/darknet/releases/download/darknet_yolo_v4_pre/yolov4-tiny.weights

!wget https://github.com/AlexeyAB/darknet/releases/download/darknet_yolo_v4_pre/yolov4-tiny.conv.29"" - for Yolov4 tiny.

**Step 4: Define Helper Functions:**

These three functions are helper functions that will allow you to show the image in your Colab Notebook after running your detections, as well as upload and download images to and from your Cloud VM.

**Step 5: Run Your Detections with Darknet and YOLOv4!**

Darknet is now built and ready to run detections using YOLOv4 in the cloud! You can find out which sorts of classes the pre-trained YOLOv4 weights can detect by clicking here. COCO CLASSES

The object detector can be run using the following command

!./darknet detector test <path to .data file> <path to config> <path to weights> <path to image>

Darknet comes with a few images already installed in the darknet/data/ folder.

Note: After running detections OpenCV can't open the image instantly in the cloud so we must run:

imShow('predictions.jpg')

This will output the image with the detections shown. The most recent detections are always saved to 'predictions.jpg'

**Some Output Prediction**


