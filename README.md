# auto_crossy_road :hatching_chick:

I'm training an AI to play "crossy road" the computer game with CNN. 

<img src="./demo/crossy.jpg" width="500">

Inspired by sentdex's GTA V project (link at the bottom).

## Table of Contents

* [Getting started](#getting-started)
* [Training model](#training-model)
* [Running model](#running-model)
* [Usage](#usage)
* [Links](#links)

## Getting started

As the name suggests, the code in grab_data takes care of the part where all the training datas are collected. The code's default running environment should be a working 'crossy road' app running on the top left corner, windowed, at 666 * 1280. The code will grab a snapshot about 10 times per second and processes it a little bit before saving each coresponding folder related to the action linked to the image, within the '/data' folder under the current working directory. This code also offers a functionality that allows you to clear all saved images under '/data', with all folders indicating motions untouched. 

### More about image processing part:

* Here is a hand drawn image for coordinate reference:

  <img src="./demo/img4.JPG" width="500">

#### Detailed steps: 

1. The original screenshot taken of the game:

    <img src="./demo/1.jpg" width="500">

2. Grayscaling the image and zero padding the bottom to prepare for straightening the image:

    <img src="./demo/2.jpg" width="500">

3. ROI after getting rid of the irrelevant information in the image: 

    <img src="./demo/3.jpg" width="500">

4. Straighten the image to get rid of the black space: 

    <img src="./demo/4.jpg" width="500">

5. Resize the image to 50 x 50 before being fed into the model

    <img src="./demo/5.jpg" width="200">

## Training model

// Under construction

## Running model

// Under construction

## Usage

// Under construction

## Links

* [Crossy Road offical website](https://www.crossyroad.com/)
* [sentdex's gta project](https://github.com/Sentdex/pygta5)
