# ViolinAI

This program receives an audio file of a violin performance of Dvořák’s Humoresque and evaluates it with a convolutionary neural network via spectrogram analysis to categorize the performance into three tiers – low, mid, and high.

## Periods of Development  
- August 14, 2021 - September 19, 2021

## Development Environment  
- 'Python 3.10'

Libraries used: Keras (TensorFlow), NumPy, seaborn
- Keras: Library used to develop CNN model
- NumPy: Library used for data analysis
- seaborn: Library used to generate confusion matrix heatmap

## Aim

During highschool 10th and 11th grade, I volunteered in Sunhak Social Welfare Center, a local daycare center at Songdo, where I, alongside other students, taught violin (and other instruments) to children from low-income households. Those children were too poor to afford lessons, let alone an instrument, and us volunteers didn’t want their financial situations to hold them back from experiencing and enjoying music. 

The school allowed us to leave a few school instruments in the welfare center for the students to be able to practice in their own time. However, each lesson I would notice the children played the music differently from last class. With no experience with dynamics, tempo, or rhythm, they would play some bars too loud or quiet, speed up or slow down based on the passage difficulty, or misread certain rhythm sections. This was due to lack of guidance during their practice sessions,where they didn’t know whether their way of playing was correct and developed bad habits. It is crucial for a beginner to receive consistent guidance in order to get used to reading/performing music, which my volunteering schedule of one lesson every two weeks did not allow. Thus I developed a program to provide rudimentary guidance in my absence. 

## Dataset

The input performance was limited to one piece: Dvořák’s Humoresque. This was partly due to it being the piece I was currently teaching, and because of the limitations of data collection. I requested the help of my violin teacher, who had access to numerous students of varying skill levels through her own students and her musical friends/relatives, and through her Ilsan Youth Orchestra. Together we collected recordings from 98 different individuals on their takes of Dvořák’s Humoresque in WAV format for lossless audio, with at least 30 of each tier (low, mid, high). 80 recordings would be used for training, 8 for validating, and 10 for testing. 

![pic1](https://github.com/user-attachments/assets/f6ce5691-bff3-41f3-9960-b4583906656f)

*Figure 1. The “mid” file with 31 mid-tier audio files*

## Core Features 

### Spectrogram Generation from Audio

ML analysis of audio recordings can be reliably done by converting the audio file into a spectrogram, which is analyzed as an image via a convolutionary neural network. Audio processing methods provided by the TensorFlow library was utilized to pre-process the WAV audio files. The `decode_audio` function was used to normalize the 16000 hz mono-channel WAV file into a tensor of float32 and range [-1.0, 1.0], which was then cut to produce equal-length portions of each recording. This was then processed by a Short-Time Fourier Transform (STFT) function (`tf.signal.stft`). This converts the audio into its respective component frequencies while also preserving time information. (This is why regular Fourier transforms (`tf.signal.fft`) were not used.) The component frequencies are given in complex tensor values; however, as we only need the magnitude of the frequencies, an absolute value function was used to create both a waveform and a spectrogram for each audio file. 

![image](https://github.com/user-attachments/assets/946c4bbd-6518-4ac1-9f18-c8e8a25503a0)
*Figure 2. Example waveform and spectrogram plotted from audio file*

### Model (CNN)

### Training

### Results
