---
title: "CNN - Sentinel Building Segmentation"
excerpt: "This project involved developing a machine learning pipeline to classify building locations in cities using satellite images. The model was trained to identify whether pixels in satellite images from the Sentinel 2 satellite contain buildings. The project included solutions for multiple sub-tasks and a final report detailing the results. Open-source ML libraries were used, and accuracy was tested on specific geographic coordinates. <br/><img src='/images/uni/berlin_building_detection.png'>"
collection: portfolio
---

### Classify building locations in cities from satellite images

**Steps:**

- **Data Acquisition and Alignment:**  
  A pipeline was created to gather training data by downloading OpenStreetMap files and Sentinel 2 satellite images. The process involved extracting building coordinates from OpenStreetMap and aligning them with satellite data. Libraries like `pyrosm` and `Openeo` automated the downloading and processing of map projections and satellite images for at least ten major cities.

- **Data Preparation:**  
  Satellite images were preprocessed by slicing them into 128x128 pixel patches for training. A cloud-cover classifier was applied to remove patches containing clouds. The result was a dataset of tensors with aligned spectral bands and corresponding target building masks. The data was split into train, validation, and test sets, ensuring no data leakage and consistent distributions.

- **Modeling and Tuning:**  
  A baseline model of four CNN layers was built to classify pixels as either containing buildings or not. Each layer increased in complexity, with the final layer outputting a single value per pixel to indicate building presence. Hyperparameter tuning (e.g., learning rate, optimizers, and early stopping) was applied to improve the model, and additional architectures like U-Net and SegNet were explored. The model’s performance was evaluated on both training and validation sets, with tuning impact reported.

- **Data Augmentation:**  
  Various data augmentation techniques, such as rotations, reflections, noise modulation, zoom, mixup, and shearing, were applied to enhance model quality. These augmentations were introduced into the data preparation pipeline, with experiments conducted to evaluate their effect on the train and validation sets. A final comparison was made between models with and without augmentation on the test data.

[Report](https://github.com/dmtschulz/satellite-image-segmentation/blob/main/report.pdf) \
[Github link with code](https://github.com/dmtschulz/satellite-image-segmentation)

![Example Classification Result](/images/uni/berlin_building_detection_result.png)
