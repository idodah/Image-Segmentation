# Image-Segmentation

In this assignment i used detectron2 in order to remove sky from a coco dataset images. To do that I cropped the image
from the lowest pixel that has sky to the highest. In order to do this assignment i used Google Colab. 

## The dataset- Quickstart Geo
A small dataset with geolocation data.
The dataset consists of 500 images from the validation split of the BDD100K dataset in the New York City area with object detections and GPS timestamps.
Dataset size: 33.50 MB

I used this dataset because most of it's photos has sky on them and the images were taken from different times in the day.
This dataset can be downloaded using fiftyone package that has many prepared datasets with different topics.

## The process
1. loading the dataset from fiftyone package.
2. Read every image.
3. Apply panoptic segmentation on each image. Panoptic segmentation will split the image to different segments including sky.
4. Get the id's of the sky segments from the image.
5. Get the lowest pixel of the sky segments in the image.
6. Crop the image by changing it's height.
7. Apply instance segmentation on the new cropped image.
8. Save the cropped and segmented image in the google colab workspace.
9. Get the image metadata and annotations from the json file. 
10. Save each image metadata and annotations in a new json file.
11. Get the paths of the cropped and segmented images from the new json file.
12. Print all the images.
