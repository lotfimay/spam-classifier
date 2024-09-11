# **Email Spam Classification Project**

This project focuses on building and comparing multiple machine learning models to classify emails as either "spam" or "ham" (not spam). Various models, including Naive Bayes, Support Vector Machines (SVM), Long Short-Term Memory (LSTM), and Convolutional Neural Networks (CNN), were trained and evaluated on accuracy.

## **Project Overview**

Spam classification is an essential task in email filtering systems to prevent unwanted messages from reaching users. This project leverages different machine learning approaches to solve this problem. The models were trained on a dataset of labeled emails and compared based on their classification accuracy.

## **Pre-processing Steps**

Before training the models, the email data underwent several pre-processing steps to convert raw text into a suitable format for machine learning models.

### 1. **Text Cleaning**
   - Convert all text to lowercase.
   - Remove punctuation marks and special characters.
   - Eliminate numbers to focus only on the text content.
   - Remove common stop words (e.g., “and,” “the”).
   - Apply stemming/lemmatization to reduce words to their base forms (e.g., "running" → "run").

### 2. **Tokenization**
   The cleaned text was broken down into individual words (tokens) to make it easier for models to process the data.

### 3. **Vectorization**
   - **Bag-of-Words (BoW)**: This method counts the frequency of each word in a document.
   - **TF-IDF (Term Frequency-Inverse Document Frequency)**: Assigns a weighted score to words, balancing word frequency in individual documents against their frequency in the overall corpus.

### 4. **Dataset Splitting**
   The dataset was split into:
   - **Training Set**: Used to train the models (typically 80% of the data).
   - **Test Set**: Used to evaluate model performance (typically 20% of the data).

### 5. **Feature Scaling**
   For models sensitive to the scale of input data, such as SVM and Neural Networks, feature scaling was applied to normalize the data using techniques like `MinMaxScaler`.

## **Models Used**

The following models were tested and compared:

1. **Naive Bayes**
2. **SVM Binary**
3. **SVM Counter**
4. **LSTM (Long Short-Term Memory)**
5. **CNN (Convolutional Neural Network)**

## **Model Performance**

The performance of each model was evaluated using accuracy, which is the percentage of correctly classified emails. Below is a summary of the accuracy for each model:

| Model       | Accuracy  |
| ----------- | --------- |
| Naive Bayes | 0.9880    |
| SVM Binary  | 0.9952    |
| SVM Counter | 0.9797    |
| LSTM        | 0.9929    |
| CNN         | 0.9964    |

### **Conclusion**

All the models demonstrated high accuracy for email classification. The CNN model had the best performance, achieving an accuracy of 99.64%. The SVM Counter model performed the lowest, but still maintained a competitive accuracy of 97.97%. The results indicate that deep learning models (LSTM and CNN) can slightly outperform traditional models like Naive Bayes and SVM for this task.


## **Future Improvements**

- **Hyperparameter Tuning**: Fine-tuning the hyperparameters of each model could further improve performance.
- **Data Augmentation**: Using data augmentation techniques to generate synthetic data could improve model robustness.
- **More Features**: Adding more features, such as metadata from emails (e.g., sender, timestamp), could provide more insights for classification.