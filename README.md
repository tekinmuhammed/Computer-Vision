# Computer Vision-Project   Potato Disease Leaf ML

This project aims to classify potato leaf diseases using deep learning techniques. By leveraging convolutional neural networks (CNNs), we can accurately identify and categorize different stages of disease in potato leaves, aiding in timely and effective agricultural interventions. Potato crops are highly susceptible to various diseases, which can significantly impact yield and quality. Early detection and accurate classification of these diseases are crucial for effective management and intervention.

### Dataset
The dataset comprises 4062 images of potato leaves. Images are categorized into three classes: Early Blight, Healthy, and Late Blight. Each image is 256x256 pixels, ensuring uniformity for model training. The dataset was split into training, validation, and testing sets to facilitate model development and evaluation.

### Classes
We classified the potato leaf images into three distinct categories:
•	Early Blight: Characterized by dark spots with concentric rings on older leaves.
•	Healthy: Leaves without any visible signs of disease.
•	Late Blight: Symptoms include brown or black lesions on leaves, often accompanied by white fungal growth on the undersides.

## Training the Model
We trained two models for this classification task:
•	Model 1: Custom CNN A custom-built convolutional neural network trained for 25 epochs using augmented training data. Data augmentation techniques were applied to prevent overfitting. The model's architecture included several convolutional layers followed by max-pooling and dense layers for classification.
•	Model 2: Transfer Learning with InceptionV3 Utilized the pre-trained InceptionV3 model, adding custom dense layers for classification. This model was also trained for 25 epochs with data augmentation. Transfer learning leverages the pre-trained weights of InceptionV3, which has been trained on a large dataset, to improve classification performance on our specific dataset.

## Results
Both models were evaluated on the test dataset. The results are summarized as follows:
•	Model 1: Custom CNN
  o	Test Accuracy: 91.15%
  o	Classification Report:
    	Early Blight: Precision: 0.41, Recall: 0.46, F1-Score: 0.44
    	Healthy: Precision: 0.29, Recall: 0.27, F1-Score: 0.28
    	Late Blight: Precision: 0.31, Recall: 0.28, F1-Score: 0.30
•	Model 2: Transfer Learning with InceptionV3
  o	Test Accuracy: 90.89%
  o	Classification Report:
    	Early Blight: Precision: 0.44, Recall: 0.49, F1-Score: 0.47
    	Healthy: Precision: 0.26, Recall: 0.21, F1-Score: 0.23
    	Late Blight: Precision: 0.37, Recall: 0.38, F1-Score: 0.37


### Conclusion
Both models demonstrated strong overall accuracy in classifying potato leaf diseases. The transfer learning model with InceptionV3 slightly outperformed the custom CNN in terms of precision and recall for Early Blight and Late Blight. The custom CNN had a marginally better test accuracy. Future improvements could involve refining data augmentation techniques and experimenting with different pre-trained models. This project highlights the potential of deep learning in agricultural disease management, enabling timely and precise intervention.

### Keywords: 
Potato leaf disease, Deep learning, Convolutional neural networks, Transfer learning, InceptionV3
