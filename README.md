# Taxi detector with YOLOv4 and Darknet !

![taxi][logo]

[logo]: https://github.com/adityarc19/taxi-detector-with-yolov4/blob/master/sample_images/taxi.jpg

## This is a taxi detector project that identifies taxis in a given image.

A big shoutout and thanks to @theAIGuysCode who have made an amazing toolkit for labelling images in YOLOv4 format. This project uses their toolkit.

**Code and Resources used:**

https://github.com/theAIGuysCode/YOLOv3-Cloud-Tutorial

https://github.com/theAIGuysCode/OIDv4_ToolKit
 
## My intuition behind making this project

I always have wanted an app on my phone wherein I open my camera and pan it out on the streets, and it detects taxis/cabs for me ! I know its a little silly and probably cab services already do have a system of locating the nearest cabs in your area. However, I havent come across a system which could be called a "taxi scanner". I feel like it would be really cool to just be able to pull out the camera on my phone and have it detect taxis around me just like a bar code scanner would scan bar codes. 
This is why I thought of making an object detector that would do the same using the current state of the art object detection technology, i.e., YOLOv4. 
In the future, I hope to turn this project into a mobile app like the way I mentioned above. 

## Initial Setup

Execute the code snippets below to setup the requirements for this task.

```
# clone darknet repo
!git clone https://github.com/AlexeyAB/darknet
```

```

# change makefile to have GPU and OPENCV enabled
%cd darknet
!sed -i 's/OPENCV=0/OPENCV=1/' Makefile
!sed -i 's/GPU=0/GPU=1/' Makefile
!sed -i 's/CUDNN=0/CUDNN=1/' Makefile
!sed -i 's/CUDNN_HALF=0/CUDNN_HALF=1/' Makefile
```

```
# make darknet (builds darknet so that you can then use the darknet executable file to run or train object detectors)
!make
```


## **Dataset prep**

I've downloaded 200 HD images of taxis from the Open Images Dataset. There is an extensive article that I've put up on Medium regarding steps on how to create your own custom dataset. Not only that, I have also explained in it how to label the dataset in YOLOv4 format. 
Check it out [here](https://medium.com/analytics-vidhya/create-your-own-dataset-for-yolov4-object-detection-in-5-minutes-fdc988231088)!

## **Training**

Before starting the training process, download the pre-trained weights from:

```
https://github.com/AlexeyAB/darknet/releases/download/darknet_yolo_v3_optimal/yolov4.conv.137
```

Training is done using YOLOv4 Darknet on Google Colab. There are a lot of files that you need for training. All those files are attached [here](https://github.com/adityarc19/taxi-detector-with-yolov4/tree/master/yolov4). However, if you want to train on your own custom dataset, you need to make a lot of changes to these files. All of it explained in the actual .pynb file [here](https://github.com/adityarc19/taxi-detector-with-yolov4/blob/master/Taxi_detector_using_yolov4.ipynb). 

![gif][code]

[code]: https://github.com/adityarc19/taxi-detector-with-yolov4/blob/master/sample_images/code.gif

## **Output**

After we complete our object detection process, we get a very decent detection system of taxis just by training with the pre-trained weights of YOLOv4.
Some sample output images are:

1.

![ot][oti]

[oti]: https://github.com/adityarc19/taxi-detector-with-yolov4/blob/master/sample_images/Screenshot%202020-07-21%20at%209.22.46%20PM.png

2.

![det][otiy]

[otiy]: https://github.com/adityarc19/taxi-detector-with-yolov4/blob/master/sample_images/Screenshot%202020-07-21%20at%209.23.01%20PM.png

3.

![d][oi]

[oi]: https://github.com/adityarc19/taxi-detector-with-yolov4/blob/master/sample_images/Screenshot%202020-07-21%20at%209.23.14%20PM.png


