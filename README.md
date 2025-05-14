# Create-Image-Dataset-using-Data-Augmentation-using-Keras

## Table of Contents
- [Project Overview](#project-overview)
- [Dependencies](#dependencies)
- [Preparing the Save Location](#preparing-the-save-location)
- [Image Augmentation Configuration](#image-augmentation-configuration)
- [Data Collection](#data-collection)
- [Creating & Saving Augmented Samples](#creating-&-saving-augmented-samples)
- [Usage](#usage)
- [Contributing](#contributing)

## Project Overview
The project takes an input image (`dog_or_cat_1.jpg`) and applies various random transformations (rotation, shifting, shearing, zooming, flipping) to generate augmented versions of the image. The augmented images are saved to a directory named `preview_directory`.

## Dependencies
The following libraries are required to run this project:
- Python 3
- TensorFlow

## Preparing the Save Location
Checks where the script is running and then creates a new folder named `preview_directory` there. If the folder already exists, it just moves on. This is done to make sure there's a place to save the new augmented images.

## Image Augmentation Configuration
Tells the tool how to randomly change your images later on. Giving it instructions like: "sometimes rotate the image," "sometimes shift it a bit," "sometimes zoom in or out," and "sometimes flip it horizontally." These instructions are based on the numbers and True/False settings which are mentioned there.

## Data Collection
This project is a demonstration of image augmentation and uses a single example image (`dog_or_cat_1.jpg`) for illustrative purposes.

## Creating & Saving Augmented Samples
It takes the original image and creates 20 slightly different versions of it by randomly rotating, shifting, zooming, and flipping it. It then saves these new versions into a folder called `preview_directory`. This helps you see how the image augmentation works.

Keras Blog: https://blog.keras.io/building-powerful-image-classification-models-using-very-little-data.html
