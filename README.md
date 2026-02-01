Task-10 KNN – Handwritten Digit Classification

Objective

The objective of this task is to build a machine learning model to classify handwritten digit images (0–9) using the K-Nearest Neighbors (KNN) algorithm and to analyze the impact of different values of K on model performance.

maodel Evaluation:

K = 3, Accuracy = 0.9666666666666667

K = 5, Accuracy = 0.9638888888888889

K = 7, Accuracy = 0.9666666666666667

K = 9, Accuracy = 0.9638888888888889


Methodology
In this task, the handwritten digits dataset provided by the sklearn.datasets module was used. Each data sample represents an 8×8 grayscale image of a digit, which is flattened into 64 numerical input features. The target variable represents the digit class ranging from 0 to 9. The dataset was first explored by visualizing a few sample images along with their labels in order to understand the structure and quality of the data.

The dataset was then divided into training and testing sets using an 80:20 split, while preserving the class distribution using stratification. Since KNN is a distance-based algorithm, feature scaling was performed using StandardScaler. The scaler was fitted only on the training data and then applied to both the training and test sets to avoid data leakage.

Multiple KNN models were trained by varying the number of neighbors (for example, K = 3, 5, 7 and 9). For each value of K, the model was trained on the scaled training data and evaluated on the test data using classification accuracy. The accuracies obtained for different K values were compared to understand the influence of the hyper-parameter and to select the most suitable value of K.

After identifying the best K value based on the highest test accuracy, a final KNN model was trained using this optimal parameter. The performance of the final model was further analysed using a confusion matrix to observe how well each digit class was classified and to identify common misclassifications. In addition, a few test images were displayed along with their true and predicted labels to visually verify the model’s predictions.

Conclusion
This task successfully demonstrates the use of the K-Nearest Neighbors algorithm for handwritten digit classification. The results show that proper data preprocessing, especially feature scaling, plays a crucial role in improving the performance of distance-based models. The experiment also confirms that the choice of the number of neighbors significantly influences model accuracy. By selecting an optimal K value and evaluating the model using accuracy and a confusion matrix, a reliable and interpretable digit classification model was obtained. Overall, the KNN approach proved to be effective for small and well-structured datasets such as the sklearn digits dataset.
