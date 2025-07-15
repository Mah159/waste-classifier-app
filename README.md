# waste-classifier-app

The dataset chosen for this app was downloaded from kaggle and accessed after uploading on drive:

https://www.kaggle.com/datasets/aashidutt3/waste-segregation-image-dataset

It contains two main folders called "val" and "train", each has two folders of biodegradable and non-biodegradable waste (plastic bottles, plastic bags, metal cans and e-waste) images.

In Google colab the code written which has been saved as waste_classifier.keras sets up and trains a deep learning model for classifying waste images into biodegradable and non-biodegradable categories. It includes steps for preprocessing the dataset (image conversion and corruption removal), initializing data generators, building a MobileNetV2-based convolutional neural network using TensorFlow/Keras, training the model, and saving it for later use. Furthermore, the accuracy and loss of the train and val portion of the dataset, the confusion matrix, the precision, recall and f1 score have been calculated.

Interpretation:

Biodegradable class:

Precision ≈ 0.75: When the model predicts biodegradable, it's correct about 75% of the time.

Recall ≈ 0.73: It successfully detects ~73% of all actual biodegradable items.

F1 Score ≈ 0.74: This is the harmonic mean of precision and recall, showing a balanced performance.

Non-biodegradable class:

Precision & Recall ≈ 0.26–0.28: The model performs poorly for this class, often misclassifying it as biodegradable.

F1 Score ≈ 0.27: Indicates weak performance in identifying non-biodegradable waste.

Conclusion: The model is much better at identifying biodegradable waste than non-biodegradable, which suggests a class imbalance or insufficient training examples for non-biodegradable items.

Confusion Matrix
True Biodegradable (664) correctly predicted.

Biodegradable misclassified as Non-biodegradable (230).

True Non-biodegradable (64) correctly predicted.

Non-biodegradable misclassified as Biodegradable (243).

Future improvements:
- Augment or balance the dataset with more non-biodegradable examples.

The next step was the create a User Interface in Gradio. Its code has been given in the file app.py. The website link was hence generated in colab. 
