# MoNuSAC2020challenge_project
## Convolutional Neural Network for Multi-Organ Nuclei Segmentation and Classification
The following codes are a first attempt at developing an algorithm to recognize different cell-types from the tissue image. 

### Resources

* [MoNuSAC grand-challenge](https://monusac-2020.grand-challenge.org/)
* [Original dataset to download](https://drive.google.com/file/d/1lxMZaAPSpEHLSxGA9KKMt_r-4S8dwLhq/view)

### Dataset

* `MoNuSAC_images_and_annotations` : original dataset which has patient's whole slide images (WSI) and ground truth. (Given by challenge organizers) [in the code is rename `dataset`]
* `MoNuSAC_masks` : contains binary masks generated from `1_image_and_mask.ipynb`.
* `dataframe_1` : contains all raw images and the ground truth masks.
* `dataframe_2` : 80/20 train-val split from `dataframe_1`.

### Getting started

1. Define the folder in which save all the dataset [in this code `PROGETTO`]
2. Put `MoNuSAC_images_and_annotations` in `PROGETTO` folder
3. Run `1_image_and_mask.ipynb`. You should get the MoNuSAC_masks folder in `PROGETTO`
4. Run `2_data_process.ipynb` to get raw images and their ground truth masks in `dataframe_1`. 
5. Run `3_cell_counting.ipynb` to count cell by type in each image and store in an excel file saved in `PROGETTO`
6. Run `4_train.iynb` to get the 80/20 split `dataframe_2`, train *UNet* on `dataframe_2`and obtain the predicted mask.
