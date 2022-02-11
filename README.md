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

This TinyML application runs two NN back to back. One is for person detection through its inbuilt microphone input. Once a person is identified by the first NN, it triggers the next bigger NN which takes its input from the camera module and runs a NN and predicts if the person is masked or not.

## Constraints and Challanges
**Dataset** <br>
Creating a model that is generic enough to works for all sections of the society requires an enourmous amount of data. Since this application involves both the audio and visual aspects, it requires enormous amounts of audio and visual data. <br>

**Memory** <br>
Since this is a TinyML application, memory is a big constraint. Hence it becomes difficult to store and process high dimensional coloured input feeds coming in from the camera module. Moreover since we are running two NN for inferencing, it presents an additional challange on the memory of the MCU. <br>

**Model** <br>
Even if we have great datasets spanning across all the sections of the society and excellent models to make predictions, due to the memory constraints imposed by the MCU, it becomes almost impossible to use those models on our MCU. Hence we have a fixed subset of small models that could be used with our MCU. <br>

## Demo

## Images

## Specifications of the project

### Dataset

**Audio Dataset** <br>
The audio dataset consists of audio samples of length 2 sec recorded by me uttering the keyword 'Alexa'. It also contains audio samples from the publicly available Pete's Keyword Spotting Dataset for unknown and background noise data. <br>

**Image Dataset** <br>
The image dataset consists of images of myself captured using the OV7670 camera module under 2 classes (i.e masked and unmasked). <br>

### Model

**Audio Model**<br>
Tiny_Conv model trained on the Spectogram of the microphone input. <br>

**Image Model** <br>
MobileNetV1 trained on the 96x96 Grayscale images. <br>

## Try this project out

### Hardware Requirements
* Arduino Nano 33 BLE Sense with headers
* Solderless breadboard
* USB cable
* 0V7670 camera module
* M-M , M-F jumper wires
* LEDs

### Software Requirements
* [Arduino](https://www.arduino.cc/en/software) IDE for you OS

### Steps
* Clone this project 

```
git clone https://github.com/suburban-daredevil/Smart-Mask-Enforcement-System.git

```

* Open `Smart-Mask-Enforcement-System.ino` on the Arduino IDE
* Connect the board to the computer
* Ensure the board and port are set
* Hit deploy

## Disclaimer

Since this model operates on an extremely low powered and memory constrained MCU, there are chances of occasional occurences of False positives and False negatives. Further improvements on the dataset and model is required to make the model more generalisable before real world deployment. <br>
