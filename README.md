# Create-Image-Dataset-using-Data-Augmentation-using-Keras

## Table of Contents
- [Project Overview](#project-overview)
- [Dependencies](#dependencies)
- [Data Collection](#data-collection)
- [Directory Management](#directory-management)
- [Image Augmentation Configuration](#image-augmentation-configuration)
- [Results and Insights](#results-and-insights)
- [Usage](#usage)
- [Contributing](#contributing)

## Project Overview
The project takes an input image (`dog_or_cat_1.jpg`) and applies various random transformations (rotation, shifting, shearing, zooming, flipping) to generate augmented versions of the image. The augmented images are saved to a directory named `preview_directory`.

## Dependencies
The following libraries are required to run this project:
- Python 3
- TensorFlow

## Data Collection
This project is a demonstration of image augmentation and uses a single example image (`dog_or_cat_1.jpg`) for illustrative purposes.

## Directory Management

This section of the code handles creating and managing the directory where the augmented images will be saved.

*   `os.getcwd()`: Retrieves the script's current working directory. This ensures that the output directory is created relative to the location where the script is executed.
*   `os.path.join(current_directory, 'preview_directory')`: Constructs the full path to the `preview_directory`. Using `os.path.join` is platform-independent and ensures that the path is correctly formatted regardless of the operating system.
*   `os.path.exists(preview_directory)` and `os.makedirs(preview_directory)`: These lines check if the `preview_directory` already exists. If it does not, `os.makedirs` creates the directory. The `exist_ok=True` parameter (implicitly used by the `if not os.path.exists` check before `os.makedirs`) would prevent an error if the directory already exists, making the script robust. This ensures that the script can be run multiple times without encountering errors due to the directory already being present.

This robust directory management ensures that the augmented images are saved in a designated location within the project structure, making it easy to access and review the generated output.

## Image Augmentation Configuration

This section defines the `ImageDataGenerator` object, which is central to the image augmentation process. The `ImageDataGenerator` is configured with various parameters to control the types and degrees of random transformations applied to the input images.

*   `rotation_range`: Specifies the range (in degrees) within which to randomly rotate images. A value of 40 means images can be rotated by up to 40 degrees clockwise or counter-clockwise.
*   `width_shift_range` and `height_shift_range`: These parameters define the range within which to randomly translate (shift) images horizontally and vertically, respectively. A value of 0.2 means the image can be shifted by up to 20% of its width or height.
*   `shear_range`: Determines the range for applying random shearing transformations. Shearing slants the image along an axis. A value of 0.2 indicates the degree of shear to be applied.
*   `zoom_range`: Controls the range for random zooming. A value of 0.2 means the image can be randomly zoomed in or out by up to 20%.
*   `horizontal_flip`: When set to `True`, the image can be randomly flipped horizontally. This is a common augmentation technique.
*   `fill_mode`: Specifies the strategy used to fill in newly created pixels that appear after a transformation (like rotation or shifting). `'nearest'` fills the new pixels with the nearest available pixel value.

These parameters are set to introduce controlled variations into the image data, helping to increase the size and diversity of the training dataset (if this were used for model training) and potentially improve model generalization. You can adjust these parameters to experiment with different augmentation strategies.







Keras Blog: https://blog.keras.io/building-powerful-image-classification-models-using-very-little-data.html
