# Appendix-size-prediction
Bachelor Thesis Project - Faculty of Electrical Engineering, University of Sarajevo

## Description
This repository contains the code and experiments developed as part of my bachelor thesis, focused on predicting appendix size using CT scan images and corresponding technical parameters. The approach is based on multimodal deep learning models that combine visual and numerical data.

## Motivation
Accurate measurement of appendix size on CT scans is often challenging and can vary depending on the radiologist. The goal of this project is to evaluate whether an AI-based model can provide more consistent and reliable estimates.

## Methodology
The model uses a multimodal architecture that combines a convolutional neural network (ResNet-18) for feature extraction from CT images with a multilayer perceptron (MLP) for processing scan parameters (CTDI, kV, mA), with the extracted features combined to produce a continuous prediction of appendix size. The dataset consists of 360 CT images of a 3D-printed appendix phantom collected under different scanning conditions, with each image paired with its corresponding technical parameters. The model was trained and evaluated using multiple train/test splits as well as cross-validation.

## Results
The results indicate that the model is capable of learning the relationship between image features and scan parameters to estimate appendix size. The best performance was achieved for the 80/20 and 60/40 train/test splits, suggesting that the model benefits from increased data availability. Across different experiments, the model produced stable and consistent predictions, and in several cases, the predicted values were closer to reference measurements than those measured manually by radiologists, indicating reduced variability.

The table below shows a comparison of absolute errors between two radiologists and the model (for two best-performing configurations). The results demonstrate that the model achieves lower or comparable errors across most scan series.

<img src="https://github.com/user-attachments/assets/ae45bb93-df48-44cd-a125-1c2f71aafbd3" width="350">
