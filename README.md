# Movie Recommendation System

## Overview
This project implements a content-based movie recommendation system using the TF-IDF vectorization technique and cosine similarity. It takes a user's favorite movie as input and recommends similar movies based on various attributes like genres, keywords, cast, and director.

## Dataset
The dataset used in this project is `movie_metadata.csv`, which contains information about 5,043 movies with 26 different features, including:
- `genres`
- `keywords`
- `cast`
- `director`
- `movie_title`
- `imdb_score`
- `budget`
- `country`

## Features Used for Recommendation
The recommendation system utilizes the following features to determine movie similarity:
- `genres`
- `keywords`
- `cast`
- `director`

## Installation & Dependencies
Ensure you have Python installed and install the required libraries:
```sh
pip install numpy pandas scikit-learn Flask
```

## How It Works
1. **Load Dataset**: Read the `movie_metadata.csv` file using pandas.
2. **Data Preprocessing**:
   - Handle missing values by replacing them with an empty string.
   - Combine selected features into a single string for each movie.
3. **Feature Extraction**:
   - Convert the combined text data into numerical feature vectors using `TfidfVectorizer`.
4. **Calculate Similarity Scores**:
   - Compute cosine similarity between movie feature vectors.
5. **User Input**:
   - The user provides a movie name.
   - The system finds the most similar movies using cosine similarity scores.

## Web Interface
A Flask web application is implemented for user interaction. Users can enter a movie name in a simple web UI and receive recommendations.

### Running the Web App
```sh
python app.py
```
Then, open `http://127.0.0.1:5000/` in your browser.

## Example Usage
1. **Command Line**:
```sh
python movie_recommendation.py
```
Example:
```
Enter your favourite movie name: Avatar
Recommended movies:
1. Pirates of the Caribbean: At World's End
2. Spectre
3. The Dark Knight Rises
4. John Carter
5. Spider-Man 3
```

2. **Web Application**:
- Open the Flask web interface.
- Enter a movie title in the input field.
- Get a list of recommended movies displayed on the page.

## Future Enhancements
- Include IMDb ratings in recommendations.
- Implement collaborative filtering.
- Deploy as a web application on a cloud platform.

## License
This project is licensed under the MIT License.

