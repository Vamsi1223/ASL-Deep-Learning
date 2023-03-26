
# American-Sign-Language-Detection-Using-Deep-Learning-Features

American Sign Language (ASL) is a visual language used by the deaf and hard-of-hearing community in the United States. The ability to detect and interpret ASL is important for improving communication and accessibility for this community. Traditional methods of detecting ASL rely on manual annotation or the use of specialized sensors, which can be costly and time-consuming. In recent years, deep learning techniques have shown promise for automated ASL detection, as they can learn representations of ASL gestures directly from raw data.

In this research, we propose to investigate the use of deep learning features for ASL detection. Specifically, we aim to train a deep neural network to recognize and classify ASL gestures based on their visual features. We will explore different types of deep learning architectures, such as Convolutional Neural Networks (CNNs), to find the most effective approach for ASL detection.




## Abstract 

Understanding sign language is one of the primary requirement in 
helping users of sign language communicate with the rest of the 
society. Speech impairment is a disability which affects an 
individuals ability to communicate using speech and hearing.
People who are affected by this use other media of communication
such as sign language. Although sign language is ubiquitous in
recent times, there remains a challenge for non-sign language
speakers to communicate with sign language speakers or signers.
With recent advances in deep learning and computer vision
there has been outstanding progress in the fields of motion and
gesture recognition using deep learning and computer vision based techniques. The focus of this work is to design a deep learning model offers sign language translation to text. In this proposed model we used Inceptionv3 for creating a new efficient model.

## Model Architecture - InceptionV3
To get foundation for the model configuration used a popular approach in deep learning called Transfer learning approach.

