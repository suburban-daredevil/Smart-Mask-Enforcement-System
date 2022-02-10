# Smart Mask Enforcement System using TinyML

## Introduction

Masks are one of the two primary weapons that we have against the unwanted neighbour of ours (of course the COVID-19 virus). We all know the importance of wearing masks in public places <br>

Presenting to you - Smart Mask Enforcement System <br>

This is a TinyML application which intelligently predicts whether you are present or not using the input it recieves through its inbuilt microphone and then predicts whether you are masked or not through the input it recieves through its camera module (the OV7670 camera module) <br>

## Demo

## Images

## Details
### Dataset
#### Image Dataset
For the image dataset, I had capurted images of myself using the OV7670 camera model under 2 classes (i.e masked and unmasked)
#### Audio Dataset
For the audio dataset, I had recorded 2 sec long audio samples of myself uttering the word 'Alexa'. I had also added audio samples from the Pete's Keyword Spotting Dataset for unknown and background noise data
### Model
#### Image Model
Tiny_Conv model trained on the Spectogram of the microphone input
#### Audio Model
MoobileNetV1 for trained on the 96x96 Grayscale images
## Try this project
