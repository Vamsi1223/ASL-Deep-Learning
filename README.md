# ASL-Deep-Learning

This Project is about detection of American Sign Language, initially detecting letters and displaying it, and then determining words with Real-time detection implementation.

Updates:
# Introduction
According to the Communication Service for the Deaf (CSD) [1], there are 360 million deaf people worldwide. Another report by the World Health Organization (WHO) [2] bumps up the number to 466 million people or over 6% of the world's population suffering from disabling hearing loss. Approximately 70 million people around the world are deaf-mute. While translation services have
become easily accessible for about 100 languages, sign language is still an area that has not been explored. Our goal is to detect & translate the letters of ASL in real-time.

# Technologies used

# About Architecture
To get foundation for the model configuration used a popular approach in deep learning called Transfer learning approach.
![image](https://user-images.githubusercontent.com/90703475/224968708-e2a7dd1b-879a-4033-beaf-55c6d05677ae.png)

Mainly Focusing on MobileNetV2 Architecture.
Model consists of a sequence of layers, with the input being a 2D image. The layers are:


4 Dense layers with 1024 units, 512 units, 256 units, 128 units and all are with ReLU activation function, and Glorot uniform weight initialization. 

Followed by, UpSampling2D layer with a size of (2, 2) and nearest-neighbor interpolation. Then followed by, Conv2D layer with a kernel size of 4, 64 filters, ReLU activation function, and VarianceScaling weight initialization.


Then followed by, DepthwiseConv2D layer with a kernel size of 4, strides of (1,1), padding of 'valid', depth multiplier of 1, ReLU activation function, and Glorot uniform weight initialization. 

Then again used UpSampling2D layer with a size of (2, 2) and nearest-neighbor interpolation. Followed by, DepthwiseConv2D layer with a kernel size of 4, strides of (1,1), padding of 'valid', depth multiplier of 1, ReLU activation function, and Glorot uniform weight initialization.


After this started implemented a Conv2D layer with a kernel size of 4, 64 filters, ReLU activation function, and VarianceScaling weight initialization.


Then used 9 Dense layers with 128 units, 256 units, 512 units, 1024 units, 2048 units, 512 units, 256 units, 128 units and all with ReLu activation function, and Glorot uniformm weight initialization.


Then used MaxPooling2D layer with a pool size of (2,2) and strides of 2. After this to flatten the output of the previous layer to a vector used a Flatten layer to flatten the output of the previous layer to a vector. Finally a Dense layer which is output layer fully connected layer with softmax activation function.

This is about the information of the implemented model and let's see the architecture of the model 


# About Dataset
We took dataset from kaggle which consists of 36 directories which includes alphabets and numbers from 0 to 9. In this project we used only alphabets for training model and each alphabet is oriented with 70 different styles. Which gives a sign of sufficient dataset for training model. Here are sample pics of dataset.

![hand1_a_bot_seg_3_cropped](https://user-images.githubusercontent.com/90703475/224979335-9e888e61-7e38-4ea0-8dbb-4a152a8b6c61.jpeg)
![hand1_b_bot_seg_2_cropped](https://user-images.githubusercontent.com/90703475/224979424-c6009276-7b09-408a-a5ed-b65650764f8c.jpeg)
![hand1_c_bot_seg_2_cropped](https://user-images.githubusercontent.com/90703475/224979519-b0e48351-734e-4a06-8657-e9bf04c30649.jpeg)

# Performance of Model

# Conclusion
# References
[1] C. Soukup, \Communication service for the deaf,"
1975. https://www.csd.org/, Last accessed on
2021-05-31.

[2] R. E. C. David W Dowdy, \World health
organization. office of library and health literature
services," 1988. https://www.who.int/, Last
accessed on 2021-05-31.

# Project Mentors
# Project Mentees
