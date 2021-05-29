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
      <a href="#usage">Usage</a>
    </li>
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

The dataset is composed by imagens and annotations (in TXT extension), being compatible with YOLO annotations.

If you need annotations in other extension, you can freely convert them using Roboflow (https://roboflow.com/).

### Original Dataset

Initially, a CNN was trained at YOLOv4 Darknet, based on an *original dataset* of 477 labelled panoramas from Google Street View (1664x832 pixels), resulting in *1413* annotations of accessibility curb ramps (splited in 80% for train and 20% for validation). This training resulted in an Avarage Precision of 44.68% (IoU 50%).

This training used batch 64 and 16 subdivisions (the best possible within the limitations of free Google Colab); and pre-trained convolutional weights available at: https://github.com/AlexeyAB/darknet/releases/download/darknet_yolo_v3_optimal/yolov4.conv.137.

Paste this snippet into a notebook from our model library to download and unzip your dataset:
!curl -L "https://app.roboflow.com/ds/5Zc6pHfJ7S?key=XLfRLnustB" > roboflow.zip; unzip roboflow.zip; rm roboflow.zip

The direct link to download your zip file is:
https://app.roboflow.com/ds/5Zc6pHfJ7S?key=XLfRLnustB

### Tiled Dataset

In order to improve the model, the final weights were trained based on a *tiled dataset* of 1095 images (416x416 pixels), totalizing *1413* labbed accessibility curb ramps (splited in 80% for train and 20% for validation). This training resulted in an Avarage Precision of 65.31%.

This training batch 64 and 16 subdivisions (the best possible within the limitations of free Google Colab), and pre-trained convolutional weights available at: https://github.com/AlexeyAB/darknet/releases/download/darknet_yolo_v3_optimal/yolov4.conv.137.

Paste this snippet into a notebook from our model library to download and unzip your dataset:
!curl -L "https://app.roboflow.com/ds/gAqIbVSys4?key=KGKGyhUSMD" > roboflow.zip; unzip roboflow.zip; rm roboflow.zip

The direct link to download your zip file is:
https://app.roboflow.com/ds/gAqIbVSys4?key=KGKGyhUSMD

OBS.: *tiled dataset* was more appropriate as ACRs in Google Street View panoramas canbe considered small objects.

<!-- GETTING STARTED -->
## Usage

This [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1dR1dR0sl7MG6M-kXXT90JChwJQnYci32?usp=sharing) Python Notebook contains all pre-requisites and installation required to run the ACR detector, including best weights for ACR detection. Follow its steps to get accessibility curb ramps detections in Google Street Vire panoramas.

## Download panorama samples

This [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1dR1dR0sl7MG6M-kXXT90JChwJQnYci32?usp=sharing) Python Notebook already contains 3 panoramas for testing detections.
If you want to download your own panoramas, of a specific loacation of interest, you can use this tool [![made-with-python](https://img.shields.io/badge/Made%20with-Python-1f425f.svg)](https://github.com/robolyst/streetview).


