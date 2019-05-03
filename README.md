# OpenImages_CustomDataset
A data preprocessing script for creating your own custom dataset out of OpenImagesDB

[OpenImages](https://storage.googleapis.com/openimages/web/index.html) is an extensive dataset made by google. I have arranged this simple script for those interested in assembling your own dataset, as a subset from OpenImages. As default, I use a subset called BodyParts (BP), but the classes, the split of train/test images, can easily be switched out for what you want.

1- Download [train-annotations-bbox.csv](https://storage.googleapis.com/openimages/2018_04/train/train-annotations-bbox.csv) into this repository

2- Edit the Jupyter Notebook script's parameters to suit your needs

3- Run the script

Assuming you use the default parameters, you'll end with your directories and files looking like this:

- Object_Detection_DataPreprocessing.ipynb
- train-annotations-bbox.csv
- train-images-boxable.csv
- class-descriptions-boxable2.csv
- BP
  - classCSVs
    - arm_img_url.csv
    - beard_img_url.csv
    - ...
  - data
    - arm
      - (arm images)
    - beard
      - (beard images)
    - ...
  - test
    - (test images)
  - train
    - (train images)
  - annotations.txt
  - test.csv
  - train.csv
  
annotations.txt is what you will want to use for training your model(s) on the custom dataset. These annotations are in the format `(img_name, x1, y1, x2, y2, label)` which are more acessible for training.

Credit to [RockyXu66](https://github.com/RockyXu66)'s work on his [Faster RCNN](https://github.com/RockyXu66/Faster_RCNN_for_Open_Images_Dataset_Keras) repo for Open Images in which this script is based on.
