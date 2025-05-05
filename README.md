# Eshara ISL Detection
## Dataset Preprocessing
### Conversion of Videos to Frames using MediaPipe
* The data preprocessing began by converting raw video files into frames using MediaPipe, a framework that detects and tracks human body landmarks. Each video was processed to extract pose keypoints for each frame, and the resulting outputs included both the visual frames and the corresponding landmark data (such as coordinates of body joints).
* The dataset of the processed videos into frames
  --> [Processed_openpose_data](https://drive.google.com/drive/folders/13FuZXt5sr-hpp905mR52lvCO2rxe-5u9?usp=sharing)
* After processing all videos, the extracted data was cleaned—frames. Once the full set of MediaPipe-processed frames was ready, the dataset was divided into training and testing sets, either by using a fixed ratio (such as 80% training and 20% testing).
* The dataset which is augmented and dividing the frames into train and test
  --->[Openpose_train_test_data](https://drive.google.com/drive/folders/1MCpPj-6nEi5hnlIywrONSZ7Z9GQ5Tbe7?usp=sharing)
  [View the colab notebook for this](01_Eshara_datapreopenpose.ipynb)
* The final structure consists of one folder containing all MediaPipe outputs and another with the data split into train and test directories, prepared for model training or evaluation.
* After the initial preprocessing with MediaPipe, we used OpenPose to generate more accurate and detailed pose estimations. This allowed us to improve the overall quality of the dataset. Using the OpenPose output, we created a more refined train and test split, ensuring better consistency and reliability for training pose-based models.
 ---> [Feature_train_test_data](https://drive.google.com/drive/folders/170prNqbxnZ2cttd1X9EVUyyQVK0kjA3f?usp=sharing)
  [View the colab notebook for this](02_Eshara_train_test_split.ipynb)
