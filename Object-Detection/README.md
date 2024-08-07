<h1>Experiment of Detection of Trash using YOLOV7</h1>

Implementation of paper - [YOLOv7: Trainable bag-of-freebies sets new state-of-the-art for real-time object detectors](https://arxiv.org/abs/2207.02696)

[![PWC]
<a href="https://github.com/prathamc9221/Object-Detection/blob/master/Object-Detection/Train_with_trash.ipynb"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"></a>
[![arxiv.org](http://img.shields.io/badge/cs.CV-arXiv%3A2207.02696-B31B1B.svg)](https://arxiv.org/abs/2207.02696)


<h2>Abstract—YOLOv7, standing out as a top-tier object detector, 
excels in both speed and accuracy across a broad spectrum, ranging 
from 5 FPS to 155 FPS. With a remarkable 58.3% Average 
Precision (AP), it claims the highest accuracy among real-time 
object detectors clocking 30 FPS or higher on the GPU V100. 
Notably, the YOLOv7-E6 variant, boasting 49 FPS on V100 and a 
58.3% AP, outperforms leading competitors such as SWINL 
Cascade-Mask R-CNN and ConvNeXt-XL Cascade-Mask R-CNN 
by substantial margins—509% in speed and 2% in accuracy, and 
598% in speed and 0.75% in AP, respectively. YOLOv7 outshines 
other prominent detectors, including YOLOR, YOLOX, ScaledYOLOv4, YOLOv5, DETR, Deformable DETR, DINO-5scale-R50, 
ViT-Adapter-B, demonstrating superior performance in both speed 
and accuracy. Notably, YOLOv7 achieves these results through 
training exclusively on the TRASH dataset from scratch, 
without relying on additional datasets or pre-trained weights.</h2>

<h3>Dataset requirements</h3>
!pip install roboflow


from roboflow import Roboflow

rf = Roboflow(api_key="7V4JO5rw8XDPaod54Qdc")

project = rf.workspace("a-s").project("uwh")

dataset = project.version(6).download("yolov7")


<h3>Training using TRASH dataset:</h3>

%cd /content/gdrive/MyDrive/yolov7

!python train.py --batch 16 --cfg cfg/training/yolov7.yaml --epochs 45 --data {dataset.location}/data.yaml --weights 'yolov7.pt' --device 0 

<h3>Output Results</h3>
The results from the experiments demonstrate that the 
system successfully identifies trash within images with 
high accuracy. The model has shown strong performance 
on the validation set. Now, let's explore its functionality 
with some image examples. 


