# Visualizing Hidden Stories Using Deep Learning

## Introduction
<p align="justify">The purpose of this project is to make a mobile application that can detect the statue and play an embedded video in seconds on the screen with no         hassle, by just pointing the camera at it. This app makes it easy to learn the history behind the statues without any extra effort.
</p>

<p align="center">
  <img src="https://github.com/anjanakg/Visualizing-Hidden-Stories-Using-Deep-Learning/blob/main/images/Picture1.png" width="350" title="Final output">
</p>

<br>

## Source of Data
<p align="justify"> Out data set comprises images from 24 sculptures all around the University of Dayton main Campus.The raw images were varying in size and some images    were not in the same format as others.  So, we did necessary preprocessing on the raw images before we feed them to the deep learning model. We reduced the size of      the images, turned all the images in the same (jpg) image format, renamed them according to the class they belong to, and added new images manually, to improve the      quality of the dataset.
</p>
<br>
<p align="center">
  <img src="https://github.com/anjanakg/Visualizing-Hidden-Stories-Using-Deep-Learning/blob/main/images/Picture3.jpg" width="1200" >
</p>

<br>
<p align="justify"> Our input is an image dataset that comprises 6820 images belonging to 24 classes. We split our dataset into training, validation sets in 70% train,   30% validation. We kept a separate dataset for testing the model that comprises 480 images, 20 images from each sculpture. 
</p>
<br>
<p align="center">
  <img src="https://github.com/anjanakg/Visualizing-Hidden-Stories-Using-Deep-Learning/blob/main/images/Picture4.png" width="1200" >
</p>

<br>

## Project Implimentation
<p align="justify"> To achieve our goal first, we created a Machine Learning(ML) image classification model and converted it to Open Neural Network Exchange(ONNX) file       format. Then we simulated and tested the model in Unity with the Barracuda inference engine. Finally, we deployed our model to an iOS device. 
</p>


<p align="justify"> Then we convert to ONNX Format. ONNX(Open Neural Network Exchange) is an intermediate machine learning framework used to convert between different    machine learning frameworks.
 </p>

<p align="justify"> After that, we loaded the model and other necessary files to Unity Barracuda. Unity Barracuda is a lightweight and cross-platform Neural Net          inference library for Unity. Barracuda can run Neural Nets both on GPU and CPU. We created an inference engine, executed the model, and fetched the results.
</p>

<p align="justify"> Finally, we deploy the model to the iPhone using Xcode IDE.
</p>

<p align="center">
  <img src="https://github.com/anjanakg/Visualizing-Hidden-Stories-Using-Deep-Learning/blob/main/images/Picture2.jpg" width="1200" >
</p>

<br>

## Model Training and Evaluation
<p align="justify"> We used the TensorFlow(TF) platform for creating our Deep Learning model. We trained our dataset on Colab notebooks as well as on Jupiter               notebooks. Colab notebooks include GPUs and it helped us to train our dataset much easier and faster than our personal computer.
</p>

<p align="justify"> 
    We tried several pre-trained models to select the best model. 
    We trained each model on the training set and evaluated each trained model’s performance on the validation set. And finally, choose the model with the best             validation set performance for testing on test data set.
</p>

<p align="justify"> 
    We faced lots of pitfalls during our process. The ResNet50 with Transfer Learning model performed very well in our data. However, we could not convert it to tflite     format. We converted it to ONNX format with ONNX opset version 11. But the file size was 150MB and also Unity was not supporting it.  
</p>

  The complete notebook of ResNet50 model implementation, training, and evaluation is
  [here](Classification_of_UDSculptures_ResNet50.ipynb) 
  .
<p align="justify"> 
    Since we were looking for ways to optimize models for deployment on a mobile device, we should have to focus on lightweight models. After overcoming various           pitfalls and performance issues, we were successful on the model EfficientNet-Lite4 on TensorFlow hub.  
</p>

  
  The complete notebook of EfficientNet-Lite4 model implementation, training, and evaluation is
  [here](UDsculptures_Classification_ENL4Final1.ipynb) 
  . 
 <p align="justify">  
  The training accuracy and validation accuracy of our model after training our dataset for 20 epochs were 95% and 94% respectively. The overall testing accuracy for     the test dataset was 88%. 
</p>

## Model Testing and Predictions

<p align="center">
  <img src="https://github.com/anjanakg/Visualizing-Hidden-Stories-Using-Deep-Learning/blob/main/images/Picture5.png" width="1200" >
</p>

<br>

<p align="center">
  <img src="https://github.com/anjanakg/Visualizing-Hidden-Stories-Using-Deep-Learning/blob/main/images/Picture6.png" width="1200" >
</p>

<br>

## Convert the Final Model to ONNX Format

<p align="center">
  <img src="https://github.com/anjanakg/Visualizing-Hidden-Stories-Using-Deep-Learning/blob/main/images/Picture8.png" width="1200" >
</p>

<br>

## Simulation on Unity

<p align="center">
  <img src="https://github.com/anjanakg/Visualizing-Hidden-Stories-Using-Deep-Learning/blob/main/images/Picture9.png" width="1200" >
</p>

<br>

## The app functioning on iphone

[![mqdefault](https://user-images.githubusercontent.com/86033987/211634286-f09ffa05-d8e9-49ff-8ea7-da1676dc20b3.jpg)](https://youtu.be/g9io2tu86XI)

## The mobile app can predict most of the UD sculptures with high accuracy

[![mqdefault](https://user-images.githubusercontent.com/86033987/211636999-d22eac4f-8c88-4a56-8f71-921e5f34a04e.jpg)](https://youtu.be/_grlndUxJ8o) [![mqdefault](https://user-images.githubusercontent.com/86033987/211637337-cac0f33b-a469-4722-a465-011605bf88fa.jpg)](https://youtu.be/prUB2lwtQNg)

<br>

**This is the final course project of the Advanced Intelligent Systems and Deep Learning in my MS in Computer Science program. I would like to share the project credits with my teammate 
[Vijay Ganaraju](https://www.vijaykvganaraju.com/)
.**
