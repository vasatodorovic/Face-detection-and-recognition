# Face-detection-and-recognition-with-YOLO

This project implements a custom YOLO (You Only Look Once)👀 model for detecting faces in images. The model has been built from scratch using PyTorch, and it predicts bounding boxes around faces in images.

1. **Model Architecture**: 
   - The YOLO architecture consists of convolutional layers for feature extraction and fully connected layers for predicting bounding boxes.
   - The model outputs grid cells (14x14), each predicting 1 bounding box along with confidence score.

2. **Loss Function**: 
   - The custom loss function includes multiple components:
     - **Coordinate Loss (`lambda_coord=5`)**: Penalizes errors in the predicted center coordinates of the bounding boxes.
     - **Size Loss (`lambda_size=5`)**: Penalizes discrepancies in the predicted width and height of the bounding boxes.
     - **Object Loss (`lambda_obj=1`)**: Penalizes differences in confidence scores for boxes that contain objects.
     - **No Object Loss (`lambda_noobj=0.5`)**: Reduces false positives by penalizing confidence in grid cells without objects.

3. **Non-Maximum Suppression (NMS)**:
   - After the model generates bounding box predictions, NMS is applied to eliminate redundant boxes. 
   - NMS filters out overlapping boxes based on Intersection over Union (IoU) and retains only the most confident predictions.

### Directory Structure

- **00_FaceDetection**: Contains the final implementation with all scripts for training, evaluation, and inference.
- **previous_attempts**: Holds earlier versions of the project, documenting issues with dataset construction and loss function design.
  
#### Constructed models: 

- https://drive.google.com/drive/folders/1YU3ZbLDScdlr_SaJtzAjiH6ksqnjWmME?usp=drive_link

#### Data: 

- https://drive.google.com/drive/folders/1WhAjMJtyc5AcPpBlUCGp75LF88TnC4Q7?usp=drive_link

#### References: 
- [Redmon_You_Only_Look_CVPR_2016_paper.pdf](https://github.com/user-attachments/files/16826241/Redmon_You_Only_Look_CVPR_2016_paper.pdf)
- [face_detection_and_recognition.pdf](https://github.com/user-attachments/files/16826240/face_detection_and_recognition.pdf)

### Student:
- Vasilije Todorović


