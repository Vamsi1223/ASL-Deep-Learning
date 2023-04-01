
# American-Sign-Language-Detection-Using-Deep-Learning-Features

American Sign Language (ASL) is a visual language used by the deaf and hard-of-hearing community in the United States. The ability to detect and interpret ASL is important for improving communication and accessibility for this community. Traditional methods of detecting ASL rely on manual annotation or the use of specialized sensors, which can be costly and time-consuming. In recent years, deep learning techniques have shown promise for automated ASL detection, as they can learn representations of ASL gestures directly from raw data.

In this research, we propose to investigate the use of deep learning features for ASL detection. Specifically, we aim to train a deep neural network to recognize and classify ASL gestures based on their visual features. We will explore different types of deep learning architectures, such as Convolutional Neural Networks (CNNs), to find the most effective approach for ASL detection.
    
    
![image](https://user-images.githubusercontent.com/90703475/229161538-55a86f9b-ac9f-4f1b-b6e4-76351698cd34.png)


The above picture gives the information about American sign language Signs. ASL is a complete and organized visual language that is expressed by employing both manual and nonmanual features.



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

The following picture shows the last layers of InceptionV3 model:


![image](https://user-images.githubusercontent.com/90703475/228722811-647f7f73-ec7d-466f-ade8-4408d791bf0a.png)




## Technologies used

<img align="left" alt="Visual Studio Code" width="26px" src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/vscode/vscode-original.svg" style="padding-right:10px;" />
<img align="left" alt="Git" width="26px" src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/git/git-original.svg" style="padding-right:10px;" />
<img align="left" alt="Tensorflow" width="26px" src="https://avatars.githubusercontent.com/u/15658638?s=200&v=4" style="padding-right:10px;" />
<img align="left" alt="Keras" width="26px" src="https://avatars.githubusercontent.com/u/34455048?s=200&v=4" style="padding-right:10px;" />
<img align="left" alt="Google Colab" width="26px" src="https://3.bp.blogspot.com/-apoBeWFycKQ/XhKB8fEprwI/AAAAAAAACM4/Sl76yzNSNYwlShIBrheDAum8L9qRtWNdgCLcBGAsYHQ/s1600/colab.png" style="padding-right:10px;" />


## Dataset


## Dataset

We trained our model by using dataset which is available in kaggle.

It consists of 29 classes in which 26 classes are for A - Z and remaining are space, delete and nothing which are very useful for Real time detection.

All images are of size 200 x 200 pixels. In each class there are 3000 images in total dataset consists of 87,000 images which are quite sufficient to train model.

Sample images from dataset we used are

![A_test](https://user-images.githubusercontent.com/90703475/229159586-adb4f6a8-889c-46e5-aa38-d1643cc3f769.jpg)



![Z_test](https://user-images.githubusercontent.com/90703475/229159595-afca017e-af70-4e79-8e08-0afd97562488.jpg)




![O_test](https://user-images.githubusercontent.com/90703475/229159598-1ed26e4c-51d8-4194-9065-2a92f372eb09.jpg)



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
et al. Imagenet large scale visual recognition challenge.2014.
7) R. Girshick, J. Donahue, T. Darrell, and J. Malik. Rich feature hierarchies for accurate object detection and semantic segmentation. In Proceedings of the IEEE Conference on Computer Vision and Pattern Recognition (CVPR), 2014



## Project Mentor


## Project Mentees

