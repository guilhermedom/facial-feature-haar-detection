# Facial Feature Haar Detection

Haar cascade classifiers detecting faces and eyes in images with OpenCV.

---

## Problem Overview

[Computer vision] has become an increasingly popular task in machine learning since the introduction of [deep learning]. [Transfer learning] has also contributed in this popularity increase while used in conjunction with [Convolutional Neural Networks] (CNNs). Many objectives were unattainable in the past due to the lack of efficiency or accuracy of classical computer vision algorithms. Deep learning has helped the field go through that barrier. However, some tasks were already reasonably workable with algorithms of the past.

Studying veteran algorithms is important because they can bring new ideas or minimize the resolving of solved problems. Many classical computer vision algorithms were already using convolution-like operations with matrices long before the advent of convolutional neural networks, a pillar of deep learning. Some of the computer vision classics were able to detect objects and persons, or even facial features, serving as classifiers or feature extractors. They also did that while being transferable; pretrained on more general image datasets.

A [haar cascade classifier] is a sequence of haar filters working to identify a pattern in an image. These filters go through the image as sliding windows. They can detect variations in pixel color intensity on many different regions of the image. If a particular pattern of intensity variation is noticed in any region of the image, this region goes through a series of haar filters that will proof check if that pattern is indeed the pattern expected to be found on the searched object. This is a very similar operation to the convolutions present in CNNs. In the next figure, the haar classifier process is illustrated:

![facial_feature_haar_detection_haar_features](https://user-images.githubusercontent.com/33037020/200151882-46e307b2-9958-4436-8fca-1106f3dfa2db.PNG)

## Analysis Introduction

Haar cascade classifiers revolutionized the computer vision field of study and were a reference to many other algorithms for face detection in smartphone cameras for focus and other adjustments. We propose to use two different haar cascade classifiers to detect facial features on images captured from a webcam and sent to the cloud. One classifier is pretrained to detect faces; the other to detect eyes. Eye detection is performed using only the face area returned by the face detector, for performance reasons. Since they are pretrained, we can also say that this work is also based on transfer learning, a recently popular technique that was already used long ago in computer vision tasks. We use [OpenCV] as back end for this project.

Since we use Google's Colab for this project, we say that our method is able to capture images from a local computer's webcam, send it to the cloud to be analyzed by our haar classifiers and displayed in the notebook in 1.2 seconds or less. Although laggy, we are able to make every frame from a webcam video stream processable, with rare false positive and false negative faces. However, even if it is an efficient method, it has its limitations considering illumination, image quality and head orientation in the image. We briefly discuss some of these in the notebook. Next we show a classified image with the face of the author of this project :).

![facial_feature_haar_detection_me](https://user-images.githubusercontent.com/33037020/200151817-1410fe93-b3f9-47f5-874e-697319723c80.PNG)

[//]: #

[computer vision]: <https://www.ibm.com/topics/computer-vision>
[deep learning]: <https://en.wikipedia.org/wiki/Deep_learning>
[haar cascade classifier]: <https://docs.opencv.org/3.4/db/d28/tutorial_cascade_classifier.html>
[transfer learning]: <https://en.wikipedia.org/wiki/Transfer_learning>
[convolutional neural networks]: <https://www.ibm.com/cloud/learn/convolutional-neural-networks>
[OpenCV]: <https://opencv.org>
