# Settylinternsolutins

## Settyl Data Science And Machine Learning Engineer Task Documentation

### 1. Data Preprocessing
- The provided dataset was loaded from the given GitHub gist using the `requests` library.
- The external status descriptions and internal status labels were cleaned and formatted using regular expressions to remove special characters, punctuation, and extra spaces.
- The cleaned data was converted into numpy arrays for further processing.
- Label encoding was applied to encode the internal status labels into numerical values.

### 2. Model Development
#### LSTM Model
- The LSTM model architecture was chosen for text classification tasks due to its effectiveness in capturing sequential patterns in text data.
- The model consists of an embedding layer, LSTM layer, and a dense output layer with softmax activation.
- The embedding layer converts words into dense vectors of fixed size, allowing the model to learn meaningful representations of words.
- The LSTM layer processes the embedded sequences and captures temporal dependencies.
- The output layer produces the probability distribution over the internal status labels.

#### Support Vector Machine (SVM) Model
- The SVM model was chosen as a baseline classifier for comparison with the LSTM model.
- The CountVectorizer was used to convert the text data into numerical vectors for input to the SVM model.
- The SVM model was trained using the one-hot encoded input features and the encoded internal status labels.

### 3. Model Training and Evaluation
#### LSTM Model
- The LSTM model was trained using the preprocessed dataset.
- The model was compiled with the Adam optimizer and sparse categorical cross-entropy loss function.
- Training was performed for 10 epochs with a batch size of 32.
- The model achieved a test accuracy of approximately 93%.

#### SVM Model
- The SVM model was trained using the preprocessed dataset and one-hot encoded input features.
- The model achieved a test accuracy of approximately 99%.

### 4. API Development
- The FastAPI framework was used to develop an API for exposing the trained LSTM model.
- The API accepts external status descriptions as input and returns the predicted internal status labels.

### 5. Testing and Validation
- The developed API was thoroughly tested to ensure its functionality and accuracy.
- Predictions were validated against a validation dataset to measure the model's generalization ability.

### 6. Conclusion
- The LSTM model demonstrated competitive performance compared to the SVM baseline.
- The API provides a convenient interface for making predictions based on external status descriptions.
- Further optimization and fine-tuning can be explored to improve model performance and scalability.
  
### 7. Recommendations
- Continuously monitor and evaluate the model's performance in real-world scenarios.
- Collect additional data to improve the model's generalization ability and robustness.
- Explore advanced techniques such as transfer learning and ensemble methods for further improvement.
