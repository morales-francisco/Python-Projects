# CNN (Tensorflow) - Sports Image Classification #


## Introduction ##
Collection of sports images covering 100 different sports. Images are 224, 224, 3 jpg format. Data is separated into train, test and valid directories

## Source ##
The data source is [Kaggle](https://www.kaggle.com/datasets/gpiosenka/sports-classification).

## Objective ##
The model's goal is to determine which sport an image belongs to. The ability to produce content that is tailored to the preferences of those who follow us on social networks is the intended business application. In order to track people's preferences, a two-day campaign is launched asking them to post a picture of their favorite sport and a specific hashtag to their Instagram stories. In order to increase follower growth and engagement, we will then modify upcoming content in light of the results by downloading the image that was posted to their stories, using this model to identify the sport to which it belongs.

## Conclusions ##

The images must first be converted into a network-compatible tensor format before being processed. We take the following actions for them: 
- Read the image files.
- Decode the JPEG content to get an RGB grid of pixels.
- Convert them into floating point tensors.
- Scale the pixel values to the interval [0, 1].

The first model's results show a significant  overfitting. The accuracy and loss are comparable between the train and test up until epoch 2. Epoch 3 onwards marks the beginning of the overfitting, as the accuracy in the train begins to tend toward 1 and does not improve in the test, while the loss curve starts to decrease in the train and rise in the test at this point.

Based on the previous model, which shows significant overfitting, I'm going to add some regularization layers (L1) and some Dropout layers. Even after using some methods to reduce overfitting, no perceptible improvements were found. Other options for improving its generalization power include continuing to test different combinations of models (reducing the number of layers or neurons) or attempting a new model.

I made the decision to use a Transfer Learning model in light of the comments mentioned above. I'm going to run the MobileNetV2 model in this specific case. I observe a notable increase in the model's accuracy and a remarkable reduction in the loss function as a result of the MobileNetV2 model's implementation. The final model (MobileNetV2) has an accuracy of 89% and a loss value of 0.35 under the same conditions, while the first model (the simplest one) had an accuracy of 36% and a loss value of 6 for the validation set after 10 epochs.

To see if we could improve and get closer to 100% accuracy, I decided to test the transfer learning model by training the layers. However, the results were disappointing (we noticed the existence of overfitting, similar to the first model). We ran the test with a larger number of layers frozen, as well as the model's final layers, but the variations in the outcomes were not statistically significant. In order to draw a final conclusion, I believe it would be preferable to use the Transfer Learning model without the trained layers because it yields better accuracy and loss validation results.
