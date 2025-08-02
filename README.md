# Music Recommender System

A content-based music recommendation system that suggests similar songs based on lyrics analysis. This project uses natural language processing techniques to analyze song lyrics and recommend songs with similar themes and content.

## Table of Contents
- [Features](#features)
- [How It Works](#how-it-works)
- [Dataset](#dataset)
- [Technologies Used](#technologies-used)
- [Installation](#installation)
- [Usage](#usage)
- [Project Structure](#project-structure)
- [How to Run](#how-to-run)
- [Future Improvements](#future-improvements)

## Features

- **Content-Based Recommendations**: Recommends songs based on lyrical content similarity
- **Spotify Integration**: Displays album artwork using the Spotify API
- **User-Friendly Interface**: Built with Streamlit for an intuitive web interface
- **Real-time Recommendations**: Get 5 song recommendations with a single click

## How It Works

1. **Text Preprocessing**: Song lyrics are cleaned and normalized
2. **Feature Extraction**: TF-IDF vectorization converts lyrics to numerical features
3. **Similarity Calculation**: Cosine similarity measures lyrical similarity between songs
4. **Recommendation Generation**: Top 5 most similar songs are suggested based on content

## Dataset

The system is trained on a dataset of song lyrics (`spotify_millsongdata.csv`) containing:
- Song names
- Artist names
- Lyrics text
- Spotify links

The dataset is preprocessed to remove irrelevant columns and clean the text data before training.

**Dataset Source**: The dataset used in this project is from Kaggle: [Spotify Million Song Dataset](https://www.kaggle.com/datasets/notshrirang/spotify-million-song-dataset)

## Technologies Used

- **Python**: Core programming language
- **Streamlit**: Web application framework
- **Spotify API**: For fetching album artwork
- **NLTK**: Natural language processing library
- **Scikit-learn**: Machine learning library for TF-IDF and cosine similarity
- **Pandas**: Data manipulation and analysis
- **Pickle**: Model serialization

## Installation

1. Clone the repository:
```bash
git clone https://github.com/your-username/music-recommender-system.git
cd music-recommender-system
```

2. Install required dependencies:
```bash
pip install -r requirements.txt
```

3. Set up Spotify API credentials:
   - Create a Spotify Developer account
   - Create an app to get your `CLIENT_ID` and `CLIENT_SECRET`
   - Update these credentials in `app.py`

## Usage

1. Run the Streamlit application:
```bash
streamlit run app.py
```

2. Select a song from the dropdown menu
3. Click "Show Recommendation" to get similar song suggestions
4. View the recommended songs with their album artwork

## Project Structure

```
music-recommender-system/
├── app.py                 # Streamlit web application
├── Model Training.ipynb   # Jupyter notebook for model training
├── df.pkl                 # Pickled song data
├── similarity.pkl         # Pickled similarity matrix
├── spotify_millsongdata.csv # Original dataset
├── requirements.txt       # Python dependencies
└── README.md             # This file
```

## How to Run

1. Ensure all dependencies are installed
2. Update Spotify API credentials in `app.py`
3. Run the application:
```bash
streamlit run app.py
```
4. Access the application in your web browser at `http://localhost:8501`

## Future Improvements

- Add user authentication and personalized recommendations
- Include audio features (tempo, key, etc.) in the recommendation algorithm
- Implement collaborative filtering for more diverse recommendations
- Add a search functionality for songs not in the dropdown
- Deploy the application to a cloud platform for public access

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
