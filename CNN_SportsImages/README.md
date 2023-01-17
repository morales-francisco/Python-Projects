# CNN (Tensorflow) - Sports Image Classification #


## Introduction ##
Collection of sports images covering 100 different sports. Images are 224, 224, 3 jpg format. Data is separated into train, test and valid directories

## Source ##
The data source is [Kaggle](https://www.kaggle.com/datasets/gpiosenka/sports-classification).

## Objective ##
The objective of the model is to identify which sport the image belongs to. The intended business application is to be able to generate content adjusted to the preferences of the people who follow us on social networks. A two-day campaign is started asking individuals to upload a photo to their stories with a specific hashtag and a picture of their preferred sport to track these preferences. There, we will download the image that they posted to their stories, use this model to determine the sport to which it belongs, find the sports that are frequently referenced, and then modify upcoming material in light of the findings to boost follower growth and engagement.

## Conclusions ##

To process the images, we first have to convert them to a tensor format that can be consumed by the network. For them, we follow these steps:
- Read the image files.
- Decode the JPEG content to get an RGB grid of pixels.
- Convert them into floating point tensors.
- Scale the pixel values to the interval [0, 1].

Based on the results from the first model, significant overfitting can be observed.Up to epoch 2, the accuracy and loss are similar in both train and test. From epoch 3 on, the overfitting starts to be evident, since the train accuracy starts to tend to 1 and in test it does not improve, while the loss curve from epoch 3 begins to decrease in train and increases in test.

Based on the previous model where a marked overfitting is observed, I am going to apply some regularization layers (L1) and add some Dropout layers.Even applying some techniques to reduce overfitting, no noticeable improvements were observed. The other options would be to continue testing different combinations of models by reducing the number of layers and/or neurons or to change the model to improve its generalization power.

Based on the above, we decided to implement a Transfer Learning model. For this particular case, we are going to try the MobileNetV2 model. From the implementation of the MobileNetV2 model we see a remarkable improvement in the accuracy of the model, as well as a remarkable decrease in the loss function. The first model (the simplest one) had an accuracy of 36% and a loss value of 6 for the validation set after 10 epochs, while the last model (MobileNetV2) has an accuracy of 89% and a loss value of 0.35 under the same conditions.

As a last step I decided to test the transfer learning model but training the layers, to see if we get an improvement and get closer to 100% in accuracy, but the reality is that we obtained a poor performance (we noticed the existence of overfitting, similar to the first model). We performed the test by freezing a larger number of layers and also freezing the last layers of the model, but the variations in the results were not significant. As a final conclusion, we think that it would be better to use the Transfer Learning model without training the MobilNetV2 parameters, since it obtains better results for both accuracy and loss validation.
