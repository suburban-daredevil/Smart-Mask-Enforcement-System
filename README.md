# Smart Mask Enforcement System using TinyML

## Table of contents
* [Purpose of the project](#Purpose-of-the-project)
* [Description of the project](#Description-of-the-project)
* [Constraints and Challanges](#Constraints-and-Challanges)
* [Demo](#Demo)
* [Images](#Images)
* [Specification of the project](#Specification-of-the-project)
* [Try this project out](#Try-this-project-out)
* [Disclaimer](#Disclaimer)

## Purpose of the project

Masks are one of the two primary weapons that we have against the unwanted neighbour of ours (of course the COVID-19 virus). Scientifically, proper mask wearing can protect us from the virus and also prevent the spread of the virus. We all know the importance of wearing masks in public places. Even then, it becomes difficult for Governments to implement proper mask wearing in public places. This project aims at solving that issue. <br>

## Description of the project

Imagine a system present at door of offices, schools, closed public places and other potential areas where it allows people inside only if they are masked. They are not allowed if they are unmasked.

Presenting to you - **Smart Mask Enforcement System** <br>

This is a TinyML application which operates on the MultiTenant Cascading architecture. This TinyML application intelligently predicts whether you are present or not using the input it recieves through its inbuilt microphone and then predicts whether you are masked or not through the input it recieves through its camera module (the OV7670 camera module) and actuates appropriate responses. <br>

## Constraints and Challanges
**Dataset** <br>
Creating a model that is generic enough to works for all sections of the society requires an enourmous amount of data. Since this application involves both the audio and visual aspects, it requires enormous amounts of audio and visual data. <br>

**Memory** <br>
Since this is a TinyML application, memory is a big constraint. Hence it becomes difficult to store and process high dimensional coloured input feeds coming in from the camera module. Moreover since we are running two NN for inferencing, it presents an additional challange on the memory of the MCU. <br.

## Demo

## Images

## Specifications of the project

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

## Try this project out

## Disclaimer
