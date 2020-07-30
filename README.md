# auto_crossy_road :rooster:

I'm training an AI to play "crossy road" the computer game with CNN. 

<img src="./demo/crossy.jpg" width="500">

Inspired by sentdex's GTA V project (link at the bottom).

## Table of Contents

* [Getting started](#getting-started)
* [Collecting data](#collecting-data)
* [Preparing data](#preparing-data)
* [Training model](#training-model)
* [Running model](#running-model)
* [Usage](#usage)
* [Links](#links)

## Getting started

When playing "crossy road", there are 5 possible actions that can be taken by our main character depending on the situation: 

| Action        | Keyboard action           | Situation
-----------------------------------------------------------------------------------------------------------------------------------
| move forward  | press 'w' on keyboard     | Open lane ahead, no risk of getting hit by car & has a safe landing space
| move left     | press 'a' on keyboard     | Got blocked by obstacle or has a car coming from the right
| move backward | press 's' on keyboard     | Got blcoked by obstacle or has a car coming from the left
| move right    | press 'd' on keyboard     | Neither the current position nor the position is ahead is safe
| stay          | press nothing on keyboard | The current position is safe and the charater is waiting for the car ahead to pass

Therefore, the main idea of this project is to first get a lot of screenshots during gameplay, with information recording about each screenshot's related action, then use that to train a CNN model that output categorical value. And during actually run, just grab the screen as frequent as possible while running the model, outputing the predicting into the game and help our chicken navigate through the map. 

## Collecting data

As the name suggests, the code in 'grab_data' takes care of the part where all the training datas are collected. The code's default running environment should be a working 'crossy road' app running on the top left corner, windowed, at 699 * 1280. The code will grab a snapshot of resolution 666 * 1280 (-33 in x-axis to get rid of the title bar) about 10 times per second and processes it a little bit before saving each coresponding folder related to the action linked to the image, within the '/data' folder under the current working directory. This code also offers a functionality that allows you to clear all saved images under '/data', with all folders indicating motions untouched. 

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

## Preparing data

Since duration of the animation of each move may vary depending on the interval between keys pressed, and the animation time is possible to be shorter than the time between which screenshot is taken, the recorded keypresses can't 100% be in sync with the screenshot of the gameplay we token. For example, during a move forward animation, since the character is still moving, we shouldn't be pressing on the 'w', but the lane ahead of the character is open, so for just that particular instance, the model should predict 'w' since the lane is open ahead. Therefore, to make sure the model can get as accuate as possible, I decided to manually go through the data, but only in the 'nop' folder, since most of the unsync situation occurs during animation and at that time no keypresses was needed. 

## Training model

// Under construction

## Running model

// Under construction

## Usage

// Under construction

## Links

* [Crossy Road offical website](https://www.crossyroad.com/)
* [Sentdex's gta project](https://github.com/Sentdex/pygta5)
