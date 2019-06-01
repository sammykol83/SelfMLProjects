# Pedestrian counter project

The purpose of the project is to analyze an offline surveillance camera video file and count the number of **walking** pedestrians in the video. 

## Table of contents
- [Motivation](#motivation)
- [Requirements](#requirements)
- [Architecture of solution](#architecture-of-solution)
- [Quick start](#quick-start)
- [Summary of results](#results)

## Motivation <a name="motivation"></a>
Pedestrian counting has many applications (For example, A tool for urban planning). So, the motivation is demonstrate a method to perform this task. 

## Requirements <a name="requirements"></a>
I developed the project on:
* OS: **WINDOWS 10**
* Python ver: **3.7.1** 
* Numpy: **1.16.2**
* Pandas: **0.23.4**
* OpenCV: **4.1.0**
(NOTICE: OpenCV installation might be a bit tricky...)

## Architecture of solution <a name="architecture-of-solution"></a>
The solution is based on a YOLO (You Only Look Once) CNN. 
1. We pass the input video file through the YOLO CNN. The output
is a modified video file containing all of the detected objects and an additional log file. 

2. We then run a Jupyter notebook which analyzes the log files, deduces the count of pedestrians per frame, and then displays the YOLO CNN output video with a counter of pedestrians overlayed on the video.

The [**YOLO**](https://pjreddie.com/darknet/yolo/) implementation itself was performed using the framework [**"darknet"**](https://pjreddie.com/darknet/). This project can be downloaded and compiled from [**AlexeyAB/darknet GitHub repository**](https://github.com/AlexeyAB/darknet).

## Quick start <a name="quick-start"></a>
1. Open the *.ipnyb Jupyter notbebook and follow the instructions inside. 
2. In case you want to run the YOLO detector using the supplied compiled binary, you'll need:
      * An X64 Windows environment. 
      * Download the [**weights (237Mbyte)**](https://pjreddie.com/media/files/yolov3.weights).      

## Summary of results <a name="results"></a>
A metric of "RMSE per second" was defined, with a score of 0.55. 
This means that per second, the system (on average) missed by 0.5 person in the people count. 

There were 2 "major" error event in the recording, explained in more detail in the IPython notebook. 



 
