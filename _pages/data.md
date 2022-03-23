---
layout: single
title: Data Description
permalink: /data/
date: 2021-07-26T00:00:00+09:00
---
The dataset was recorded in the Smart Life Care Unit of the Kyushu Institute of Technology in Japan. A motion capture system from Motion Analysis Company is used for this experiment. It has 29 body markers but in the challenge, we are opening only 13 body marker data. 4 subjects (men) in their 20's and 30's participated in this experiment. Each of the subjects is instructed to put three types of food in the bento box.

- [Download train and test data](https://ieee-dataport.org/competitions/bento-packaging-activity-recognition-challenge)

Here they were instructed to perform 5 different scenarios:

<iframe width="560" height="315" src="https://www.youtube-nocookie.com/embed/mQgCaCjC7fI" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

- Normal
- Forgot to put ingredients
- Failed to put ingredients
- Turn over bento-box and
- Fix/rearranging ingredients

Actions are done in two different patterns inward and outward. Participants were asked to repeat each work 5 times. 20 infrared cameras are used to track the markers. The three-dimensional position of each marker is recorded. The markers may be labeled incorrectly in some cases due to the complex setting.


- Length of each activity segment:  50~70 s.
- Position of the markers:

![Position of th markers](/bento2021/assets/images/marker_position.png)

- Frequency: 100Hz
- Preprocessing: No preprocessing method is applied to this data
- Training data format:

<style>
table,
thead,
tbody  {
    width: 100%;
}
thead tr {
    width: 100%;
}

th {
    width: 50%;
}
</style>

|Activity Name | Label Number in Training Data|
|:--:|:--:|
|Normal(inward)|1|
|normal(outward)|2|
|Forgot to put ingredients (inward)|3|
|Forgot to put ingredients (outward)|4|
|Failed to put ingredients(inward)|5|
|Failed to put ingredients(inward)|6|
|Turn over bento-box (inward)|7|
|Turn over bento-box (outward)|8|
|Fix/rearranging ingredients (inward)|9|
|Fix/rearranging ingredients (outward)|10|


- Testng data format: same as training data.
