# ViolinAI

This program receives an audio file of a violin performance of Dvořák’s Humoresque and evaluates it with a convolutionary neural network via spectrogram analysis to categorize the performance into three tiers – low, mid, and high.

## Periods of Development  
- August 14, 2021 - September 19, 2021

## Development Environment  
- 'Python 3.10'

Libraries used: Keras (TensorFlow), NumPy, seaborn
- Keras: Library used to develop CNN model
- NumPy: Library used for data analysis
- seaborn: Library used to generate confusion matrix

## Aim

During highschool 10th and 11th grade, I volunteered in Sunhak Social Welfare Center, a local daycare center at Songdo, where I, alongside other students, taught violin (and other instruments) to children from low-income households. Those children were too poor to afford lessons, let alone an instrument, and us volunteers didn’t want their financial situations to hold them back from experiencing and enjoying music. 

The school allowed us to leave a few school instruments in the welfare center for the students to be able to practice in their own time. However, each lesson I would notice the children played the music differently from last class. With no experience with dynamics, tempo, or rhythm, they would play some bars too loud or quiet, speed up or slow down based on the passage difficulty, or misread certain rhythm sections. This was due to lack of guidance during their practice sessions,where they didn’t know whether their way of playing was correct and developed bad habits. It is crucial for a beginner to receive consistent guidance in order to get used to reading/performing music, which my volunteering schedule of one lesson every two weeks did not allow. Thus I developed a program to provide rudimentary guidance in my absence. 

## Dataset

The input performance was limited to one piece: Dvořák’s Humoresque. This was partly due to it being the piece I was currently teaching, and because of the limitations of data collection. I requested the help of my violin teacher, who had access to numerous students of varying skill levels through her own students and her musical friends/relatives, and throug her Ilsan Youth Orchestra. Together we collected recordings from 98 different individuals on their takes of Dvořák’s Humoresque in .wav format for lossless audio, with at least 30 of each tier (low, mid, high). 80 recordings would be used for training, 8 for validating, and 10 for testing. 

<figure class="image">
  <img src="https://github.com/user-attachments/assets/70d8c27e-fe9e-4628-9695-f2ee2ed90fe8">
  <figcaption>Figure 0.1 The “mid” file with 31 mid-tier audio files</figcaption>
</figure>

## Core Features  
