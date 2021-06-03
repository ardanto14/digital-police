# DigitalPolice
DigitalPolice is B21-CAP0081 capstone project for Bangkit 2021 program. The product is an android application to receive alert notification from our machine learning model that is trained to detect anomaly in surveillance camera video. The detected anomaly is indicated as a crime, in which for our project we use these type of crimes: Robbery, Vandalism, Stealing, and Assault.

This github repository containing the code for Machine Learning implementation, consists of:
- sources for C3D pretrained model, misc, dataset and cited paper.
- Data preprocessing steps by extracting features from raw dataset in a notebook
- Building and training model steps in a notebook

## Sources

### Cited Paper: 
Sultani, W., Chen, C., Shah, Mubarok. (2018). Real-World Anomaly Detection in Surveillance Videos. University of Central Florida. Can be accessed through https://openaccess.thecvf.com/content_cvpr_2018/papers/Sultani_Real-World_Anomaly_Detection_CVPR_2018_paper.pdf

### Source Dataset: 
https://www.crcv.ucf.edu/research/real-world-anomaly-detection-in-surveillance-videos/

### Source C3D : 
https://github.com/adamcasson/c3d

### Source Misc :
https://github.com/rajanjitenpatel/C3D_feature_extraction

## Machine Learning implementation steps
1. from the raw dataset, extract the features following the steps in feature-extraction.ipynb. the output of the extracted features is stored at our GCP Bucket in form of .txt files from .mp4 dataset
2. before building the model, split the anomaly dataset (that has been extracted) into training and testing as it is not splitted from the raw dataset
3. after splitting the dataset, build the CNN model and use the extracted features as the input in 4096 shapes
4. analyzing the result to find the proper model to use
5. test the model result in the test ground
6. steps 2 until 5 can be found in DP-building-model.ipynb file 


