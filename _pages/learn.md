---
layout: single
title: About the Nurse Care Activity Recognition Challenge 2022
permalink: /learn/
date: 2022-04-14T00:00:00+09:00
---

Human Activity Recognition (HAR) is the process of handling information from sensors and/or video capture devices under certain circumstances to correctly determine human activities. Traditionally, the HAR can be achieved by human observation through the visualization of video recording devices. However, it is time and labor consuming. Nowadays, this traditional way could be replaced by other simple and automatic methods based on sensors and Artificial Intelligence platforms. For instance, your smartphone or other smart wearable devices have the ability to recognize some of your movements such as walking or running based on the inside accelerometer sensor.

In addition, HAR has several remarkable applications in the real world, especially in the healthcare field. Besides the elderly/patient’s activity monitoring, the caregiver’s activity recognition plays an important role to improve the healthcare quality. Moreover, specifically in developed countries, the number of the elderly increases rapidly due to population aging, while the number of nurses can not satisfy. The greater the pressure on nurses, the more uncertain the healthcare quality is. Therefore, nurse care activity recognition is implemented to help the caregiver/nurse well manage and improve the quality of their work. In this challenge, based on the accelerometer data collected from the smartphone, the cheapest and easy-to-implement way, we aim to recognize the daily nurse care activities taking place at the nursing care facility.

## Challenge Goal
The goal of the Nurse Care Activity Recognition Challenge is to recognize the daily activities of a caregiver/nurse in a healthcare facility based on the accelerometer data collected from smartphones. Participants utilize accelerometer data and its activity labels in training files, propose the methods to extract features from these data, and then feed to their own model. Finally, each team needs to use their model to predict the activity based on the accelerometer data following by the timestamp in the test data. 

- [Tutorial here](/challenge2022/data/). 
- [Registration is opening now.](https://forms.gle/d22qHnHWmJ9FNgHR7)
- [To understand the dataset more clearly](/challenge2022/tutorial/).

The training and testing dataset contains accelerometer data of 12 users (2, 3, 4, 5, 6, 7, 9, 12, 17, 19, 21, and 22), which were collected on May and June, 2018. The training data is provided with the activities labels, which describe the users’ activities before 18th June, 2018. The testing data was the accelerometer data acquired on 18th June and afterward. Participants are required to propose their pipelines, predict and submit the activity label for the testing dataset.


## Evaluation
Accuracy will be used as the performance measure.

<!--
Submissions will be evaluated by the average of the accuracy of macro activity classification (ma) and the average accuracy of micro-activity classification (mi). That is (ma+mi)/2.

The average accuracy of micro-activity classification is based on the multi-label accuracy formula. The accuracy of one sample is given by the number of correct labels predicted divided by the number of total true and predicted labels (cardinality of the union). 
-->

## Prizes
- The winning team will be awarded 100,000 jpy.
- The registration fee for the 1st and 2nd runner-up teams will be waived.
- Each of the participating teams will be awarded with participation certificate.

