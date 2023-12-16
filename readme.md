
In the aftermath of natural disasters or conflict-ridden areas, rapid and well-informed decision-making is crucial. This project proposes an innovative solution by integrating satellite imagery with deep learning techniques, specifically utilizing YOLO and U-Net image segmentation models. The goal is to automate and expedite critical tasks such as identifying helicopter landing zones and mapping suitable roads, providing timely and precise information for emergency response.

## Features

- Helicopter Landing Zone Detection with Aerial Depth Estimation and Zone Classification using YOLO and Inception modules.
- Road mapping on unfamiliar terrains utilizing U-Net deep learning model with SAR patches and OpenStreetMap (OSM) road data masks.

### Helicopter Landing Zone Detection

The approach involves estimating aerial depth maps using YOLO on RGB images, leveraging datasets like KITTI. The system focuses on the farthest depth data, utilizing a classifier with Inception modules for potential landing zone classification. YOLO is trained on synthetic aerial images generated from urban scenarios.

### Road Mapping on Unfamiliar Terrains

The proposed methodology utilizes a U-Net model trained on SAR patches and OSM road data masks. Soft Dice loss and Jaccard index are employed to address class imbalance. The model, demonstrated in challenging desert landscapes, showcases robustness and scalability using free Sentinel-1 data for cost-effective global road mapping.


- Landing Site DataSet : https://drive.google.com/drive/folders/1huNchFOyIBEkGaozXrIlmC50OMsUa-Sd
- Road Data
