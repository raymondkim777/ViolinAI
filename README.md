# ViolinAI

## Aim
During 10th and 11th grade, I volunteered in Sunhak Social Welfare Center, a local daycare center at Songdo, where I, alongside other students, taught violin (and other instruments) to children from low-income households. Those children were too poor to afford lessons, let alone an instrument, and us volunteers didn’t want their financial situations to hold them back from experiencing and enjoying music. 

However, I soon realized a problem. We had left a few school instruments in the welfare center for the students to be able to practice in their own time. However, whenever I gave lessons, I noticed the children would play the music differently from how I taught before. With no experience with dynamics, tempo, or rhythm, they would play some bars too loud or quiet, speed up or slow down based on the passage difficulty, or misread certain rhythm sections. This was because of their practice sessions; without any guidance, they didn’t know whether their way of playing was correct, and felt lost. It is crucial that a beginning student has constant teacher guidance in order to get used to reading and performing music, but our volunteering schedule of one lesson every two weeks just wasn’t enough. 

I hence decided to create a program that could instead do it for me. A teacher/volunteer couldn’t be present every day to help the students in their practice, but a computer program could. I created an AI program to receive an audio file of the student’s performance and evaluate it with spectrogram analysis to categorize the performance into three tiers – low, mid, and high.

## Dataset
I decided to limit the musical pieces my AI would analyze to the piece I was currently teaching my students: Dvořák’s Humoresque. Working closely with my violin teacher, who alone taught many students of different skill levels and also had many musical friends/relatives who were also teachers, as well as Ilsan Youth Orchestra (where I was a member), we collected recordings from 98 different individuals on their takes of the piece, with at least 30 of each tier (low, mid, high) for both pieces. The audio files’ format was converted from .m4a to .wav. I was going to use 80 random recordings to train the data, 8 for validation, and 10 for testing. 

<figure class="image">
  <img src="https://github.com/user-attachments/assets/70d8c27e-fe9e-4628-9695-f2ee2ed90fe8">
  <figcaption>Figure 0.1 The “mid” file with 31 mid-tier audio files</figcaption>
</figure>



