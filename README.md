## Movie Recommender System
![image](https://github.com/GeetGhai/Movie_recommender_Sys/assets/154088899/94b4ff51-be82-404b-a66f-297c80e8b28b)


### Overview

This project is a Movie Recommender System that uses various features from movie data to suggest similar movies. The recommender system is built using Python and leverages natural language processing techniques to analyze movie metadata and provide recommendations.

### Project Structure

The project is organized in a Jupyter notebook format with the following main sections:

1. **Data Loading and Preprocessing**: Loading the movie dataset and preparing it for analysis.
2. **Feature Extraction**: Extracting important features from the dataset, such as genres, keywords, cast, and crew.
3. **Text Vectorization**: Using techniques like TF-IDF to convert text data into numerical vectors.
4. **Similarity Computation**: Calculating similarity scores between movies based on their features.
5. **Recommendation Function**: Implementing the function to recommend movies based on a given input movie.
6. **Saving the Model**: Persisting the processed data and model for future use.

### Installation

To run the project, you need the following dependencies:

- Python 3.x
- pandas
- numpy
- scikit-learn
- pickle
- Jupyter Notebook

You can install these dependencies using pip:

```bash
pip install pandas numpy scikit-learn
```

### Usage

1. **Clone the Repository**: 
   ```bash
   git clone <repository-url>
   cd <repository-directory>
   ```

2. **Open the Jupyter Notebook**:
   ```bash
   jupyter notebook Movie-Recommender-system.ipynb
   ```

3. **Run the Cells**: Execute the cells in the notebook to load data, preprocess it, compute similarity, and save the models.

4. **Get Recommendations**: Use the `recommend` function to get movie recommendations. For example:
   ```python
   recommend('Avatar')
   ```

### Data

The dataset used in this project includes the following features:
- `id`: Unique identifier for each movie.
- `title`: The title of the movie.
- `genres`: List of genres associated with the movie.
- `keywords`: List of keywords describing the movie.
- `overview`: Brief summary of the movie.
- `cast`: List of main actors in the movie.
- `crew`: List of main crew members, including the director.

### Feature Extraction

The following features are extracted and used for computing similarity:
- Genres
- Keywords
- Cast
- Crew
- Overview

These features are combined into a single string for each movie and vectorized using TF-IDF.

### Similarity Computation

Cosine similarity is used to calculate the similarity between the TF-IDF vectors of movies. This results in a similarity matrix, where each element represents the similarity score between two movies.

### Recommendation Function

The `recommend` function takes a movie title as input and returns a list of similar movies based on the similarity matrix.

### Saving the Model

The processed data and similarity matrix are saved using the pickle module for future use. The following files are generated:
- `movies.pkl`: Pickled DataFrame containing movie information.
- `similarity.pkl`: Pickled similarity matrix.

### Example

```python
# Load the processed data and similarity matrix
movies_list = pickle.load(open('movies.pkl', 'rb'))['title'].values
similarity = pickle.load(open('similarity.pkl', 'rb'))

# Get recommendations
print(recommend('Avatar'))
```
![image](https://github.com/GeetGhai/Movie_recommender_Sys/assets/154088899/ffa6cf33-6da4-46d6-976e-9219252ed12d)

### Conclusion

This Movie Recommender System provides a simple yet effective way to suggest similar movies based on various features extracted from the movie dataset. By following the steps outlined in this README, you can set up and run the recommender system on your own machine.
