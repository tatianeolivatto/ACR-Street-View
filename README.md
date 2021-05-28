<h3 align="center">ACR-Street View</h3>


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
