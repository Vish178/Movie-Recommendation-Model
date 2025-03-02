# Movie Recommendation Model

This repository contains a Jupyter Notebook for building a movie recommendation model using the TMDB 5000 dataset.

## Files

- `MRM.ipynb`: The main Jupyter Notebook containing the code for the movie recommendation model.
- `tmdb_5000_credits.csv`: Dataset containing credits information for movies.
- `tmdb_5000_movies.csv`: Dataset containing detailed information about movies.

## Usage

1. Clone the repository:
    ```sh
    git clone https://github.com/your-username/Movie-Recommendation-Model.git
    cd Movie-Recommendation-Model
    ```

2. Install the required dependencies:
    ```sh
    pip install numpy pandas jupyter
    ```

3. Open the Jupyter Notebook:
    ```sh
    jupyter notebook MRM.ipynb
    ```

## Code Overview

### Importing Libraries

The notebook starts by importing the necessary libraries:
```python
import numpy as np
import pandas as pd
```
## Loading Datasets

Loading Datasets
The datasets are loaded using ```pandas```:

```python
movies = pd.read_csv("tmdb_5000_movies.csv")
crew = pd.read_csv("tmdb_5000_credits.csv")
```
## Data Processing
The notebook includes various data processing steps, such as cleaning and transforming the data. For example:
```python
df['cast'] = df['cast'].apply(lambda x: [i.replace(" ", "") for i in x])
df['genres'] = df['genres'].apply(lambda x: [i.replace(" ", "") for i in x])
```
## Example Output
The notebook provides example outputs for the processed data:
```python
recommend("Independence Day")
```
