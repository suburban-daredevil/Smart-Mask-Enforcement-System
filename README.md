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
Images of myself captured using the OV7670 camera module under 2 classes (i.e masked and unmasked)
#### Audio Dataset
Audio samples of length 2 sec recorded by me uttering of the keyword 'Alexa'. Also added audio samples Pete's Keyword Spotting Dataset for unknown and background noise data
### Model
#### Image Model
Tiny_Conv model trained on the Spectogram of the microphone input
#### Audio Model
MobileNetV1 trained on the 96x96 Grayscale images
## Try this project
