# Network Intrusion Detection Using Decision Trees

This project focuses on analyzing and classifying various types of network intrusions to detect potential attacks. It uses machine learning models, particularly decision trees, to accurately classify and identify different intrusion types.

## Dataset

The dataset used for this project is the **KDD Cup 1999 dataset**. These sets include multiple features that describe network connections and label attack types. The structure is as follows:

- **Training set**: Used to train the machine learning models, containing a mixture of attack types and normal traffic.
- **Test set**: Used to evaluate the models' performance, including both known and new attack types.

## Features

The dataset includes various features related to network traffic, such as:

- `duration`: Duration of the network connection.
- `protocol_type`: The type of network protocol (e.g., TCP, UDP).
- `service`: The network service on the destination port (e.g., HTTP, FTP).
- `flag`: Status of the connection.
- `src_bytes`, `dst_bytes`: Number of bytes from the source and destination, respectively.

Additionally, the dataset includes a label column, indicating whether a connection is normal or represents a specific type of attack.

## Data Preprocessing

To prepare the dataset for machine learning models, the following preprocessing steps were performed:

- **Label Encoding**: Categorical features like `protocol_type`, `service`, and `flag` were transformed into numeric values.
- **One-Hot Encoding**: The same categorical features were also converted into a binary format for better model performance.
- **Feature Selection**: Techniques like `SelectPercentile` and Recursive Feature Elimination (RFE) were used to select the most relevant features for identifying each attack type.
- **Normalization**: A `StandardScaler` was applied to normalize the features, ensuring they are on a similar scale.

## Attack Categories

The project targets the classification of four primary attack categories:

1. **DoS (Denial of Service)**
2. **Probe (Information Gathering)**
3. **R2L (Remote to Local)**
4. **U2R (User to Root)**

Each attack category requires careful analysis of specific features to ensure accurate detection and classification.

## Model Training and Evaluation

Multiple models were trained, with decision trees being used extensively due to their interpretability and ability to handle complex feature sets. The models were evaluated using the following metrics:

- **Confusion Matrix**: To analyze misclassifications.
- **Accuracy**: To measure the overall performance of the model.
- **Feature Importance**: To highlight which features contributed most to the model's predictions.

## Results and Insights

The following key results were observed:

- **Selected Features**: Identified the most important features for detecting each attack category.
- **Performance Metrics**: Provided accuracy scores and confusion matrices for each model.
- **Insights**: Detailed observations on which features are most indicative of specific attack types.

## Future Considerations

To extend the project's scope, consider the following:

- **Cross-Validation**: Implement cross-validation to improve the robustness of the model.
- **Model Diversity**: Explore other machine learning models such as Random Forest, Support Vector Machines (SVM), or Neural Networks.
- **Handling Imbalanced Data**: Experiment with techniques to address imbalanced attack categories, such as oversampling or undersampling.
- **Real-World Application**: Investigate the deployment of these models in a real-world intrusion detection system (IDS).

## Installation

To run the project:

1. **Clone the repository**:
    ```bash
    git clone https://github.com/Shreyagoyal0708/Network_intrusion-decision-tree-.git
    ```

2. **Run the project**:
    - Open the project in Visual Studio, Jupyter Notebook, or any Python-compatible IDE.
    - Ensure that both the training and test datasets are in the correct directories.
    - Run the Jupyter notebook to train and evaluate the models.

## Contributing

Contributions are welcome! If you encounter a bug or would like to suggest new features, feel free to open an issue or submit a pull request.
