# GENDER AND AGE DETECTION USING DEEP LEARNING 

## A. PROJECT SUMMARY

**Project Title:** Gender and Age Detection

![family](https://user-images.githubusercontent.com/44885554/114744544-6329f180-9d80-11eb-874b-4e89cc841c5d.png)

**Team Members:** 
- MUHAMMAD AKMAL BIN MOHD SABRI
- WAN MUHAMMAD ISMAT BIN WAN AZMY
- MUHAMMAD AKMAL KHAIRI BIN ABDUL HALIM
- MUHAMMAD IMRAN BIN ISMAIL

**Objectives:**
- To build a gender and age detector that can approximately guess the gender and age of the person (face) in a picture using Deep Learning on the Adience dataset.

##  B. ABSTRACT 

In this Python Project, we will use Deep Learning to accurately identify the gender and age of a person from a single image of a face. We will use the models trained by Tal Hassner and Gil Levi. The predicted gender may be one of ‘Male’ and ‘Female’, and the predicted age may be one of the following ranges- (0 – 2), (4 – 6), (8 – 12), (15 – 20), (25 – 32), (38 – 43), (48 – 53), (60 – 100) (8 nodes in the final softmax layer). It is very difficult to accurately guess an exact age from a single image because of factors like makeup, lighting, obstructions, and facial expressions. And so, we make this a classification problem instead of making it one of regression.

**The CNN Architecture:**
The convolutional neural network for this python project has 3 convolutional layers:

- Convolutional layer; 96 nodes, kernel size 7
- Convolutional layer; 256 nodes, kernel size 5
- Convolutional layer; 384 nodes, kernel size 3

It has 2 fully connected layers, each with 512 nodes, and a final output layer of softmax type.

To go about the python project, we’ll:

- Detect faces
- Classify into Male/Female
- Classify into one of the 8 age ranges
- Put the results on the image and display it

![python-project-example-output-1](https://user-images.githubusercontent.com/58213194/114746369-3f67ab00-9d82-11eb-8f39-0730d750ef30.png)

**Figure 1:** AI output of detecting the user's gender & age.

## C.  DATASET

For this python project, we’ll use the Adience dataset; the dataset is available in the public domain and you can find it here. This dataset serves as a benchmark for face photos and is inclusive of various real-world imaging conditions like noise, lighting, pose, and appearance. The images have been collected from Flickr albums and distributed under the Creative Commons (CC) license. It has a total of 26,580 photos of 2,284 subjects in eight age ranges (as mentioned above) and is about 1GB in size. The models we will use have been trained on this dataset.

**Prerequisites:**

You’ll need to install OpenCV (cv2) to be able to run this project. You can do this with pip-

```python
  pip install opencv-python
```

Other packages you’ll be needing are math and argparse, but those come as part of the standard Python library.

**Purposes:**

- Detect human's gender either ‘Male’ and ‘Female’ in images
- Detect human's age in images
- Detect human's gender & age in real-time video streams

Let’s try this gender and age classifier out on some of our own images now.

We’ll get to the command prompt, run our script with the image option and specify an image to classify:

**Example 1**

![interesting-python-project-example](https://user-images.githubusercontent.com/58213194/114747254-388d6800-9d83-11eb-9748-dfaeb2f416d1.png)

**Figure 2:** Example python command to execute & evaluate the image from the dataset.

**Output:**

![python-project-example-output-1](https://user-images.githubusercontent.com/58213194/114747518-80ac8a80-9d83-11eb-9402-5a7699d5d153.png)

**Figure 3:** Program output after evaluating the image provided into the command.

***

**Example 2**

![2](https://user-images.githubusercontent.com/58213194/114747675-ac2f7500-9d83-11eb-9b6a-641f3e778a93.png)

**Figure 4:** Example python command to execute & evaluate the second image from the dataset.

**Output:**

![22](https://user-images.githubusercontent.com/58213194/114747704-b3568300-9d83-11eb-991e-6f5326d95b21.png)

**Figure 5:** Program output after evaluating the second image provided into the command.

***

**Example 3**

![3](https://user-images.githubusercontent.com/58213194/114747910-ea2c9900-9d83-11eb-8cfa-b8b98aa0f5b8.png)

**Figure 6:** Example python command to execute & evaluate the third image from the dataset.

**Output:**

![33](https://user-images.githubusercontent.com/58213194/114747968-fa447880-9d83-11eb-8552-8b296cd14b69.png)

**Figure 7:** Program output after evaluating the third image provided into the command.

***

**Example 4**

![4](https://user-images.githubusercontent.com/58213194/114748191-3d065080-9d84-11eb-8c20-4d1287070689.png)

**Figure 8:** Example python command to execute & evaluate the fourth image from the dataset.

**Output:**

![44](https://user-images.githubusercontent.com/58213194/114748224-45f72200-9d84-11eb-8386-69d3a754cf40.png)

**Figure 9:** Program output after evaluating the fourth image provided into the command.

***

**Example 5**

![5](https://user-images.githubusercontent.com/58213194/114748285-57d8c500-9d84-11eb-960a-c0b67a25f9fc.png)

**Figure 10:** Example python command to execute & evaluate the fifth image from the dataset.

**Output:**

![55](https://user-images.githubusercontent.com/58213194/114748307-5dcea600-9d84-11eb-98d0-b6a04b6a571b.png)

**Figure 11:** Program output after evaluating the fifth image provided into the command.

***

**Example 6**

![6](https://user-images.githubusercontent.com/58213194/114748359-6cb55880-9d84-11eb-8356-51be189eb69b.png)

**Figure 12:** Example python command to execute & evaluate the sixth image from the dataset.

**Output:**

![66](https://user-images.githubusercontent.com/58213194/114748392-76d75700-9d84-11eb-8f67-d76539b2933e.png)

**Figure 13:** Program output after evaluating the sixth image provided into the command.

## D.   PROJECT STRUCTURE

The following directory is our structure of our project:
- $ tree --dirsfirst --filelimit 14
- .
- ├── age_deploy.protxt
- ├── age_net.caffeemodel
- ├── gad.py
- ├── age_deploy.protxt
- ├── age_net.caffeemodel
- ├── girl1.jpg
- ├── girl2.jpg
- ├── kid1.jpg
- ├── man1.jpg
- ├── minion.jpg
- ├── opencv_face_detector.pbtxt
- ├── opencv_face_detector.uint8.pb
- ├── woman1.jpg
- ├── woman2.jpg
- 14 files


The dataset/ directory contains the data described in the “Gender and Age Detection” section.

Eight image examples/ are provided so that you can test the static image gender and age detector.

We’ll be reviewing a Python scripts in this tutorial:

- detect_mask_image.py: Performs gender and age detection in static images & using your webcam, this script applies Age & Gender detection to every frame in the stream

In the next two sections, we will train our Age & Gender detector.


## E   TRAINING THE COVID-19 FACE MASK DETECTION

We are now ready to train our face mask detector using Keras, TensorFlow, and Deep Learning.

From there, open up a terminal, and execute the following command:

- $ python train_mask_detector.py --dataset dataset
- [INFO] loading images...
- [INFO] compiling model...
- [INFO] training head...
- Train for 34 steps, validate on 276 samples
- Epoch 1/20
- 34/34 [==============================] - 30s 885ms/step - loss: 0.6431 - accuracy: 0.6676 - val_loss: 0.3696 - val_accuracy: 0.8242
- Epoch 2/20
- 34/34 [==============================] - 29s 853ms/step - loss: 0.3507 - accuracy: 0.8567 - val_loss: 0.1964 - val_accuracy: 0.9375
- Epoch 3/20
- 34/34 [==============================] - 27s 800ms/step - loss: 0.2792 - accuracy: 0.8820 - val_loss: 0.1383 - val_accuracy: 0.9531
- Epoch 4/20
- 34/34 [==============================] - 28s 814ms/step - loss: 0.2196 - accuracy: 0.9148 - val_loss: 0.1306 - val_accuracy: 0.9492
- Epoch 5/20
- 34/34 [==============================] - 27s 792ms/step - loss: 0.2006 - accuracy: 0.9213 - val_loss: 0.0863 - val_accuracy: 0.9688
- ...
- Epoch 16/20
- 34/34 [==============================] - 27s 801ms/step - loss: 0.0767 - accuracy: 0.9766 - val_loss: 0.0291 - val_accuracy: 0.9922
- Epoch 17/20
- 34/34 [==============================] - 27s 795ms/step - loss: 0.1042 - accuracy: 0.9616 - val_loss: 0.0243 - val_accuracy: 1.0000
- Epoch 18/20
- 34/34 [==============================] - 27s 796ms/step - loss: 0.0804 - accuracy: 0.9672 - val_loss: 0.0244 - val_accuracy: 0.9961
- Epoch 19/20
- 34/34 [==============================] - 27s 793ms/step - loss: 0.0836 - accuracy: 0.9710 - val_loss: 0.0440 - val_accuracy: 0.9883
- Epoch 20/20
- 34/34 [==============================] - 28s 838ms/step - loss: 0.0717 - accuracy: 0.9710 - val_loss: 0.0270 - val_accuracy: 0.9922
- [INFO] evaluating network...

|      |    precision    | recall| f1-score | support |
|------|-----------------|-------|----------|---------|
|with_mask|0.99|1.00|0.99|138|
|without_mask|1.00|0.99|0.99|138|
|accuracy| | |0.99|276|
|macro avg|0.99|0.99|0.99|276|
|weighted avg|0.99|0.99|0.99|276|


![Figure 4](https://www.pyimagesearch.com/wp-content/uploads/2020/04/face_mask_detector_plot.png)

Figure 4: Figure 10: COVID-19 face mask detector training accuracy/loss curves demonstrate high accuracy and little signs of overfitting on the data

As you can see, we are obtaining ~99% accuracy on our test set.

Looking at Figure 4, we can see there are little signs of overfitting, with the validation loss lower than the training loss. 

Given these results, we are hopeful that our model will generalize well to images outside our training and testing set.


## F.  RESULT AND CONCLUSION

Detecting Age & Gender with OpenCV in real-time

You can then launch the mask detector in real-time video streams using the following command:
- $ python gad.py

[![Figure5](https://img.youtube.com/vi/wYwW7gAYyxw/0.jpg)](https://www.youtube.com/watch?v=wYwW7gAYyxw "Figure5")

Figure 5: Age & Gender Detection in real-time video streams

In Figure 5, you can see that our Age & Gender detector is capable of running in real-time (and is correct in its predictions as well.



## G.   PROJECT PRESENTATION 

In this python project, we implemented Convolutional Neural Network (CNN) to detect gender and age from a single picture of a face

**What is Computer Vision?**

Computer Vision is the field of study that enables computers to see and identify digital images and videos as a human would. The challenges it faces largely follow from the limited understanding of biological vision. Computer Vision involves acquiring, processing, analyzing, and understanding digital images to extract high-dimensional data from the real world in order to generate symbolic or numerical information which can then be used to make decisions. The process often includes practices like object recognition, video tracking, motion estimation, and image restoration.

**What is OpenCV?**

OpenCV is short for Open Source Computer Vision. Intuitively by the name, it is an open-source Computer Vision and Machine Learning library. This library is capable of processing real-time image and video while also boasting analytical capabilities. It supports the Deep Learning frameworks TensorFlow, Caffe, and PyTorch.

**What is a CNN?**

A Convolutional Neural Network is a deep neural network (DNN) widely used for the purposes of image recognition and processing and NLP. Also known as a ConvNet, a CNN has input and output layers, and multiple hidden layers, many of which are convolutional. In a way, CNNs are regularized multilayer perceptrons.

[![demo](https://img.youtube.com/vi/-p7HGwOWxtg/0.jpg)](https://www.youtube.com/watch?v=-p7HGwOWxtg "demo")
