---
layout: single
title: Bento Packaging Activity Recognition Challenge
permalink: /learn/
date: 2021-07-28T00:00:00+09:00
---

Human activity recognition (HAR) has a great impact on human-robot collaboration. With the betterment of lifestyle, it is getting harder to find human labor at a lower wage. This is a big problem for various industries where a big amount of workforce is required at a low wage. Robots can be a great solution for this problem if they can be used as an assistant for humans to do small tasks. To do so the robot needs to first understand what the human is doing! By keeping this in mind Bento Packaging Activity Recognition Data has been collected. Here subjects are asked to perform Bento-box packaging tasks. Though several datasets are available on cooking([abc cook2020](https://abc-research.github.io/cook2020/), [epic kitchens](https://epic-kitchens.github.io/2021)) and daily living data([activity net](http://activity-net.org/index.html)), this type of industrial activity data set is very hard to find. Cooking needs to follow a step-by-step workflow like Bento packing-which is another good place to implement human-robot collaboration but there are a lot of differences between these two types. While cooking the steps and ingredients used in the food solely depends on the user but during packing a bento you need to put the items the company asked you to do. So, it is very common to forget to put an ingredient and forget to notice, or sometimes when you notice the box is far away in the conveyor belt and if you hustle to put you might mess up the whole thing. Instances like this are very common in Bento-making companies which creates a lot of trouble. To help in this scenario a robot hand can be a perfect assistant but for that, it needs to know what the human is doing and if he has made any mistake, and what type of mistake has been made. Also recognizing these steps can be used for care quality assessment and for ensuring that safety protocols have been followed to avoid the human-robot collision.

Also, in current activity recognition systems it does not matter where you need to put the ingredients but during Bento packing it is very important to identify on which side of the conveyor belt the bento is. Depending on this we have divided activities into inside and outside activity. You can easily identify the position if it is happening inside or outside but their combined recognition to decide which activity is happening is critical for analysis. Therefore, in this challenge, we aim at the recognition of the inside-outside activities and main activities taking place during bento packing sessions.

## Challenge Goal
The goal of the Bento Packaging Activity Recognition Challenge is to distinguish activities taking place during each segment based on the motion data collected with motion capture sensors while performing Bento-box packaging tasks ([Read data description](/bento2021/data/)). In the training dataset, we have provided data about 3 subjects along with all activity labels. In the test dataset unlabeled data of the remaining subject has been given. Participants have to submit their predicted activity labels on the test dataset using their models.

- [Registration is opening now.](/bento2021/registration/)
- [To understand the dataset more clearly](/bento2021/data/).

The training dataset contains data about 3 subjects and contains all activity labels.
The test dataset contains data about the other subject and is not labeled.
Participants must submit their predicted macro and micro activities on the test dataset using their models.


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

