# CASA0018-Banana-Ripeness-Detection
Author: Haoming Wang (Axe)  
https://www.youtube.com/watch?v=7h5FKB_-l3k (YouTube)  
https://studio.edgeimpulse.com/studio/363527 (Edge-Impulse project page)  
https://github.com/whmfmvp/CASA0018-Banana-Ripeness-Detection (GitHub Repo)  

**Introduction**  
This project aims to develop a banana ripeness detection system based on deep learning for sensor networks. Through this system, users can quickly and accurately judge the ripeness of bananas, which is divided into three stages: Underripe, Ripe, and Overripe. This system is trained on the Edge Impulse platform and uses a large amount of banana image data from different maturity stages to ensure the accuracy of the model. This model is deployed on the mobile phone and implements a portable and practical banana ripeness detection tool.  

The inspiration comes from a common problem in daily life: how to accurately determine the ripeness of fruits. Most people judge whether fruits are ripe by observing their appearance, color, hardness, or smell, which is not only time-consuming and laborious but also has limited accuracy. Accurate judgment of maturity is particularly important, especially for fruits like bananas that are prone to spoilage.  

Adhi Harmoko Saputro(2018) states that the change in the banana's skin color from green to yellow, which signals the banana's maturity, is due to the breakdown of chlorophyll pigment. The real-time classification of bananas using an image processing tool in MATLAB, which employs the RGB color detection technique, is a non-destructive, quick, reliable, and effective process for categorizing bananas (Maithilee Nagesh Kulkarni and Rohini Mudhalwadkar, 2017). A simple algorithm using the CNN model is proposed to determine the ripeness color of fruit, specifically bananas, which can enhance the efficiency for cashiers and customers at counters by simplifying the process of determining fruit and vegetable prices, potentially replacing the conventional weighing method and saving time(Priyanka et al., n.d., 2020).  

**Research Question**  
How to develop an accurate and efficient real-time banana ripeness detection system using deep learning technology and IoT devices?  

**Application Overview**  
This project contains three main parts. First of all, take photos of bananas in different maturity stages and find some pictures online to form banana datasets. Secondly, import datasets in Edge Impulse and choose the best deep learning model by conducting 63 experiments by changing parameters, such as learning block, model chosen, learning rate, dropout rate, batch size, data augmentation and epochs. Lastly, export the code and deploy it on a mobile phone to detect whether the banana is underripe, ripe or overripe.  
![Figure 1. Application diagram of the building blocks of the banana ripeness detection](imgs/Figure_1.png)  
Figure 1. Application diagram of the building blocks of the banana ripeness detection  

**Data**  
Data source  
I went to the supermarket to buy some bananas and took photos of them at different times of purchase and storage to obtain a dataset of underripe, ripe, and overripe bananas. In addition, I collected banana images from different maturity stages online to enrich the dataset and enable the model to receive sufficient training.  

Datasets  
The total number of collected data is 1,189 images, divided into three different labels(Underripe, Ripe and Overripe). Among them, 80 percent images are used for model training and the remaining 20 percent are used for model testing. In addition, 20 percent training images are used for validation, so total ratio of training, validation and testing is 60:20:20.  

	|Training|	Testing|	Total|
 |---------|--------|-------|
|Underripe|	325|	82|	407|
|Ripe|	283|	68|	351|
|Overripe|	348|	83|	431|
|Total|	956|	233|	1189|  
Table 1. Datasets description  

Data pre-processing
The original images have different sizes, I resize all images with 96 width and 96 height in order to unify the banana datasets. Besides, I use “fit shortest axis” and “squash” two different resize modes to test which one has better accuracy performance.  

![Figure 2. Feature explorer of three ripeness types of banana dataset](imgs/Figure_2.png)  
Figure 2. Feature explorer of three ripeness types of banana dataset  

![Figure 3. Create impulse interface](imgs/Figure_3.png)  
Figure 3. Create impulse interface  




