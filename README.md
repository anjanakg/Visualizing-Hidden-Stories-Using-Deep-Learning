# Visualizing-Hidden-Stories-Using-Deep-Learning

## Introduction
<p align="justify">The purpose of this project is to make a mobile application that can detect the statue and play an embedded video in seconds on the screen with no         hassle, by just pointing the camera at it. This app makes it easy to learn the history behind the statues without any extra effort.
</p>

<p align="center">
  <img src="https://github.com/anjanakg/Visualizing-Hidden-Stories-Using-Deep-Learning/blob/main/images/Picture1.png" width="350" title="Final output">
</p>

## Project Implimentation
<p align="justify"> To achieve our goal first, we created a Machine Learning(ML) image classification model and converted it to Open Neural Network Exchange(ONNX) file       format. Then we simulated and tested the model in Unity with the Barracuda inference engine. Finally, we deployed our model to an iOS device. 
</p>

<p align="center">
  <img src="https://github.com/anjanakg/Visualizing-Hidden-Stories-Using-Deep-Learning/blob/main/images/Picture2.jpg" width="1200" >
</p>

## Source of Data
<p align="justify"> Out data set comprises images from 24 sculptures all around the University of Dayton main Campus.The raw images were varying in size and some images    were not in the same format as others.  So, we did necessary preprocessing on the raw images before we feed them to the deep learning model. We reduced the size of      the images, turned all the images in the same (jpg) image format, renamed them according to the class they belong to, and added new images manually, to improve the      quality of the dataset.
</p>



