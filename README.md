# MovieLens Recommender Algorithm Comparison

This project compares the performance of five collaborative filtering algorithms: KNNBasic, SVD, NMF, SlopeOne, and CoClustering. Using the MovieLens ml-latest-small dataset (100,836 ratings), each model was implemented with the Surprise library and evaluated using 5-fold cross-validation. The goal is to measure accuracy (RMSE, MAE), training time, and prediction time to determine which approach performs best for recommendation tasks.

## Dataset

MovieLens ml-latest-small  
- 100,836 ratings  
- 610 users  
- 9,742 movies  
- Rating scale: 0.5 to 5.0  

Source: GroupLens Research  
Dataset documentation included in `rec-movies/README.txt`.

## Algorithms Compared

- KNNBasic: Neighborhood-based collaborative filtering  
- SVD: Matrix factorization  
- NMF: Non-negative matrix factorization  
- SlopeOne: Item-based differences algorithm  
- CoClustering: User–item co-clustering  

## Methodology

All algorithms were evaluated using:  
- 5-fold cross-validation  
- RMSE  
- MAE  
- Fit time  
- Test time  

All experiments were conducted in Python using the Surprise library.

## Summary of Results

SVD achieved the lowest RMSE and MAE and provided the best balance of accuracy and speed. Other algorithms performed as follows:

| Algorithm      | RMSE    | MAE    | Notes                         |
|----------------|---------|--------|-------------------------------|
| SVD            | ~0.87   | ~0.67  | Best overall performance      |
| SlopeOne       | ~0.90   | ~0.69  | Moderate accuracy, very slow  |
| NMF            | ~0.92   | ~0.71  | Good accuracy, slower training|
| CoClustering   | ~0.95   | ~0.73  | Weak performance              |
| KNNBasic       | ~0.95   | ~0.73  | Baseline performance          |


Porject Structure
├── movielens/
│ ├── ratings.csv
│ ├── movies.csv
│ ├── tags.csv
│ ├── links.csv
│ └── README.txt
├── notebooks/
│ └── discussion19_1.ipynb
├── README.md
└── requirements.txt


## Running the Project

Install dependencies:



pip install -r requirements.txt


Open the notebook:



jupyter notebook notebooks/discussion19_1.ipynb


## Requirements

- Python 3.8 or higher  
- pandas  
- numpy  
- scikit-surprise  
- jupyter notebook  

## License

This project uses the MovieLens dataset under the GroupLens Research terms of use.

