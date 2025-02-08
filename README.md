# Fraud Detection using Anomaly Detection Techniques

## Objective
The objective of this project is to detect fraudulent transactions in a financial dataset. The focus is on building anomaly detection models that can efficiently identify fraud while minimizing false negatives, which are crucial in fraud detection. To achieve this, we explore various models and apply techniques such as dimensionality reduction and hyperparameter tuning to optimize performance.

## Why Anomaly Detection?
In fraud detection, the challenge lies in identifying rare events (fraudulent transactions) that deviate significantly from the norm. Since fraudulent transactions are highly imbalanced compared to non-fraudulent ones, **supervised learning** methods are not ideal. This is because supervised learning requires a significant amount of labeled fraud data, which is often not available. **Anomaly detection**, on the other hand, works by detecting outliers or anomalies in the data, which is exactly the case with fraud. By using **unsupervised learning**, we can identify transactions that differ significantly from the majority, even if no labeled fraud examples are provided.

However, we did use **labels** for **model evaluation** to assess the performance of the anomaly detection models. This helped in tuning the models and selecting the best-performing one based on key metrics such as **F2-Score**, **Precision**, **Recall**, and **Accuracy**.

## Models Used
1. **Support Vector Machine (SVM)**
2. **Isolation Forest**
3. **Gaussian Anomaly Detector (PDF-based)**

We evaluated these models on a validation set, using **F2-Score** (with a beta of 5) as the primary metric to prioritize recall. The best-performing model was chosen based on these results.

## Data Preprocessing and Dimensionality Reduction
We used **dimensionality reduction** techniques to reduce the complexity of the data and improve model performance. This step helped in removing unnecessary features and reducing noise, allowing the models to focus on the most relevant information.

### Hyperparameter Tuning
We performed **hyperparameter tuning** on the validation set, particularly focusing on adjusting the **threshold** parameter to determine the best threshold for anomaly detection. The best threshold was selected based on the highest F2-Score.

### Test Set and Unseen Fraud Examples
To evaluate the models' ability to detect unseen frauds, we excluded **fraud examples** from the test set. This approach allows us to assess how well the models can generalize and detect fraud in real-world, unseen scenarios.

## Visualizations
Visuals provided insights into the differences between fraudulent and non-fraudulent transactions, helping to inform the model choice.

## Results
### Metrics on Test Set
- **F2-Score**: 0.8521
- **F1-Score**: 0.8024
- **Precision**: 0.7546
- **Recall**: 0.8565
- **Accuracy**: 0.9965

## Conclusion
The **Gaussian Anomaly Detector (PDF-based model)** performed the best in this project, yielding the highest **F2-Score** and **Recall**. This model was able to identify fraudulent transactions effectively while minimizing false negatives. The use of **hyperparameter tuning** and **dimensionality reduction** contributed to optimizing model performance, ensuring that the model can handle unseen fraud examples and generalize well on the test set.

## Future Work
There are several ways this project can be expanded or improved:
- **Deep Learning**: Experimenting with deep learning-based anomaly detection methods such as autoencoders or neural networks, which might be able to capture more complex patterns in the data.
- **Real-time Fraud Detection**: Implementing real-time fraud detection systems where incoming transactions are classified as fraud or not in real-time.
- **Ensemble Methods**: Combining multiple models or using ensemble techniques to improve performance further and reduce the chances of misclassification.
- **Model Interpretability**: Adding interpretability to the models, such as SHAP or LIME, to better understand why certain transactions are classified as fraudulent.

## Contributing
We welcome contributions from the community. If you'd like to contribute, please follow these steps:
1. Fork the repository.
2. Create a new branch for your changes (`git checkout -b feature-branch`).
3. Commit your changes (`git commit -am 'Add new feature'`).
4. Push to your branch (`git push origin feature-branch`).
5. Open a pull request.

Make sure to follow the coding standards and write tests for new features or bug fixes.

## License
This project is licensed under the MIT License.
