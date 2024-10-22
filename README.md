# Topic Modeling on Amazon Reviews

## Project Overview

This project applies **Latent Dirichlet Allocation (LDA)** to Amazon customer reviews to uncover underlying topics within the reviews. The aim is to efficiently extract meaningful insights from customer feedback and evaluate the model's performance using coherence and perplexity metrics. The project also includes hyperparameter tuning to optimize the model for better performance.

## Table of Contents
- [Introduction](#introduction)
- [Dataset](#dataset)
- [Technologies Used](#technologies-used)
- [Project Workflow](#project-workflow)
- [Model Performance](#model-performance)
- [How to Use](#how-to-use)
- [Installation](#installation)
- [Future Improvements](#future-improvements)
- [License](#license)

## Introduction

Customer reviews contain valuable insights about products and services. This project focuses on **topic modeling** of Amazon reviews using LDA to identify and visualize key topics discussed by customers. The main objectives are:
- **Identify common themes** from customer feedback.
- **Evaluate model performance** using coherence and perplexity scores.
- **Optimize model performance** through hyperparameter tuning.

## Dataset

The dataset used contains Amazon customer reviews, with each entry including a review and its associated sentiment. For this project, we primarily focus on the review text and preprocess it to make it suitable for topic modeling.

Key features of the dataset:
- **Total entries**: 14,675 reviews
- **Columns**: Review text and sentiment (0 or 1)

## Technologies Used

- **Python**: For data preprocessing, modeling, and evaluation.
- **Pandas & NumPy**: For data manipulation and numerical operations.
- **NLTK & Gensim**: For text preprocessing and topic modeling.
- **Matplotlib & pyLDAvis**: For visualizing the topics and insights.
- **WordCloud**: For generating word clouds representing each topic.

## Project Workflow

1. **Data Loading & Exploration**: Load the dataset and explore the structure to prepare for preprocessing.
2. **Text Preprocessing**: 
   - Convert text to lowercase, tokenize, remove stopwords, and lemmatize the text.
   - Perform POS tagging and extract relevant parts of speech (e.g., nouns).
3. **Topic Modeling (LDA)**: 
   - Build an initial LDA model to identify topics from the reviews.
   - Evaluate model coherence and perplexity.
4. **Hyperparameter Tuning**:
   - Tune the LDA model using various combinations of the number of topics, alpha, and beta parameters to improve coherence.
5. **Visualization**:
   - Visualize the topics using pyLDAvis and WordCloud to display the most relevant words associated with each topic.
6. **Model Optimization**: 
   - Rebuild the LDA model after removing unwanted tokens and fine-tune for optimal performance.

## Model Performance

The LDA model was evaluated based on coherence scores, and hyperparameter tuning was performed to enhance the model's effectiveness. After testing several configurations, the 3-topic model was found to be the most interpretable and efficient, with a coherence score of **0.627**.

- **Topic 1**: Product Performance and Service Issues
- **Topic 2**: Phone Battery and Performance Concerns
- **Topic 3**: Camera and Multimedia Features

## How to Use

### Clone the repository:
```bash
git clone https://github.com/megokul/Topic_Modeling.git
```

## Installation
Ensure the following dependencies are installed:
```bash
pip install pandas numpy matplotlib nltk gensim pyLDAvis wordcloud
```
Alternatively, use the provided requirements.txt file:
```bash
pip install -r requirements.txt
```

## Future Improvements

- **Further Topic Refinement**: Experiment with different topic numbers to identify more granular topics.
- **Real-Time Processing**: Incorporate real-time topic extraction for customer reviews.
- **Enhanced Visualizations**: Improve topic interpretation through advanced visualization techniques.
- **Additional Models**: Explore other topic modeling techniques like **NMF** for comparison.

## License

This project is licensed under the MIT License.
