Experiment of Detection of Trash using YOLOV7

Implementation of paper - [YOLOv7: Trainable bag-of-freebies sets new state-of-the-art for real-time object detectors](https://arxiv.org/abs/2207.02696)

[![PWC]
<a href="https://github.com/prathamc9221/Object-Detection/blob/master/Object-Detection/Train_with_trash.ipynb"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"></a>
[![arxiv.org](http://img.shields.io/badge/cs.CV-arXiv%3A2207.02696-B31B1B.svg)](https://arxiv.org/abs/2207.02696)


Training using TRASH dataset
%cd /content/gdrive/MyDrive/yolov7
!python train.py --batch 16 --cfg cfg/training/yolov7.yaml --epochs 45 --data {dataset.location}/data.yaml --weights 'yolov7.pt' --device 0 
