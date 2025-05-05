# Sign-Language-Detection-Using-Modified-Alexnet-Architecture
A dataset of 48*48-pixel sign language image dataset for the alphabets and blank class that captures the background is created . The dataset contains 960 images of 27 classes and were taken in non-uniform background and lighting. Some images are shown below.
![image](https://github.com/user-attachments/assets/e1f9466c-b092-4833-a249-5ac879d5fcc7)
#PRE-PROCESSING OF DATASET

In image pre-processing, we converted the images from 3 channel color to grayscale to reduce colour complexity. Then we resized the images into 48*48 pixels for evaluation through CNN. Next, we normalised the grayscale values (0–255) to (0-1) by diving by 255, which gives the pixel array that contains values in the ranges (0–1). The utility of this normalization is that CNN works effectively in the (0–1) range than any other value limits.
#MODEL BUILDING

The model is built using 4 convolutional layers with kernel size 3*3 and ReLU activation function. Dropout layers are used to increase the robustness of the model and is set to 40%. Max pooling layer is used in between the layers to reduce dimensionality of the data. A flattening layer is added to the last of convolutional layer. The neural layer has 4 dense layers and an output layer, with soft max activation. It is optimised with ADAM and categorical cross entropy loss function. The layers also have dropout layers to improve the robustness. The summary of model is shown below.
![image](https://github.com/user-attachments/assets/2756f24c-a56c-4483-aca7-735d51ffb3fb)
![image](https://github.com/user-attachments/assets/6b653291-2363-4f50-9cd7-428231a909ae)
![image](https://github.com/user-attachments/assets/371cbe52-2614-4351-b34e-6b896105ec4c)
#TRAINING AND TESTING
The input images were data augmented to introduced some randomness and variability in data in training so that the model would be robust to overfitting. Image Data Generator did image augmentation with rotation range being 40 degrees, width shift range at 0.2, height shift range at 0.2, shear range at 0.2, zoom range at 0.2, horizontal flip and fill mode set to 'nearest'.  For 100 epochs, the model is trained and the results is shown below.
#RESULTS
The proposed model augments the generated sparse data and use them for training the model. This increases the robustness and decreases the chances of overfitting. The RGB images are converted to grayscale and rescaled to definite size. The CNN model has feature extracting convolution layer, which also helps in decreasing the dimension of the data. The layers are added with batch normalising function to normalise the layer to unit mean unit variance data. The dropout layers randomly drop out neurons in the layer and strengthens the effect of neurons. The dense layers are progressively increased in number of neurons and are activated with ReLU function, and also have dropout function. This model when trained with the data achieved 90%  accuracy.
![image](https://github.com/user-attachments/assets/4bb79f31-533d-435c-8583-afee6afb7cef)
