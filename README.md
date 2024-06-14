# Drone-based-geo-spatial-ML-for-crop-health-yield-assessment
## Problem Statement 
Vikram Farm, a sugarcane field in UP, is experiencing suboptimal yields compared to other sugarcane fields in the region. To address this issue, it is necessary to identify and analyze the varying nitrogen and water levels across the farm to find the nutrient (nitrogen) and stress levels contributing to the lower yields.
## Objective
The primary objective of our project is to enhance the sugarcane yield at Vikram Farm by implementing a classification system. Utilizing the drone-based data, we aim to segment the field into nine distinct classes defined by varying levels of nitrogen (low, medium, high) and water (low, medium, high).

<img src="https://github.com/saimaansi13/Drone-based-geo-spatial-ML-for-crop-health-yield-assessment/assets/125540201/7e96eeb4-76d7-4c58-bcb8-bae30561d9fb" width="300">

## Data Pipeline
### 1) Image Stitching
WebODM, a web extension of OpenDroneMap, served as a robust solution for our project. It allowed for optimal stitching across bands and enabled us to view various indices, such as NDVI for plant health. This capability was crucial as it enabled us to create a complete view of the field from fragmented drone images. By integrating this with the ground truth data from shapefiles, we were able to establish an efficient data pipeline.

<img src="https://github.com/saimaansi13/Drone-based-geo-spatial-ML-for-crop-health-yield-assessment/assets/125540201/9b32b05e-83c1-4562-ac4f-ad3855fa5a08" width="800">

### 2) Orthomosaic to chips
To enhance feature learning, reduce computational load, and balance class representation, we utilized a method to convert orthomosaic images into smaller chips. This process involves:

Inputs: TIFF image, chip width, chip height, and overlap percentage.
Outputs: Number of extracted chips, a sample of 20 chips, and saving the chips to disk.

By processing the orthomosaic image into smaller sections, we improve model learning from finer details, reduce computational requirements, and ensure balanced class representation in the dataset. Additionally, we created a Streamlit interface for this process to facilitate easy and user-friendly interaction.

<img src="https://github.com/saimaansi13/Drone-based-geo-spatial-ML-for-crop-health-yield-assessment/assets/125540201/5a81bee3-516a-40a9-9614-103e236e6be1" width="300">

### 3) Dynamic Tiling
