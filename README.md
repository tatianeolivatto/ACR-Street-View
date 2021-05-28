<h1 align="center">ACR-Street View</h1>

<!-- TABLE OF CONTENTS -->
<details open="open">
  <summary>Table of Contents</summary>
  <ol>
    <li><a href="#about-the-project">About The Project</a></li>
    <li>
      <a href="#Image-Datasets-used-for-training">Image Datasets used for training</a>
      <ul>
        <li><a href="#Original-Dataset">Original Dataset</a></li>
        <li><a href="#Tiled-Dataset">Tiled Dataset</a></li>
      </ul>
    </li>
    <li>
      <a href="#getting-started">Getting Started</a>
      <ul>
        <li><a href="#prerequisites">Prerequisites</a></li>
        <li><a href="#installation">Installation</a></li>
      </ul>
    </li>
    <li><a href="#usage">Usage</a></li>
    <li><a href="#roadmap">Roadmap</a></li>
    <li><a href="#contributing">Contributing</a></li>
    <li><a href="#license">License</a></li>
    <li><a href="#contact">Contact</a></li>
    <li><a href="#acknowledgements">Acknowledgements</a></li>
  </ol>
</details>

<!-- ABOUT THE PROJECT -->
## About The Project

This project was developed aiming to provide an object detector for ACRs (accessibility cyrb ramps) located in sidewalks covering Brazilian Cities (specifically São Paulo State).

## Image Datasets used for training

### Original Dataset

Initially, a CNN was trained at YOLOv4 Darknet, based on an *original dataset* of 477 labelled panoramas from Google Street View (1664x832 pixels), resulting in *1413* annotations of accessibility curb ramps (splited in 80% for train and 20% for validation). This training resulted in an Avarage Precision of 44.68% (IoU 50%).

This training used batch 64 and 16 subdivisions (the best possible within the limitations of free Google Colab); and pre-trained convolutional weights available at: <https://github.com/AlexeyAB/darknet/releases/download/darknet_yolo_v3_optimal/yolov4.conv.137.

Paste this snippet into a notebook from our model library to download and unzip your dataset:
!curl -L "https://app.roboflow.com/ds/5Zc6pHfJ7S?key=XLfRLnustB" > roboflow.zip; unzip roboflow.zip; rm roboflow.zip

The direct link to download your zip file is:
https://app.roboflow.com/ds/5Zc6pHfJ7S?key=XLfRLnustB

### Tiled Dataset

In order to improve the model, the final weights were trained based on a *tiled dataset* of 1095 images (416x416 pixels), totalizing *1413* labbed accessibility curb ramps (splited in 80% for train and 20% for validation). This training resulted in an Avarage Precision of 65.31%.

This training batch 64 and 16 subdivisions (the best possible within the limitations of free Google Colab), and pre-trained convolutional weights available at: <https://github.com/AlexeyAB/darknet/releases/download/darknet_yolo_v3_optimal/yolov4.conv.137.

Paste this snippet into a notebook from our model library to download and unzip your dataset:
!curl -L "https://app.roboflow.com/ds/gAqIbVSys4?key=KGKGyhUSMD" > roboflow.zip; unzip roboflow.zip; rm roboflow.zip

The direct link to download your zip file is:
https://app.roboflow.com/ds/gAqIbVSys4?key=KGKGyhUSMD








The code available refers to an ACR (accessible curb ramps) detector developed in YOLOv4 Darknet.

1. Dataset used for training refers to Tiled Google Street View panoramas, available for download at:

https://app.roboflow.com/ds/gAqIbVSys4?key=KGKGyhUSMD

Or to download and unzip into a notebook paste this snippet:

!curl -L "https://app.roboflow.com/ds/gAqIbVSys4?key=KGKGyhUSMD" > roboflow.zip; unzip roboflow.zip; rm roboflow.zip


2. But original dataset is available for download at:

https://app.roboflow.com/ds/5Zc6pHfJ7S?key=XLfRLnustB

Or to download and unzip into a notebook paste this snippet:

!curl -L "https://app.roboflow.com/ds/5Zc6pHfJ7S?key=XLfRLnustB" > roboflow.zip; unzip roboflow.zip; rm roboflow.zip


# obs.:
Tiled images resulted in an 
This image dataset contains 477 labelled panoramas from Google Street View covering Brazilian Cities (specifically São Paulo State). Altogheter, there are 1413 annotations of accessibility curb ramps divided in two folders: "obj" (80% of images in train folder) and "test" (20% of images in validation folder).

Annotations are in TXT extension, being compatible with YOLO annotations. If you need annotations in other extension, you can freely convert them using Roboflow (https://roboflow.com/).
