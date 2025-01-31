# Movie Recommendation System

## About the Project

This project is a **Movie Recommendation System** built using **User-Based and Item-Based Collaborative Filtering** in **Python**. The system recommends movies to users based on their past interactions and ratings, leveraging collaborative filtering techniques.

## Dataset

We used the **MovieLens 100K Dataset**, which consists of **100,000 ratings** from **943 users** on **1,682 movies**.

For our system, however, we made use of two CSV files mainly, which are:

- **u.data (ratings)**
- **u.item (items)**

You can find the dataset on Kaggle:  
[MovieLens 100K Dataset](https://www.kaggle.com/datasets/prajitdatta/movielens-100k-dataset)

## Technologies Used

- **MongoDB & MongoDB Atlas**: For storing and managing the dataset.
- **Google Colab**: For developing and training the recommendation models.
- **Python Libraries**:
  - **pymongo** - Connecting MongoDB Atlas to Colab
  - **numpy & pandas** - Data processing and manipulation
  - **scipy.sparse** - Creating and handling sparse matrices
  - **sklearn.metrics.pairwise** - Calculating similarity matrices
  - **joblib** - Exporting trained models
  - **gradio** - Creating a GUI for user interaction

## Steps to Implement

### 1. Setting Up MongoDB Atlas

- Create a cluster in **MongoDB Atlas**.
- Connect cluster with MongoDB Compass.
- Obtain the **connection string** to link MongoDB Atlas with Colab.

### 2. Connecting MongoDB Atlas with Google Colab

- Use **pymongo** to establish a connection.
- Load data from MongoDB into **pandas DataFrames**.

### 3. Data Preprocessing

- Extract relevant columns (**user_id, movie_id, rating**).
- Map **movie_id** to **movie titles** for better readability.
- Convert DataFrames into structured formats.

### 4. Creating Sparse Matrix

- Convert the utility matrix (user-movie interactions) into a **sparse format** instead of a dense matrix to optimize memory usage.

### 5. Building Similarity Matrices

- **User-Based Similarity Matrix**: Using **cosine similarity**.
- **Item-Based Similarity Matrix**: Using **cosine similarity**.

### 6. Storing Similarity Matrices

- Save the **user-based** and **item-based similarity matrices** in `.npz` format to **Google Drive** for efficient access in the GUI notebook.

### 7. Collaborative Filtering

- Perform **User-Based Collaborative Filtering**.
- Perform **Item-Based Collaborative Filtering**.
- Generate recommendations based on similarity scores.

### 8. Exporting Models

- Use **joblib** to export trained recommendation models.
- Store them for reusability in the **GUI notebook**.

### 9. Creating GUI with Gradio

- Build an **interactive interface** using **Gradio**.
- Allow users to input their **user ID** and get **personalized movie recommendations**.

---

This repository provides an efficient **Movie Recommendation System** with an interactive user experience.

