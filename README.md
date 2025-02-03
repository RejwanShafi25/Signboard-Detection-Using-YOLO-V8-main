# Signboard Detection Using YOLO V8
 This project involves building a custom object detection model using YOLOv8 as part of my coursework for CSE428 (Image Processing) back in Spring24 Semester. The model is designed to detect signboards in images.

### Group Members:
- [Rejwan Shafi](https://www.linkedin.com/in/rejwan-shafi-905ba32a8/)
- [Homairah Ferdousia](https://github.com/HOMAIRAH-FERDOUSIA)
- Ramisa Sharar Nidhi
- Anurag Sikder

## Model Implementation
For this project, we imported YOLOv8 directly from the Ultralytics library rather than building the model from scratch. This allowed us to focus on dataset preparation, training, and evaluation while leveraging YOLOv8's state-of-the-art object detection capabilities.

## Dataset
We used a local dataset containing approximately 3,800 images, all captured in Bangladesh. The dataset was not pre-split into training, validation, and test sets, so we manually divided it into three subsets.

### Dataset Challenge
- Most signboards were accurately annotated.
- Some images contained incorrect annotations, where objects other than signboards were labeled.
- Very small, distant signboards were often not annotated in the dataset.

> _**Note:**_ Due to copyright restrictions, we are unable to publicly share the dataset.

## Model Performance
After training our YOLOv8 model, we evaluated its performance on both the validation and test sets:
| Metric        | Validation Set | Test Set |
|--------------|---------------|----------|
| **Box Precision** | 60.4%       | 61.2%    |
| **Recall**        | 67.4%       | 67.0%    |
| **mAP@50**       | 63.7%       | 64.8%    |
| **mAP@50-95**    | 43.8%       | 43.9%    |


### Additional Testing
Beyond the test set, we scraped additional signboard images from the web, including:
- More images from Bangladesh
- Signboard images from India
Our model performed well on these new images, successfully detecting both very small and small signboards.

## Example Predictions
Here are some examples of successful signboard detections by our model:

![image](https://github.com/user-attachments/assets/65842521-ab61-45a2-818f-c8dc1b952348) ![image](https://github.com/user-attachments/assets/ac6df766-9d67-4890-8404-28fca3a12cab)![image](https://github.com/user-attachments/assets/558cb3f4-e3a3-439f-8538-b7fe518948b9) ![image](https://github.com/user-attachments/assets/d2bf08d0-89cf-464c-9b45-4f7de3eb23b9)


