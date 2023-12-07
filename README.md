# EE541_Final_Project

# Movie Recommender System Using Neural Networks

## Overview
This project aims to develop a movie recommender system using a neural network model with the MovieLens dataset. The system is designed to process movie data, including titles, genres, and IDs, and utilizes these features to predict movie ratings.

## Dataset
The MovieLens dataset is used, which comprises a variety of movie attributes. This dataset is a popular choice for building recommendation systems due to its richness in movie-related information.

## Data Processing Steps
Data processing is a crucial step in preparing the dataset for the neural network model. The process involves several key steps:

### 1. Loading the Data
The MovieLens dataset is loaded into a Pandas DataFrame for ease of manipulation. Key columns such as movie titles, genres, and IDs are focused on.

### 2. Handling Genres
- **Extraction**: Genres are extracted from the dataset.
- **One-Hot Encoding**: The genres are one-hot encoded to convert them into a format suitable for the neural network.

### 3. Processing Movie Titles
- **Tokenization**: Movie titles are tokenized to convert them into sequences of integers.
- **Padding**: The sequences are padded to ensure they have a uniform length, making them suitable for input into the neural network.

### 4. Managing Movie IDs
- **Indexing**: Movie IDs are indexed to provide a unique identifier for each movie.
- **Handling NaN Values**: Special attention is given to handle NaN values in the movie ID column to ensure data integrity.

## Model Architecture
The neural network model used in this project includes several layers and components:

- **Embedding Layers**: Separate embedding layers are utilized for movie titles and IDs to convert these features into dense vectors of fixed size.
- **Convolutional Neural Network (CNN)**: Applied to the embedded title representations to capture local patterns.
- **Concatenation Layer**: Combines features from different sources (IDs, genres, titles) into a single vector.
- **Fully Connected (Dense) Layers**: These layers are used after concatenation to further process the combined features.
- **Output Layer**: Consists of a single neuron that predicts the movie rating based on the processed features.

## Training the Model
The model is trained using the processed features from the MovieLens dataset. Key aspects of the training process include:

- **Splitting the Dataset**: The dataset is split into training and validation sets to enable model evaluation.
- **Model Compilation**: The model is compiled with an appropriate optimizer, loss function, and evaluation metrics.
- **Model Fitting**: The model is trained on the training set and its performance is validated on the validation set.

## Challenges Encountered and Solutions
Throughout the development of this project, several challenges were encountered:

- **Data Preprocessing**: Handling NaN values and ensuring data types were correct required careful data preprocessing.
- **Model Architecture Tuning**: Adjustments were made to the model architecture to better suit the nature of the dataset.
- **Debugging Training Issues**: Addressing issues like decreasing accuracy during training involved revisiting data preprocessing and model configuration.

## Future Enhancements
The following areas are identified for future improvements:

- **Expand Feature Set**: Incorporating additional features such as user data might enhance the model's performance.
- **Optimization**: the model is not very ideal and we have to think more about the reason of low accuracy.
- **Advanced Model Architectures**: Experimenting with more complex neural network architectures, such as recurrent neural networks (RNNs) or Transformers, could be beneficial.
- **Hyperparameter Optimization**: Systematic tuning of hyperparameters might yield better results.