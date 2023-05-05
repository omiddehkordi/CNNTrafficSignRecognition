# CNNTrafficSignRecognition

Color vs Grayscale CNN Model

Based on the performance and evaluation of both the color and grayscale model, we can say the grayscale model has a higher accuracy and lower loss and therefore is the better model.
During both the fitting and evaluation phase the training, validation and test accuracy were higher for the grayscale model as can be seen in the graph comparing the training and validation accuracy and loss

Model Class Quality

The classification report indicates that the model’s classes are good and have an average precision and f1 score over .9. However, there are classes that perform worse, but usually those classes have less samples and/or the image quality of the data is very low. The traffic sign for pedestrians performed the worst in both models. The classes worked better for the grayscale model.

Grayscale and Resizing

I used the Pillow library to resize and convert the images to grayscale through functions that can be used on any input data in array/list form. The load functions I created in the notebook take care of reading images from folders into lists/arrays.

Layers

I got my Optimal solution with 4 Conv2d Layers, 2 MaxPool2d layers, 3 Dropout layers, 1 Flatten Layer and 2 Dense Layers with the last Dense layer having a softmax activation to give the final output

Training and Validation Accuracy and Loss

For both models the accuracy of the validation and test data was significantly higher than the training data. The loss was also less for both. A possible explanation could be that the test data was easier. It is also possible that the model is underfitting and that needs to be fixed.

Amount of Data

The Data was distributed among the classes similarly in both training and test data which is probably why there was such high accuracy for test and validation. The weaker performing classes need substantially more data. If the test data had more data for the classes with the least data in training the accuracy would most likely be lower and more representative of how well the model is working, because in training there wasn’t enough data to strengthen the model’s ability to recognize images in those classes.
