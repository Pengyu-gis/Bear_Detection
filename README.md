# Intelligent Bear Prevention System Based on Computer Vision and IoT: A New Approach to Reduce Human-Bear Conflicts  

<p align="center">
  
**Pengyu Chen<sup>1, 2</sup>, Teng Fei<sup>1*</sup>, Yunyan Du<sup>3</sup>, Jiawei Yi<sup>3</sup>**

</p>

<sup>1</sup> School of Resources and Environmental Sciences, Wuhan University, Wuhan 430070, China  
<sup>2</sup> Department of Geography, University of South Carolina, Columbia 29201, USA  
<sup>3</sup> State Key Laboratory of Resources and Environmental Information System, Beijing 100101, China  

---

## Dataset  

The dataset contains a total of 6 labels and 1,195 images, organized as follows:  

| Label  | Training Set / Validation Set | Total |
| ------ | ----------------------------- | ----- |
| Cat    | 133 / 6                       | 139   |
| Cow    | 155 / 7                       | 162   |
| Dog    | 154 / 7                       | 161   |
| Bear   | 794 / 10                      | 804   |
| Goat   | 70 / 6                        | 76    |
| Human  | 131 / 6                       | 137   |  

---

## Training Parameters  

### Image Augmentation  

- **Random mirroring**: Enabled  
- **Random rotation**: Disabled  
- **Random blurring**: Enabled  
- **Scaling method**: Contain  
- **Scaling size**: 224 x 224  
- **Mean value**: 123.5  
- **Standard deviation**: 58.395  

### Model Information  

- **Deployment platform**: nncase  
- **Model architecture**: YOLOv2  
- **Backbone network**: MobileNet_0.75  

### Training Parameters  

- **Training epochs**: 150  
- **Batch size**: 32  
- **Learning rate**: 0.001  
- **Bounding box limit**: 8  
- **Data balancing**: Disabled  
- **Allow negative samples**: Enabled  

---

## Training Results  

The best accuracy on the validation set was achieved at the 150th training iteration: **0.654**.  

![Training Results Visualization](https://github.com/user-attachments/assets/efc49203-af0e-4688-a9e8-fdcd2bdf20f3)  

---

## Validation Set Results  

### Correct Results  

<p align="center">
  <img src="https://github.com/user-attachments/assets/eaf3997c-ee4a-422b-80e9-7d6364908e45" width="20%" alt="Correct Result 1">
  <img src="https://github.com/user-attachments/assets/21c88ac9-24a0-4a07-a99c-77eb79e7c828" width="20%" alt="Correct Result 2">
  <img src="https://github.com/user-attachments/assets/6d375edf-8404-48fd-8f80-1b6bfcfc0ea3" width="20%" alt="Correct Result 3">
  <img src="https://github.com/user-attachments/assets/bdd65ba1-653b-41f2-8265-41d3d5dd4447" width="20%" alt="Correct Result 4">
</p>

### False Results  

<p align="center">
  <img src="https://github.com/user-attachments/assets/93f39411-53c7-4c55-a106-09bd4305cf78" width="20%" alt="False Result 1">
  <img src="https://github.com/user-attachments/assets/f31dcce2-121d-4aa9-9937-de81589aac77" width="20%" alt="False Result 2">
  <img src="https://github.com/user-attachments/assets/fe7f89ea-a063-4c96-b7b1-d9d2e054dc83" width="20%" alt="False Result 3">
  <img src="https://github.com/user-attachments/assets/9c6d58a9-971b-4b5e-9d92-9b716100a411" width="20%" alt="False Result 4">
</p>

---

> - *White boxes are user-labeled boxes.*  
> - *The green box is the model's correct prediction box.*  
> - *The red box is the model's incorrect prediction box.*  
> - *Only white boxes indicate that the model did not detect the target.*  

---

### Notes  

For better clarity, images are scaled down for display. Full-size images are available in the dataset directory.  
