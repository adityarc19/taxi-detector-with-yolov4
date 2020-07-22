# Taxi detector with YOLOv4 and Darknet !

![taxi][logo]

[logo]: https://github.com/adityarc19/taxi-detector-with-yolov4/blob/master/sample_images/taxi.jpg

## This is a taxi detector project that identifies taxis in a given image.

A big shoutout and thanks to @theAIGuysCode who have made an amazing toolkit for labelling images in YOLOv4 format. This project uses their toolkit.
**Code and Resources used:**

https://github.com/theAIGuysCode/YOLOv3-Cloud-Tutorial

https://github.com/theAIGuysCode/OIDv4_ToolKit
 
 
## **Dataset prep**

I've downloaded 200 HD images of taxis from the Open Images Dataset. There is an extensive article that I've put up on Medium regarding steps on how to create your own custom dataset. Not only that, I have also explained in it how to label the dataset in YOLOv4 format. 
Check it out [here](https://medium.com/analytics-vidhya/create-your-own-dataset-for-yolov4-object-detection-in-5-minutes-fdc988231088)!

## **Training**

Training is done using YOLOv4 Darknet on Google Colab. The entire training process is attached [here](https://github.com/adityarc19/taxi-detector-with-yolov4/blob/master/Taxi_detector_using_yolov4.ipynb).

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


