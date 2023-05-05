# CNNTrafficSignRecognition

TRAINING DATA NOT INCLUDED

The Training Data is not included, because the size was too big. Datasets can be found online. The Training folder should have subfolders labeled 0-42 for each of the traffic signs the model is trained for. I've listed the number to traffic sign dictionary below:

0: Speed limit (20km/h)

1: Speed limit (30km/h) 

2: Speed limit (50km/h) 

3: Speed limit (60km/h) 

4: Speed limit (70km/h) 

5: Speed limit (80km/h) 

6: End of speed limit (80km/h) 

7: Speed limit (100km/h) 

8: Speed limit (120km/h) 

9: No passing 

10: No passing vehicle over 3.5 tons 

11: Right-of-way at the intersection 

12: Priority road 

13: Yield 

14: Stop 

15: No vehicles 

16: Vehicle > 3.5 tons prohibited 

17: No entry 

18: General caution 

19: Dangerous curve left 

20: Dangerous curve right 

21: Double curve 

22: Bumpy road 

23: Slippery road 

24: Road narrows on the right 

25: Road work 

26: Traffic signals 

27: Pedestrians 

28: Children crossing 

29: Bicycles crossing 

30: Beware of ice/snow

31: Wild animals crossing 

32: End speed + passing limits 

33: Turn right ahead 

34: Turn left ahead 

35: Ahead only 

36: Go straight or right 

37: Go straight or left 

38: Keep right 

39: Keep left 

40: Roundabout mandatory 

41: End of no passing 

42: End no passing vehicle > 3.5 tons 

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