![image](https://user-images.githubusercontent.com/90703475/224968708-e2a7dd1b-879a-4033-beaf-55c6d05677ae.png)


Architecture we used is InceptionV3.


Inception-v3 is a convolutional neural network architecture that was introduced by Google in 2015. It is a successor to the original Inception-v1 and Inception-v2 architectures and was designed to achieve better accuracy and efficiency in image recognition tasks.

The Inception-v3 architecture consists of a series of convolutional layers, followed by a global average pooling layer and a fully connected layer. The convolutional layers use various filter sizes, including 1x1, 3x3, and 5x5, in order to capture features of different scales. The network also includes inception modules, which are blocks of layers that incorporate multiple filter sizes and pooling operations in parallel.

Inception-v3 also includes several other features that contribute to its performance, such as batch normalization, dropout regularization, and label smoothing. Additionally, the network uses an auxiliary classifier to provide additional regularization and facilitate training.

Overall, the Inception-v3 architecture has been shown to achieve state-of-the-art performance on a variety of image recognition tasks, including the ImageNet Large Scale Visual Recognition Challenge.

The model architecture is as follows:






## Dataset

We trained our model by using dataset which is available in kaggle.

It consists of 29 classes in which 26 classes are for A - Z and remaining are space, delete and nothing which are very useful for Real time detection.

All images are of size 200 x 200 pixels. In each class there are 3000 images in total dataset consists of 87,000 images which are quite sufficient to train model.

Sample images from dataset we used are


<img src="https://storage.googleapis.com/kagglesdsdata/datasets/23079/29550/asl_alphabet_test/asl_alphabet_test/A_test.jpg?X-Goog-Algorithm=GOOG4-RSA-SHA256&X-Goog-Credential=databundle-worker-v2%40kaggle-161607.iam.gserviceaccount.com%2F20230326%2Fauto%2Fstorage%2Fgoog4_request&X-Goog-Date=20230326T084416Z&X-Goog-Expires=345600&X-Goog-SignedHeaders=host&X-Goog-Signature=8bbd6d90be8c878aea74e6ac4f25aefe9e168a6bef34dba61a273e60dd77b631fa20f44de246358d0a4e51a240d592f12b3f9a07a8afbce9b7b61837233b4b8fe1aed43ee2c36be5a39da43a2ea2a079f96df146719f464d81f1c88f09c7ef575d91e7d19520445d4170adb51286f9f2b8627c7d0644737202c351a08ce42af0e6b4d0d93360ad91f49b7f180245eb2201b80c448a5b2038a12313f94d1e0e672b7115a297fd6d6475f3ab15b78e5f15cb684ad16b824949c38842c95437b8eed75a6a5846bec799792052314633dca80d60d2bf4907d5aa816a44a1d76736cdb7714029fe93e0eb59c6593a366d69a8cfe89be09eb10302d82e0386b5e3ecfc" alt="A" width="200" height="200">
<img src="https://storage.googleapis.com/kagglesdsdata/datasets/23079/29550/asl_alphabet_test/asl_alphabet_test/U_test.jpg?X-Goog-Algorithm=GOOG4-RSA-SHA256&X-Goog-Credential=databundle-worker-v2%40kaggle-161607.iam.gserviceaccount.com%2F20230326%2Fauto%2Fstorage%2Fgoog4_request&X-Goog-Date=20230326T084416Z&X-Goog-Expires=345600&X-Goog-SignedHeaders=host&X-Goog-Signature=bc8084176ea63a03c2017b52be0ce67c6df650f804fce4ea0c9a0361b5fab1333960f421ac0ffd1ccec30b6f322b69ec44e351b6e32fc2da50a7f31ae3362229dad7bace8f92b67ea4ce15c3b3cd61b717459beac829279b5c2bf72f0f0c304f335c7bb145aeab4709635063470f361d67329bfb155faf9a34f468fe24708710b7cfd95db8ff384ab17538efa42445ecbf99c2abed4f7565e85d768e00108d521107722ef945c5f07c04e97ee1e39754f018c77b933bc8b16abacf632aedbc645f685a29e826fd2bcc9729dc65b9c8279e788a8e7d85166764a4810f848240ef4395f3c4418926f4f014416f2b3252b078cd2f5725dca27a95589b3f012eb3df" alt="Y" width="200" height="200">
<img src="https://storage.googleapis.com/kagglesdsdata/datasets/23079/29550/asl_alphabet_test/asl_alphabet_test/O_test.jpg?X-Goog-Algorithm=GOOG4-RSA-SHA256&X-Goog-Credential=databundle-worker-v2%40kaggle-161607.iam.gserviceaccount.com%2F20230326%2Fauto%2Fstorage%2Fgoog4_request&X-Goog-Date=20230326T084416Z&X-Goog-Expires=345600&X-Goog-SignedHeaders=host&X-Goog-Signature=c00be6903f4f2b527aff53eda12cd4d16cc000cd3a57e15729f2630027b5fdcd6ff80eb160f70c7f4d3dfedcf7cd124726bfb95b00a1fc5a24565153fbfa8350c5d021ca5c5bf49c24c6b226d465ab041d60daed015f3c05bad5816973ce8126947723913ed96205359bb7985dc41c1b58b40b32ecaa207d47a5fdee8e7c2c79e152ecc89ec30df0c199509bdca5d6a2d33d692ea22e6f47cf7844eed7152c4d52eabb52aff3ef1fc5a70768c19ed31ad4716c6aec1ae1bfe8361b12ad4e65d6c49c479f56b0ec110fe0a405159c0762cf76ca77b9a81f78486ca89ad8ad6c51786a79a211e8a67bd549834a6f80728bffaf0d8bfbdfd056dfdbcd6c206ab415" alt="O" width="200" height="200">

## Performance

This Model which we trained using ASL dataset is giving an accuracy of 96.42%. 


The accuracy plot is as follows:


![image](https://user-images.githubusercontent.com/90703475/227776913-bbcb8702-34e4-4a53-baa8-e1d5870d420f.png)


Loss plot is as follows: 


![image](https://user-images.githubusercontent.com/90703475/227776787-8dc18c60-b379-4b77-88fe-baeb294b99da.png)


## References

1) Ira Cohen, Nicu Sebe, Ashutosh Garg, Lawrence S, Chen and Thomas S. Huang (2003, February). Facial expression recognition from video sequences: temporal and static modeling. Computer Vision and Image Undertaking 91.
2) Brandon Garcia and Sigberto Viesca, "Real-time American Sign Language Recognition with Convolutional Neural Networks", in Convolutional Neural Networks for Visual Recognition at Stanford University, 2016
3) Continuous dynamic Indian Sign Language gesture recognition with invariant backgrounds by Kumud Tripathi, Neha Baranwal, G. C. Nandi at 2015 Conference on Advances in Computing, Communications and Informatics (ICACCI)
4) G. Saldana Gonz ˜ alez, J. Cerezo S ´ anchez, M. M. Bustillo D ´ ´ıaz, and A. Ata Perez, “Recognition and classification of sign language for ´ spanish,” Computacion y Sistemas ´ , vol. 22, no. 1, pp. 271–277, 2018.
5) D. Chakraborty, D. Garg, A. Ghosh, and J. H. Chan, “Trigger detection system for american sign language using deep convolutional neural networks,” in Proceedings of the 10th International Conference on Advances in Information Technology, 2018, pp. 1–6.
6)  O. Russakovsky, J. Deng, H. Su, J. Krause, S. Satheesh,
S. Ma, Z. Huang, A. Karpathy, A. Khosla, M. Bernstein,
et al. Imagenet large scale visual recognition challenge.
2014.
## Project Mentor


## Project Mentees

