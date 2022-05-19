---
layout: single
title: Data Description
permalink: /data/
date: 2022-05-18T00:00:00+09:00
---
The accelerometer data has been collected using one smartphone carried by subjects, which are caregivers and nurses, when they were conducting daily works at a healthcare facility. The smartphone was carried in an arbitrary position such as a pocket. There are a total of 27 activities divided into 4 groups. All the activities are listed in the below table.

<style>
tr,
td {
    border: none;
}

</style>
<table style="border: none">
  <tr>
    <th style="text-align: left"><h3>Activities of direct care</h3></th>
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
    <th style="text-align: left"><h3>Activities of residence cleaning</h3></th>
  </tr>
    <tr><td>15: Linen exchange</td></tr>
    <tr><td>23: Preparation and checking of goods</td></tr>
    <tr><td>24: Organization of medications</td></tr>
    <tr><td>16: Cleaning</td></tr>
</table>

<table>
  <tr>
    <th style="text-align: left"><h3>Documentation/Communication activities</h3></th>
  </tr>
    <tr><td>17: Handwriting recording</td></tr>
    <tr><td>22: Doctor visit correspondence</td></tr>
    <tr><td>25: Family/doctor contact</td></tr>
    <tr><td>18: Delegating/meeting</td></tr>
</table>

<table>
  <tr>
    <th style="text-align: left"><h3>Other activities</h3></th>
  </tr>
    <tr><td>26: Break</td></tr>
    <tr><td>28: Special remarks/notes</td></tr>
</table>


## Data structure
The training and testing dataset contains accelerometer data and care record data of 5 users ( 8, 13, 14, 15, 25), which were collected on May and June, 2018. Training and testing data were separated in 70~30 ratio based on each user data.

The provided each user folder includes the accelerometer data files for whole time, training care record file and testing care record file. In training care record we have activity information but in testing care record we remove it. Your work is to predict these activities and generate files.
In each accelerometer data file, we have 4 columns: datetime and 3 coordinates of the accelerometer data.

![data-acc](/nurse2021/assets/data-acc.png)

In the care record file, we have 12 columns: id (label id), user_id, role, activity_type_id, activity_type (name in japanese), activity_type_e (name in english), date, start time, finish time (of the activity), target_id (patients), target_role, activity2user_id. Participants should note that the start and finish time at the label_train file may differ from the datetime at the accelerometer file due to the different time zone.
<!---
In this challenge, participants are provided training data and test data. Training data contains accelerometer data from 12 subjects (2, 3, 4, 5, 6, 7, 9, 12, 17, 19, 21, and 22) and the activity labels file, which was collected in May and June, 2018 (before June 18th). Test data contains the data of 12 subjects (same id with the train data), which was collected in June, 2018 (at 18th and afterward).

The provided training data folder includes the accelerometer data files of 12 subjects and the “label” folder, which contains “label_train.csv". 

![fiels](/nurse2021/assets/files.png)

In each accelerometer data file, we have 4 columns: datetime and 3 coordinates of the accelerometer data.

![data-acc](/nurse2021/assets/data-acc.png)


In the label file (“label.csv”), we have 12 columns: id (label id), user_id, role, activity_type_id, activity_type (name in japanese), activity_type_e (name in english), date, start time, finish time (of the activity), target_id (patients), target_role, activity2user_id.
Participants should note that the start and finish time at the label_train file may differ from the datetime at the accelerometer file due to the different time zone.

![data-record](/nurse2021/assets/data-record.png)
-->

## Test Data Setting
This dataset was used in our previous work, titled [“Integrating Activity Recognition and Nursing Care Records: The System, Deployment, and a Verification Study”](https://dl.acm.org/doi/abs/10.1145/3351244). The authors of this work proposed a theory that  extension of start and ending time of the activities can increase the prediction rate. The reason behind the theory is that many of the nurses provided the labels before or after completing an activity. In the paper they verified and proved this theory. Following the theory, in the test data the time is extended for both start and end of an activity for 20 minutes. As the time is extended, there are some overlaps for the activity labels for some samples. So, the submission of the participants will be evaluated per activity following the same test setting as the paper. The final score will be calculated by taking the prediction average of all the activities.

## Data use
All participants may use the data free of charge.

<!--
The accelerometer data has been collected using one smartphone carried by subjects, which are caregivers and nurses, when they were conducting daily works at a healthcare facility. The smartphone was carried in an arbitrary position such as a pocket. There are a total of 27 activities divided into 4 groups. All the activities are listed in the below table.

<ul>
  <li><b>Position of the Mobile phone:</b> Attached in right arm using armband</li>
  <li><b>Sampling rate:</b> 60 Hz</li>
  <li><b>Preprocessing:</b> No preprocessing method is applied on this data</li>
  <li><b>Training and Testing data:</b> <a href = "https://ieee-dataport.org/open-access/nurse-care-activities-datasets-laboratory-and-real-field">Download the training and testing data</a></li>
</ul>

<style>
ul.no-bullets {
  list-style-type: none;
  margin: 1;
  padding: 1;
}
</style>
### Activities of direct care
<ul class="no-bullets">
  <li> 1: Vital </li>
  <li> 7: Morning gathering/ exercises </li>
  <li> 13: Family/guest response </li>
  <li> 2: Meal/medication </li>
  <li> 8: Rehabilitation / recreation </li>
  <li> 14: Outing response </li>
  <li> </li>
  <li> </li>
  <li> </li>
  <li> </li>
  <li> </li>
  <li> </li>
</ul>

## Data structure (not final)
### Training
In this challenge, participants are provided training data and test data. Training data contains accelerometer data from 12 subjects (2, 3, 4, 5, 6, 7, 9, 12, 17, 19, 21, and 22) and the activity labels file, which was collected in May and June, 2018 (before June 18th). Test data contains the data of 12 subjects (same id with the train data), which was collected in June, 2018 (at 18th and afterward).

The provided training data folder includes the accelerometer data files of 12 subjects and the “label” folder, which contains “label_train.csv”.

In each accelerometer data file, we have 4 columns: datetime and 3 coordinates of the accelerometer data.

In the label file (“label.csv”), we have 12 columns: id (label id), user_id, role, activity_type_id, activity_type (name in japanese), activity_type_e (name in english), date, start time, finish time (of the activity), target_id (patients), target_role, activity2user_id. Participants should note that the start and finish time at the label_train file may differ from the datetime at the accelerometer file due to the different time zone.

<ul>
  <li>Field accelerometer data (6 subjects)</li>
  <li>Lab  accelerometer data (2 subjects)</li>
  <li>labels of field data</li>
  <li>labels of lab data</li>
</ul>

### Testing
This dataset was used in our previous work, titled “Integrating Activity Recognition and Nursing Care Records: The System, Deployment, and a Verification Study”. The authors of this work proposed a theory that extension of start and ending time of the activities can increase the prediction rate. The reason behind the theory is that many of the nurses provided the labels before or after completing an activity. In the paper they verified and proved this theory. Following the theory, in the test data the time is extended for both start and end of an activity for 20 minutes. As the time is extended, there are some overlaps for the activity labels for some samples. So, the submission of the participants will be evaluated per activity following the same test setting as the paper. The final score will be calculated by taking the prediction average of all the activities.

<ul>
  <li>Field accelerometer data (3 subjects) </li>
</ul>
--->
