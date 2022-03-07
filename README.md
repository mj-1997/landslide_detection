# Landslide detection
Landslide detection and segmentation based on Sentinel-1 imagery using deep learning models. 

Each folder contains one or a few notebooks and a readme file describing what is in the Notebook. This readme file will give an overview on how to use all Notebooks.

First images from google earth engine are produced and exported to the local Google Drive
, as tiff files. This is done in nb_export_gee_images. These images will be forming the base of the dataset on which models are trained for landslide detection.

Then the tiff files are converted to tfrecords files. Subsequently they are uploaded to Kaggle,
such that they can be used as a cloud file, which enables fast training. The conversion to tfrecords, and some post processing is done in nb_make_tfrecords.

Then either a conditional Generative Adversarial Network (cGAN) can be used, which is described and implemented in nb_cgan  or a U-Net which is described and implemented in
nb_unet.

Finally the results of the cGAN can be done via nb_validate_results. The results of the U-Net are foud in nb_unet. nb_validate_results also visualizes some images before training, to verify the quality of the images data sets.

Tfrecords used can be found under https://www.kaggle.com/marjamachielse.

