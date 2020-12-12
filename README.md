<div align="center">
  <img src="images/SoDV.png">
</div>

# Social Distance Violation Detection (SoDV) using pre-trained YOLOv3 model ![SoDV](https://img.shields.io/badge/Build-v1.1-BLUE)

The initial idea of this project is to use MobileNet SSD with Caffe implementation as the person detection algorithm. [![FYP](https://img.shields.io/badge/Build-v1.0_pass-BRIGHTGREEN)](https://github.com/afiqharith/Social-Distancing-and-Safety-Violation-Alert-ROI-MobileNetSSD-FYP) In November 2020, I decided to further improve the detection algorithm by using YOLOv3 to increase the accuracy.
</br>

Detect the social distance violations in real time using OpenCV and deep learning

> ## ***"Social distancing is the only way to counter Covid-19"***

**Requirements**
- Python
- Numpy
- OpenCV
- Scipy
- Object Detection models (Mobilenet or Googlenet or YOLO)

***Steps***
1. Input the video stream using OpenCV
2. Detect the people in the video stream using any of the object detection models
3. Find the centroids of the identified people and calculate the distance between the centroids
4. Check if the distance calculated above is lesser than the minimum value (in pixels) and consider it as violation
5. Draw the bounding boxes in red color around the person if violating, green color box if the person is following the norms


_💻 Install the dependencies on command line:_

```sh
$ pip3 install -r requirement.txt
```

_💻 To run the program on command line:_

```sh
$ python3 social-distance-yolo.py
```

</br>

### 🎬 Output example:

| ![outputimage](/images/TownCentre_new.gif) |
| ------------------------------------------ |


**Frame 10 to 500:**

| ![outputimage](/images/data/frame%2010.jpg) | ![outputimage](/images/data/frame%20100.jpg) | ![outputimage](/images/data/frame%20200.jpg) |
| :-----------------------------------------: | :------------------------------------------: | :------------------------------------------: |
|                **FRAME 10**                 |                **FRAME 100**                 |                **FRAME 200**                 |

| ![outputimage](/images/data/frame%20300.jpg) | ![outputimage](/images/data/frame%20400.jpg) | ![outputimage](/images/data/frame%20500.jpg) |
| :------------------------------------------: | :------------------------------------------: | :------------------------------------------: |
|                **FRAME 300**                 |                **FRAME 400**                 |                **FRAME 500**                 |

### 🎯 Accuracy for person detection:

| Dataset            | TP  | TN  | FP  | FN  | %    |
| ------------------ | --- | --- | --- | --- | ---- |
| Oxford Town Centre | 29  | 0   | 0   | 11  | 72.5 |

### 🎯 Accuracy for social distance violation detection:

| Dataset            | TP  | TN  | FP  | FN  | %   |
| ------------------ | --- | --- | --- | --- | --- |
| Oxford Town Centre | NA  | NA  | NA  | NA  | NA  |

### ⛔ Social distance violation detection using distance formula Drawback:

- No camera calibration for intrinsic parameter

### ⏳ Future upgrades:

| Features                                              | Status                                                                |
| ----------------------------------------------------- | --------------------------------------------------------------------- |
| Camera calibration for intrinsic parameter (distance) | ![STATUS](https://img.shields.io/badge/camera_calibration-TBD-orange) |
| Add facemask detection                                | ![STATUS](https://img.shields.io/badge/facemask_detection-TBD-orange) |

---

## Kindly check out below links:

**👀 YOLO Pre-Trained Model** </br>
[![YOLO](https://img.shields.io/badge/YOLO-Darknet-YELLOW)](https://pjreddie.com/darknet/yolo/) [![Darknet](https://img.shields.io/badge/Darknet-GitHub-lightgrey)](https://github.com/pjreddie/darknet.git)

**📊 Dataset** </br>
MegaPixels: Origins, Ethics, and Privacy Implications of Publicly Available Face Recognition Image Datasets </br>
[![Oxford TownCentre](https://img.shields.io/badge/Oxford_Town_Centre-URL-yellowgreen)](https://megapixels.cc/)