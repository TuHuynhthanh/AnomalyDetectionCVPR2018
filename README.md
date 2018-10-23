We tested code on **(https://github.com/WaqasSultani/AnomalyDetectionCVPR2018)** and edited code to run on PyQt5 in Demo_GUI.py file .


The implementation is tested using Python virtual enviroment:

- Keras version 1.1.0 
- Theano 1.0.2
- Python 3.6
- Ubuntu 18.04

Install requirements: ```python pip install -r requirement.txt```
Using Theano backend, edit **keras.json** file in **~/.keras/keras.json** with contents:
```
{
    "epsilon": 1e-07,
    "backend": "theano",
    "floatx": "float32",
    "image_data_format": "channels_last"
}
```
We used C3D-v1.0 (https://github.com/facebook/C3D) with default settings as a feature extractor.
 
Training_AnomalyDetecor_public.py is to Train Anomaly Detection Model


Testing_Anomaly_Detector_public.py is to test trained Anomaly Detection Model


Save_C3DFeatures_32Segments is to save already computed C3D features for the whole video into 32 segment features.


weights_L1L2.mat: It contains the pre-trained weights for the model ‘model.json’.

Demo_GUI: We have provided a simple GUI which can be used to see results of our approach on sample videos.

SampleVideos: This folder contains C3D features (32 segments) for sample videos. It order to see testing results for the features in this folder, please copy the corrosponding videos in the same folder.


Plot_All_ROC:  This code can be use to plot the ROC results reported in the paper. The data to plot ROCs of methods discussed in the paper can be found in folder Paper_Results.


The project page and UCF-Crimes dataset can be found at: http://crcv.ucf.edu/projects/real-world/


The dataset can be also downloaded from the dropbox link given here:
https://webpages.uncc.edu/cchen62/dataset.html
