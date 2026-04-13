# Friction(less) - BSc Electronic Music, Computing and Technology 2025 - Final Project by Christopher Lilleorg

Goldsmiths, University of London

Instructed by Charles Hutchins

Student ID: 33772935

Date: June 2nd, 2025


# Project Overview


Friction(less) is an audiovisual touch-interactive magic mirror that allows the user to generate dream-like sounds and images by drawing on the screen. 

This project aims to research the affective, haptic and psychoacoustic properties of tactile visual feedback and immersive sound design techniques used in modern touchscreen devices to create new methods of digital mythmaking.

The project consists of an immersive audiovisual experience that is interactable via a large touchscreen interface. Drawing on the screen controls an audio-reactive brush used as an image prompt to generate AI images in real time. The touchscreen input also controls a neural network powered granular synthesiser which responds to finger movements and provides tactile sonic feedback, creating the illusion of materiality. A harmonic drone provides background ambience throughout the experience, designed to utilize the psychoacoustic and emotionally affective properties of sound to create a state of deep focus and meditation.

This project integrates Max/MSP with the FluCoMa and ODOT packages for audio synthesis, and TouchDesigner with the custom StreamDiffusionTD component by DotSimulate for the visuals. Data is sent between Max and TouchDesigner via OSC messages.

The installation is normally controlled with a touchscreen interface, but the code for this version has been adjusted to enable mouse controls.


# Project Report

[Friction(less): Exploring digital mythmaking, psychoacoustics and ethical AI art with a magic mirror](https://github.com/user-attachments/files/26678047/Friction.less._Final_Project_Report-1.pdf)



# Video Documentation

[Friction(less) demo 1](https://youtube.com/shorts/iQ6FExcTmnY?feature=share) 

[Friction(less) demo 2](https://youtube.com/shorts/QzwLYErVDXo?feature=share)

These were filmed during the 2025 Goldsmiths Music Computing BA degree show.


# Software & Libraries

[Max/MSP](https://cycling74.com)

[FluCoMa](https://cycling74.com/packages/fluidcorpusmanipulation) package for Max/MSP

[ODOT](https://cycling74.com/packages/odot) package for Max/MSP

[TouchDesigner](https://derivative.ca/)

[StreamDiffusionTD](https://www.patreon.com/posts/streamdiffusiont-122151622) custom component by DotSimulate (Requires NVIDIA GPU, CUDA 12.8, and Python 3.10.6)

[SD-Turbo](https://huggingface.co/stabilityai/sd-turbo) as the base diffusion model for StreamDiffusionTD

[camroll_LoRa](https://drive.google.com/file/d/1-4jrxpGijo_yXnG-TMdL8scdss4ZPMww/view?usp=sharing) as the custom-trained LoRa fine-tuning model for StreamDiffusionTD

[CUDA 12.8](https://developer.nvidia.com/cuda-12-8-0-download-archive)

[Python 3.10.6](https://www.python.org/search/?q=3.10.6&submit=)



# Hardware Requirements

Windows 10 or 11

NVIDIA GPU (for CUDA support)

# Setup Instructions


## Audio Setup in Max/MSP and TouchDesigner

Connect the audio output from Max/MSP to the Audio Device In operator in TouchDesigner using an audio routing software (such as [VB-Audio Matrix](https://vb-audio.com/Matrix/) on Windows). 

Set the audio output device in the Audio Device Out operator to hear sound output.

## Load and Slice Samples in Max/MSP

Open the Max/MSP patch and connect the synthesizer to the path of the provided sample folder.

To load and slice the samples, click on the message box containing the file path.

Start the Drone2.flac file and set it to play on loop in Max/MSP.

## Visual Setup in TouchDesigner

Open the TouchDesigner project.

Set up the StreamDiffusionTD component as per the provided instructions by DotSimulate. Select sd-turbo as the base model and the provided custom LoRa as the fine-tuning model.

Click on the Window operator within the project file. Open the project in Presentation mode. 

## Interaction


Press 5 on the keyboard to start the introductory sequence and then use your mouse to click within the TouchDesigner window to begin drawing and generating real-time AI imagery and controlling the synthesiser. 


# Acknowledgements


FluCoMa – Developed by FluCoMa Team, providing a comprehensive framework for computational music analysis and composition. https://www.flucoma.org/

ODOT – Developed by Jack Armitage and David Bowden, offering a flexible environment for live coding and algorithmic composition in Max/MSP. https://odot.systems/

TouchDesigner – Created by Derivative, offering a node-based visual programming environment used for real-time interactive multimedia content. https://www.derivative.ca/

StreamDiffusionTD – Custom component by DotSimulate, used to generate AI imagery in real time within TouchDesigner. 
DotSimulate StreamDiffusionTD Component


# License

This project is for educational purposes and is not for commercial use. All third-party libraries and components are credited in the acknowledgements section.
