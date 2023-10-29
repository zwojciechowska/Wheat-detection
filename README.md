# Dataset Description
My project uses the data from Global Wheat Detection from Kaggle: <a href=https://www.kaggle.com/competitions/global-wheat-detection/data>Global Wheat Detection</a>
The data is images of wheat fields, with bounding boxes for each identified wheat head. Not all images include wheat heads / bounding boxes. The images were recorded in many locations around the world.

The CSV data is simple - the image ID matches up with the filename of a given image, and the width and height of the image are included, along with a bounding box. 
There is a row in train.csv for each bounding box. Not all images have bounding boxes.

The project is about predicting bounding boxes around each wheat head in images that have them using the YOLOv5 pre-trained model.

# Requirements
This project uses:
- numpy
- pandas
- matplotlib
- scikit-learn
- pytorch
- torchvision

Before use make sure you have a `kaggle.json` file which contains your API token in order to download the dataset from Kaggle.


The following steps were performed:

1. Data review, convertion to pandas dataframes 
2. Check for missing data
3. Images preview
4. Data preparation before using it in the model training
5. Models training - 3 variants of YOLOv5 model were used: YOLOv5s, YOLOv5m, YOLOv5x
6. All models were saved and can be used to predict wheat heads on images.


# Usage

The `user_interface.ipynb` file allows to detect wheat heads on images using 3 trained models.