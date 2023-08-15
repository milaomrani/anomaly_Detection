# Anomaly Detection Using AutoEncoder
Overview
This repository contains the implementation of two AutoEncoder models for anomaly detection in carpet images. The AutoEncoder(s) are trained to learn the normal patterns within the images, and it can detect anomalies by reconstructing the input and measuring the reconstruction error.

## Dataset
The dataset consists of two main categories of carpet images taken from MVTec:

Normal Images: These images represent the standard pattern without any anomalies.
Anomalous Images: These images contain anomalies that deviate from the normal pattern.

### Methodology
AutoEncoder Architecture: The AutoEncoder is a neural network that consists of two main parts:

Encoder: Compresses the input into a latent-space representation. It encodes the input image as an internal fixed-size representation in reduced dimensionality.
Decoder: Maps the encoded data back to the original data space. The decoder reconstructs the input data from the internal representation.

Anomaly Detection: Anomalies are detected by calculating the reconstruction error between the original image and the reconstructed image. A higher reconstruction error indicates an anomaly.


Training: The AutoEncoder is trained on normal images to learn the standard pattern.
Reconstruction: The trained AutoEncoder reconstructs both normal and anomalous images.
Error Calculation: The reconstruction error is calculated using a metric such as Mean Squared Error (MSE).
Thresholding: A threshold is set to classify an image as anomalous if the reconstruction error is above a certain level.
Results
The following images showcase the anomalies detected by the AutoEncoder:
Original Image: Description of the original image.
Reconstructed Image: Description of the reconstructed image.

### Threshold
<img src="Images\thresh.png" alt="Image 3" width="360"/>

### Image Rresult after 100 training epoch
<img src="Images\ae1.png" alt="Image 2" width="520"/>

<img src="Images\2_1.png" alt="Image 1" width="260"/> <img src="Images\2_2.png" alt="Image 2" width="260"/>

<img src="Images\3_1.png" alt="Image 1" width="260"/> <img src="Images\3_3.png" alt="Image 2" width="260"/>


### Conclusion ###
This project demonstrates the effectiveness of using AutoEncoders for anomaly detection in images. The model successfully identifies the anomalies and provides insights into the underlying patterns.
