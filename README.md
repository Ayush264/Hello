Cyberbullying Detection Project
Introduction
This project aims to detect cyberbullying in tweet text using various machine learning models. The goal is to classify tweets into different categories of cyberbullying or as not cyberbullying, helping to identify and potentially mitigate harmful online content.

Installation
To run this notebook and project, you need to install the following Python libraries. You can install them using pip:

%pip install numpy
%pip install pandas matplotlib demoji
%pip install scikit-learn
%pip install seaborn
%pip install tweepy nbformat ipykernel nltk plotly
Dataset
The project uses the cyberbullying_tweets.csv dataset, which contains tweet texts labeled with different cyberbullying types:

not_cyberbullying
gender
religion
other_cyberbullying
age
ethnicity
The dataset is loaded and explored to understand its structure and distribution of cyberbullying types.

Data Preprocessing
Before training the models, the tweet texts undergo several preprocessing steps:

Cleaning: Removal of hashtags, mentions, URLs, and other non-alphabetic characters.
Lowercasing: All text is converted to lowercase.
Tokenization and Lemmatization: Words are tokenized and then lemmatized to reduce them to their base form.
Stop Word Removal: Common English stop words are removed to focus on more meaningful terms.
Emojis are also handled using the demoji library, although the specific implementation for emoji removal/handling was part of the clean_text function.

Model Training and Evaluation
Several machine learning models were trained and evaluated for cyberbullying detection:

Random Forest Classifier
Multinomial Naive Bayes
Decision Tree Classifier
Logistic Regression
Linear SVM
Tweet texts are converted into numerical features using CountVectorizer for most models, and TfidfVectorizer specifically for the final Logistic Regression model used in the interactive predictor. The models are evaluated based on their accuracy scores, and a confusion matrix and classification report are provided for the best-performing model (Logistic Regression).

The Logistic Regression model achieved the highest accuracy of approximately 80.94%.

Usage (Interactive Predictor)
An interactive widget is provided to predict the cyberbullying type of a given tweet. Follow these steps:

Run all cells in the notebook, especially the cells under 'Model Training and Evaluation' and the last two cells that set up the interactive predictor.
Enter a tweet text into the provided text area.
Click the 'Predict' button.
The predicted cyberbullying type will be displayed below the button.
