# Overview

The project aims to create an automated deep learning model leveraging CNN's (Convolutional Neural Networks) for the accurate classification of weather conditions from images. It focuses on identifying distinct weather categories such as cloudy, rain, shine, and sunrise. By employing advanced data preprocessing and augmentation techniques, the project seeks to standardize and enrich the dataset, thus improving the model's performance and reliability in recognizing diverse weather patterns. The dataset used is sourced from [Mendeley Data](https://data.mendeley.com/datasets/4drtyfjtfy/1).

# Repository Contents
- `dataset2.zip`: This compressed file contains a collection of weather images, organized in a folder. Each image is named according to the weather condition it represents, serving as a label.
- `Weather_Recognition.ipynb`: A Jupyter notebook that encompasses the complete code involved in the project.

# Methodology
- **Data Preparation**: Extracted images from `dataset2.zip` and organized them into a DataFrame with 'filename' and 'label' columns.
- **Visualization**: Analyzed class distributions and visualized images for each weather category.
- **Data Splitting**: Divided the dataset into 90% training, 5% validation, and 5% test sets.
- **Data Augmentation**: Used image data generators for training, validation, and testing sets.
- **Model Development**:
  - Calculated class weights for balanced learning.
  - Established helper functions for model compilation, training, evaluation, and result visualization.
  - Created three CNN architectures:
    1. Basic CNN 
    2. Multi-Layer CNN 
    3. CNN with Merge Layers 
       
# Installation and Usage
To set up the project, clone the repository, install dependencies, and navigate to the directory. Run Jupyter Notebook to view the project:
```bash
git clone https://github.com/Shanmukhi1920/Weather_Recognition
cd Weather_Recognition
pip install -r requirements.txt
jupyter notebook
```
Then, open `Weather_Recognition.ipynb` in Jupyter.

# Results

- **First Model (Basic CNN)**: Best at classifying 'cloudy' and 'shine'. Struggled with 'rain'. Test accuracy: 82.4%.
- **Second Model (Multi-Layer CNN)**: High accuracy across all classes, especially 'rain' and 'shine'. Test accuracy: 92%.
- **Third Model (CNN with Merge Layers)**: Good at 'shine','cloudy' and 'sunrise'.  Struggled with 'rain'. Test accuracy: 87%. 

The Multi-Layer CNN model demonstrated the highest overall accuracy and ability to discern between the classes.
