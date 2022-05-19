---
layout: single
title: About the Nurse Care Activity Recognition Challenge 2022
permalink: /learn/
date: 2022-05-19T00:00:00+09:00
---

Human Activity Recognition (HAR) is the process of handling information from sensors and/or video capture devices under certain circumstances to correctly determine human activities. Traditionally, the HAR can be achieved by human observation through the visualization of video recording devices. However, it is time and labor consuming. Nowadays, this traditional way could be replaced by other simple and automatic methods based on sensors and Artificial Intelligence platforms. For instance, your smartphone or other smart wearable devices have the ability to recognize some of your movements such as walking or running based on the inside accelerometer sensor.

In addition, HAR has several remarkable applications in the real world, especially in the healthcare field. Besides the elderly/patient’s activity monitoring, the caregiver’s activity recognition plays an important role to improve the healthcare quality. Moreover, specifically in developed countries, the number of the elderly increases rapidly due to population aging, while the number of nurses can not satisfy. The greater the pressure on nurses, the more uncertain the healthcare quality is. Therefore, nurse care activity recognition is implemented to help the caregiver/nurse well manage and improve the quality of their work. In this challenge, based on the accelerometer data collected from the smartphone, the cheapest and easy-to-implement way, we aim to recognize the daily nurse care activities taking place at the nursing care facility.

## Challenge Goal (to be updated)
This year's goal of the Nurse Care Activity Recognition Challenge is to predict the daily activities of a caregiver/nurse in a healthcare facility based on the care records file and accelerometer data collected from smartphones. Along with the time data from the care records we expect participants to utilize accelerometer data to predict the future occurrence of the activities. The activity labels can be found in care record files. We want the participants to propose the methods to extract features from these data, use different windowing methods if possible and then feed them to their own model. Finally, each team needs to use their model to predict the activity followed by the timestamp in the test data. You can check out the basic [HAR tutorial here]("https://abc-research.github.io/nurse2021/tutorial/tutorial.html").

The training and testing dataset contains accelerometer data and care record data of 5 users ( 8, 13, 14, 15, 25), which were collected on May and June, 2018. Training and testing data were separated in 70~30 ratio based on each user data. Participants are required to propose their pipelines, predict and submit the activity label for the testing dataset.


<!--edit this part
The goal of the Nurse Care Activity Recognition Challenge is to recognize the daily activities of a caregiver/nurse in a healthcare facility based on the accelerometer data collected from smartphones. Participants utilize accelerometer data and its activity labels in training files, propose the methods to extract features from these data, and then feed to their own model. Finally, each team needs to use their model to predict the activity based on the accelerometer data following by the timestamp in the test data. 

- [Tutorial here](/challenge2022/tutorial/tutorial.html) 
- [To understand the dataset more clearly](/challenge2022/data/)

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



## Data Description
The accelerometer data has been collected using one smartphone carried by subjects, which are caregivers and nurses, when they were conducting daily works at a healthcare facility. The smartphone was carried in an arbitrary position such as a pocket. There are a total of 27 activities divided into 4 groups. All the activities are listed in the below table.

<style>
tr,
td {
    border: none;
}

</style>
<table style="border: none">
  <tr>
    <th style="text-align: center"><h3>Activities of direct care</h3></th>
  </tr>
    <tr><td>1: Vital</td></tr>
    <tr><td>7: Morning gathering/ exercises</td></tr>
    <tr><td>13: Family/guest response</td></tr>
    <tr><td>2: Meal/medication</td></tr>
    <tr><td>8: Rehabilitation / recreation</td></tr>
    <tr><td>14: Outing response</td></tr>
    <tr><td>3: Oral care</td></tr>
    <tr><td>9: Morning care</td></tr>
    <tr><td>19: Get up assistance</td></tr>
    <tr><td>4: Excretion</td></tr>
    <tr><td>10: Daytime user response</td></tr>
    <tr><td>20: Change dressing assistance</td></tr>
    <tr><td>5: Bathing/wiping</td></tr>
    <tr><td>11: Night care</td></tr>
    <tr><td>21: Washing assistance</td></tr>
    <tr><td>6: Treatment</td></tr>
    <tr><td>12: Nighttime user response</td></tr>
    <tr><td>27: Emergency response such as accident</td></tr>
</table>

<table>
  <tr>
    <th style="text-align: center"><h3>Activities of residence cleaning</h3></th>
  </tr>
    <tr><td>15: Linen exchange</td></tr>
    <tr><td>23: Preparation and checking of goods</td></tr>
    <tr><td>24: Organization of medications</td></tr>
    <tr><td>16: Cleaning</td></tr>
</table>

<table>
  <tr>
    <th style="text-align: center"><h3>Documentation/Communication activities</h3></th>
  </tr>
    <tr><td>17: Handwriting recording</td></tr>
    <tr><td>22: Doctor visit correspondence</td></tr>
    <tr><td>25: Family/doctor contact</td></tr>
    <tr><td>18: Delegating/meeting</td></tr>
</table>

<table>
  <tr>
    <th style="text-align: center"><h3>Other activities</h3></th>
  </tr>
    <tr><td>26: Break</td></tr>
    <tr><td>28: Special remarks/notes</td></tr>
</table>


## Data structure
In this challenge, participants are provided training data and test data. Training data contains accelerometer data from 12 subjects (2, 3, 4, 5, 6, 7, 9, 12, 17, 19, 21, and 22) and the activity labels file, which was collected in May and June, 2018 (before June 18th). Test data contains the data of 12 subjects (same id with the train data), which was collected in June, 2018 (at 18th and afterward).

The provided training data folder includes the accelerometer data files of 12 subjects and the “label” folder, which contains “label_train.csv". 

![fiels](/nurse2021/assets/files.png)

In each accelerometer data file, we have 4 columns: datetime and 3 coordinates of the accelerometer data.

![data-acc](/nurse2021/assets/data-acc.png)


In the label file (“label.csv”), we have 12 columns: id (label id), user_id, role, activity_type_id, activity_type (name in japanese), activity_type_e (name in english), date, start time, finish time (of the activity), target_id (patients), target_role, activity2user_id.
Participants should note that the start and finish time at the label_train file may differ from the datetime at the accelerometer file due to the different time zone.

![data-record](/nurse2021/assets/data-record.png)

## Test Data Setting
This dataset was used in our previous work, titled [“Integrating Activity Recognition and Nursing Care Records: The System, Deployment, and a Verification Study”](https://dl.acm.org/doi/abs/10.1145/3351244). The authors of this work proposed a theory that  extension of start and ending time of the activities can increase the prediction rate. The reason behind the theory is that many of the nurses provided the labels before or after completing an activity. In the paper they verified and proved this theory. Following the theory, in the test data the time is extended for both start and end of an activity for 20 minutes. As the time is extended, there are some overlaps for the activity labels for some samples. So, the submission of the participants will be evaluated per activity following the same test setting as the paper. The final score will be calculated by taking the prediction average of all the activities.

## Prizes
- The winning team will be awarded 100,000 jpy.
- The registration fee for the 1st and 2nd runner-up teams will be waived.
- Each of the participating teams will be awarded with participation certificate.

