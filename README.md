# 🎬 Recommendation System 

A **Movie Recommendation System** built using **Machine Learning
techniques** (no deep learning).\
This project explores **Collaborative Filtering (User-User &
Item-Item)** and **Matrix Factorization (FunkSVD)** on the [MovieLens
100k Dataset](https://grouplens.org/datasets/movielens/100k/).

------------------------------------------------------------------------

## 📊 Features

-   User-User Collaborative Filtering\
-   Item-Item Collaborative Filtering\
-   Matrix Factorization using FunkSVD (with biases)\
-   Evaluation using **RMSE, Precision@K, Recall@K**\
-   Generate **Top-N recommendations** for a given user\
-   Human-readable outputs (movie titles, not just IDs)

------------------------------------------------------------------------

## 🗂️ Project Structure

    recommendation-system-ml/
    │── data/                # Dataset (MovieLens 100k)
    │── notebooks/           # Jupyter notebooks (EDA + experiments)
    │── src/                 # Source code
    │   ├── preprocessing.py
    │   ├── collaborative_filtering.py
    │   ├── matrix_factorization.py
    │   ├── evaluation.py
    │── app/                 # (Optional) Streamlit web app
    │── results/             # Evaluation results, plots
    │── README.md            # Project documentation
    │── requirements.txt     # Python dependencies

------------------------------------------------------------------------

## 📂 Dataset

We use the **MovieLens 100k** dataset, which contains **100,000
ratings** from **943 users** on **1,682 movies**.

Download link: [MovieLens
100k](http://files.grouplens.org/datasets/movielens/ml-100k.zip)

------------------------------------------------------------------------

## ⚙️ Installation

1.  Clone this repository:

    ``` bash
    git clone https://github.com/Arghadeepkar85/recommendation-system-ml.git
    cd recommendation-system-ml
    ```

2.  Create virtual environment & install dependencies:

    ``` bash
    pip install -r requirements.txt
    ```

3.  Download and extract the dataset:

    ``` bash
    python src/download_dataset.py
    ```

------------------------------------------------------------------------

## ▶️ Usage

Run the full pipeline (training + evaluation):

``` bash
python src/main.py
```

Example Output:

    RMSE Item-based CF: 1.0038
    RMSE User-based CF: 1.0053
    RMSE Matrix Factorization (FunkSVD): 0.9102

    Top-10 Recommendations for User 1:
    1. Star Wars (1977) – Predicted rating: 4.74
    2. Fargo (1996) – Predicted rating: 4.68
    3. Shawshank Redemption (1994) – Predicted rating: 4.56
    ...

------------------------------------------------------------------------

## 📈 Results

-   **User-based CF RMSE**: \~1.00\
-   **Item-based CF RMSE**: \~1.00\
-   **Matrix Factorization RMSE**: \~0.91\
-   Precision@10 and Recall@10 show that MF produces better
    recommendations.

------------------------------------------------------------------------

## 🚀 Future Improvements

-   Implement **Hybrid Recommender Systems** (CF + Content-based)\
-   Add **implicit feedback handling** (clicks, views)\
-   Scale with **Spark ALS** for large datasets\
-   Deploy as a **Streamlit Web App**

------------------------------------------------------------------------

## 🛠️ Tech Stack

-   Python 3.x\
-   Pandas, NumPy, SciPy\
-   Scikit-learn\
-   Matplotlib / Seaborn (for plots)

------------------------------------------------------------------------

## 📜 License

This project is licensed under the MIT License -- see the
[LICENSE](LICENSE) file for details.

------------------------------------------------------------------------


