---
layout: single
title: About the Nurse Care Activity Recognition Challenge 2022
permalink: /learn/
date: 2022-05-19T00:00:00+09:00
---

Human Activity Recognition (HAR) is the process of handling information from sensors and/or video capture devices under certain circumstances to correctly determine human activities. Traditionally, the HAR can be achieved by human observation through the visualization of video recording devices. However, it is time and labor consuming. Nowadays, this traditional way could be replaced by other simple and automatic methods based on sensors and Artificial Intelligence platforms. For instance, your smartphone or other smart wearable devices have the ability to recognize some of your movements such as walking or running based on the inside accelerometer sensor.

In addition, HAR has several remarkable applications in the real world, especially in the healthcare field. Besides the elderly/patient’s activity monitoring, the caregiver’s activity recognition plays an important role to improve the healthcare quality. Moreover, specifically in developed countries, the number of the elderly increases rapidly due to population aging, while the number of nurses can not satisfy. The greater the pressure on nurses, the more uncertain the healthcare quality is. Therefore, nurse care activity recognition is implemented to help the caregiver/nurse well manage and improve the quality of their work. In this challenge, based on the accelerometer data collected from the smartphone, the cheapest and easy-to-implement way, we aim to recognize the daily nurse care activities taking place at the nursing care facility.

## Challenge Goal 
This year's goal of the Nurse Care Activity Recognition Challenge is to predict the daily activities of a caregiver/nurse in a healthcare facility based on the care records file and accelerometer data collected from smartphones. Along with the time data from the care records we expect participants to utilize accelerometer data to predict the future occurrence of the activities. The activity labels can be found in care record files. We want the participants to propose the methods to extract features from these data, use different windowing methods if possible and then feed them to their own model. Finally, each team needs to use their model to predict the activity followed by the timestamp in the test data. You can check out the basic [HAR tutorial here](https://abc-research.github.io/nurse2021/tutorial/tutorial.html).

- [Check the tutorial here](https://colab.research.google.com/drive/1euqLhhsb21bbOETWMY9DkUcue6t33j1j?usp=sharing) 
- [To understand the dataset more clearly](/challenge2022/data/)
- [To download the dataset](https://ieee-dataport.org/documents/2022-nurse-care-activity-recognition-challenge-datasets)

The training and testing dataset contains accelerometer data and care record data of 5 users ( 8, 13, 14, 15, 25), which were collected on May and June, 2018. Training and testing data were separated in 70~30 ratio based on each user data. Participants are required to propose their pipelines, predict and submit the activity label for the testing dataset.

<!--edit this part
The goal of the Nurse Care Activity Recognition Challenge is to recognize the daily activities of a caregiver/nurse in a healthcare facility based on the accelerometer data collected from smartphones. Participants utilize accelerometer data and its activity labels in training files, propose the methods to extract features from these data, and then feed to their own model. Finally, each team needs to use their model to predict the activity based on the accelerometer data following by the timestamp in the test data. 



The training and testing dataset contains accelerometer data of 12 users (2, 3, 4, 5, 6, 7, 9, 12, 17, 19, 21, and 22), which were collected on May and June, 2018. The training data is provided with the activities labels, which describe the users’ activities before 18th June, 2018. The testing data was the accelerometer data acquired on 18th June and afterward. Participants are required to propose their pipelines, predict and submit the activity label for the testing dataset.
-->

<!--old
## Evaluation
Accuracy will be used as the performance measure.
Submissions will be evaluated by the average of the accuracy of macro activity classification (ma) and the average accuracy of micro-activity classification (mi). That is (ma+mi)/2.

The average accuracy of micro-activity classification is based on the multi-label accuracy formula. The accuracy of one sample is given by the number of correct labels predicted divided by the number of total true and predicted labels (cardinality of the union). 
-->

## Data use
All participants may use the data free of charge.


## Prizes
- The winning team will be awarded 100,000 jpy.
- The registration fee for the 1st and 2nd runner-up teams will be waived.
- Each of the participating teams will be awarded with participation certificate.

