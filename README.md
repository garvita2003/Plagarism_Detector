# Plagarism_Detector
Plagiarism detection is a crucial task in educational and professional settings. By leveraging machine learning techniques, we can create a robust plagiarism detector that can accurately identify copied content. 

# Collecting the Dataset
The first step in building our plagiarism detector is gathering a comprehensive dataset. The dataset should consist of text documents that contain both original and plagiarized content. This dataset will help train our machine learning model to distinguish between original and copied content.

# Preprocessing the Data
Before feeding the data into our machine learning model, we need to preprocess it. Preprocessing steps include:
1. Tokenization: Splitting the text into individual words or tokens.
2. Lowercasing: Converting all text to lowercase to ensure uniformity.
3. Removing Punctuation: Eliminating punctuation marks to avoid treating them as words.
4. Stopwords Removal: Removing common words like "and", "the", etc., that do not contribute to the meaning of the text.

# Building the Machine Learning Model
We use the Term Frequency-Inverse Document Frequency (TF-IDF) vectorizer to transform the text data into numerical features. Then, we train a model using these features. For this example, we will use a simple logistic regression model.

# Creating the Flask Web Application
To make our plagiarism detector easily accessible, we create a Flask web application. This application will provide a user interface where users can input two text documents and receive a plagiarism score.

# Approach:

1. Approach 1:
- Model used - Logistic Regression, Random Forest, Naive Bayes and Support Vector Machine
- pip install flask
- pip install scikit-learn==1.6.0 -> this is a version that is being showed in the jupiter notebook Plagarism_Checker_using_ML
- Run app.py and go to the web page

3. Approach2:
- option 1 : comparing folder with Masterfile
  - plagiarism allowed: 15
  - file:test folder path -> TestFile
  - master file: main.txt path -> main.txt

- option 2: check for plagiarism in two files
  - plagiarism allowed : 20
  - file1 : sample1.txt path -> TestFile\sample1.txt
  - file2: sample2.txt path -> TestFile\sample2.txt

- option 3: check for plagiarism in all the files in the folder
  - plagiarism allowed:20
  - file: test folder path -> TestFile

# Technology Used:
1. Python
2. Machine Learning
3. Sklearn
4. Flask
5. Term Frequency-Inverse Document Frequency (TF-IDF) vectorizer
6. Numpy
7. Pandas

# Overview:
Approach 1:
- Logistic Regression:

![Screenshot 2025-01-08 124702](https://github.com/user-attachments/assets/8342df45-7aef-4c22-83f8-00f7f6e0f0aa)

- Random Forest:

![Screenshot 2025-01-08 124744](https://github.com/user-attachments/assets/8a9e95e7-9d2f-4d8d-ac9b-f811101fb7d4)

- Naive Bayes:

![Screenshot 2025-01-08 124814](https://github.com/user-attachments/assets/9e77a54f-db1f-44ce-8c5a-3b18ad048b60)

- Support Vector Machine:

![Screenshot 2025-01-08 124820](https://github.com/user-attachments/assets/b74109ff-3175-4cc7-b5dc-f49d502a510a)

- Implementation:

![Screenshot 2025-01-08 124835](https://github.com/user-attachments/assets/9737155c-88ad-4b52-bd38-70bf4b8c5211)

Implement the above notebook example in the flask app:

![Screenshot 2025-01-08 125317](https://github.com/user-attachments/assets/c71ebe35-e77e-4ce5-905d-5efd85df10ff)
![Screenshot 2025-01-08 125344](https://github.com/user-attachments/assets/45d28b54-2153-4451-a1eb-ede296295daf)
![Screenshot 2025-01-08 125411](https://github.com/user-attachments/assets/27e7fe5e-7720-4dce-8c93-74cb0c7cc0ac)


Approach 2:
- Option 1:
  
![Screenshot 2025-01-08 124023](https://github.com/user-attachments/assets/7dae416c-972d-4e71-b05a-c60a4098562a)

- Option 2:

 ![Screenshot 2025-01-08 124307](https://github.com/user-attachments/assets/248eb335-a9fe-4286-af53-049e3db38a9e)

- Option 3:

![Screenshot 2025-01-08 124415](https://github.com/user-attachments/assets/db2206a0-6635-4589-bf1d-6db3de1046c1)
