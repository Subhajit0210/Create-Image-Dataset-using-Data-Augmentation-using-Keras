# Create-Image-Dataset-using-Data-Augmentation-using-Keras

## Table of Contents
- [Project Overview](#project-overview)
- [Dependencies](#dependencies)
- [Preparing the Save Location](#preparing-the-save-location)
- [Image Augmentation Configuration](#image-augmentation-configuration)
- [Data Collection](#data-collection)
- [Creating and Saving Augmented Samples](#creating-and-saving-augmented-samples)
- [Reference and Inspiration](#reference-and-inspiration)
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

## Creating and Saving Augmented Samples
It takes the original image and creates 20 slightly different versions of it by randomly rotating, shifting, zooming, and flipping it. It then saves these new versions into a folder called `preview_directory`. This helps you see how the image augmentation works.

## Reference and Inspiration
This repository is based on the concepts presented in the Keras blog post:
[Building powerful image classification models using very little data](https://blog.keras.io/building-powerful-image-classification-models-using-very-little-data.html)
The article demonstrates how to effectively train image classification models even with a small dataset by leveraging Keras' built-in data augmentation techniques. This repository applies those principles to show how image datasets can be created and expanded using augmentation, enabling better model performance and generalization in low-data scenarios.

## Usage
To run the project, follow these steps:
1. Clone the repository:
```bash
git clone https://github.com/yourusername/Face-Mask-Detection-using-CNN.git
```
2. Navigate to the project directory:
```bash
cd Face-Mask-Detection-using-CNN
```
4. Run the Jupyter notebook:
```bash
jupyter notebook Face_Mask_Detection_using_CNN.ipynb
```

## Contributing
Contributions are welcome! Please create a new branch for any changes and submit a pull request for review.
