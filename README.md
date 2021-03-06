# AI-Challenge-2020
=======
## Artificial intelligence application solutions in Ho Chi Minh City 2020

### 1. Introduction

In this competition, the competition team will count the number of vehicles in each type of vehicle moving in different directions in the video recorded from a traffic camera in Ho Chi Minh City.

This problem serves to analyze vehicle traffic on roads, thereby supporting the proposal and design of solutions to reduce traffic congestion.

<img src="vd1.png">

The image illustrates a video from a traffic camera with the MOI (Motion of Interest) moving directions of the vehicle and the ROI (Region of Interest) counting area.

Source: [AI Challenge](http://aichallenge.hochiminhcity.gov.vn/huong-dan-nhom-1)

### 2.Member team

| Name | Github |
| ------ | ------ |
| Nguyen Huu Doanh | [Github](https://github.com/huudoanh123qn) |
| Nguyen Minh Châu | [Github](https://github.com/chauminhnguyen) |
| Nguyen Huynh Anh | [Github](https://github.com/anhhuynh1506) |
| To Viet Anh | [Github](https://github.com/anhtv26062000) |

### 3.Method

To resolve above problem, the team divived the problem into 3 modules:

* **Object detection**: Using YOLOv3 to detect object. The result is a list of bouding boxes corresponding to all the means of transport in the image.

* **Multi object tracking**: Based on the IOU (index measuring the overlap of two bounding boxes), the bounding boxes in consecutive frames will be grouped by DeepSort technique and from there will form the moving trajectory of the vehicle itself. 

* **Counting vehicles**: The vehicle's MOI will be selected based on the similarity (here using Cosine Similarity Score) between the trajectories of each vehicle and the MOIs will be calculated by heatmap algorithm.

### 4.Running

Link models:
https://drive.google.com/drive/folders/1-uo8GWvDq9Kah8X0yaWk659bhCZRDEHb?usp=sharing

The models should be in the lath: /save_models

To running, using command cmd:

		bash ./run.sh

### 5.Result

| Rank | Team | Score |
| --- |:--:|:---:|
| 16 |089|5.341649

![Result](https://user-images.githubusercontent.com/52884083/154944407-a4765c91-b2aa-4c67-abcd-f16b1340ee03.jpg)
