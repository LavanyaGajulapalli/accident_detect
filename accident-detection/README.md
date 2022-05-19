# Accident-Detection
[![made-with-python](https://img.shields.io/badge/Made%20with-Python-1f425f.svg)](https://www.python.org/)
[![HitCount](http://hits.dwyl.com/manojpawarsj12/accident-detection.svg)](http://hits.dwyl.com/manojpawarsj12/accident-detection)
[![GitHub license](https://img.shields.io/github/license/Naereen/StrapDown.js.svg)](https://github.com/Naereen/StrapDown.js/blob/master/LICENSE)
[![Codacy Badge](https://api.codacy.com/project/badge/Grade/8e257c8d07a74dba891cfb03cd18d76f)](https://www.codacy.com/manual/manojpawarsj12/accident-detection?utm_source=github.com&amp;utm_medium=referral&amp;utm_content=manojpawarsj12/accident-detection&amp;utm_campaign=Badge_Grade)
![alt text](https://raw.githubusercontent.com/manojpawarsj12/accident-detection/master/htdocs/1.png)
# Overview 
Our main goal of this project is to use deep learning and computer vision to detect accidents on dashcam and report it to nearby emergency services with valid accident images.


# Challenges 
1. Our main challenge was to gather accident images and videos and manually categuorize images into accient and non-accident frames

2. To design a deep convolutional neural networks model for this project.

3. Limited hardware resorces like GPU's.
# Team Members
1: Manoj Pawar Sj [Github](https://github.com/manojpawarsj12) [LinedLn](https://www.linkedin.com/in/manojpawarsj)

2: Manjunath Inti [Github](https://github.com/intimanjunath) [LinedLn](https://www.linkedin.com/in/manjunath-i-7b7bb3190)

3.Bharat Kaushik [Github](https://github.com/bharatkaushik9194) [LinedLn](https://www.linkedin.com/in/bharat-kaushik-562887191)

4.DIkshita Basu [Github](https://github.com/hiyabose) [LinkedLn](https://www.linkedin.com/in/dikshita-basu-a74ab2173)

5.Bikash Singha [Github](https://github.com/bikas17080) [LinkedLn](https://www.linkedin.com/in/bikash-singha-28733518a)

6.Rema Rose Toppo [Github](https://github.com/ReemaRoseToppo) [LinkedLn](https://www.linkedin.com/in/udacitystudentreema-rose-toppo)

# Model Overview
1 . For this project we have tweaked Densenet-161 architecture

Dense Convolutional Network (DenseNet), connects each layer to every other layer in a feed-forward fashion. Whereas traditional convolutional networks with L layers have L connections - one between each layer and its subsequent layer - our network has L(L+1)/2 direct connections. For each layer, the feature-maps of all preceding layers are used as inputs, and its own feature-maps are used as inputs into all subsequent layers. DenseNets have several compelling advantages: they alleviate the vanishing-gradient problem, strengthen feature propagation, encourage feature reuse, and substantially reduce the number of parameters.

The 1-crop error rates on the imagenet dataset with the pretrained model are listed below.

Model structure    Top-1 error    Top-5 error

densenet121  :  25.35   : 7.83

densenet169  :  24.00   : 7.00

densenet201  :  22.80   : 6.43

densenet161  :  22.35   : 6.20

![alt text](https://raw.githubusercontent.com/manojpawarsj12/accident-detection/master/assets/densenet1.png)


# Prerequisite 

Download anaconda from here https://www.anaconda.com/distribution/#download-section

1. Pytorch 

> conda install pytorch torchvision cudatoolkit=10.1 -c pytorch


2. OpenCV 

> conda install -c conda-forge opencv

3. Dataset of accident/non-accident images 

>  https://drive.google.com/open?id=1o0D7vnGUZHS72is6n1jV1ge2BDfObzVi

4. Pretrained Model binary file

>  https://drive.google.com/open?id=1AnJSogx65iyfIG0cSm5D15xfTGJzst8d


5.  A proper php-language environment like xampp,remove htdocs folder and replace that with htdocs in this repo 


6. Clone or Download this repo 

> git clone https://github.com/manojpawarsj12/accident-detection.git

# DEMO

***1.accident***

![alt text](https://raw.githubusercontent.com/manojpawarsj12/accident-detection/master/assets/5.gif)

***2.Non-accident***

![alt text](https://raw.githubusercontent.com/manojpawarsj12/accident-detection/master/assets/6.gif)


# Train 

Go to bash/cmd and type

python train.py

# Tensorboard visual 
**1. Traning set 
![alt text](https://raw.githubusercontent.com/manojpawarsj12/accident-detection/master/assets/4.png)
2. Validation set**
![alt text](https://raw.githubusercontent.com/manojpawarsj12/accident-detection/master/assets/2.png)
**3.Number of corercts v/s epochs**
![alt text](https://raw.githubusercontent.com/manojpawarsj12/accident-detection/master/assets/3.png)
# Test/Accuracy

Go to bash/cmd and type

> python test.py

# Test on video

> python evaluate.py

# Test on Webcam

> python livewebcam.py
# Result

![alt text](https://raw.githubusercontent.com/manojpawarsj12/accident-detection/master/assets/1.png)

The model reaches a classification accuracy of 86.00% accuracy on a randomly sampled test set, composed of 20% of the total amount of video sequences from our dataset. Will re-train this model when we have a good GPU and somre data .
