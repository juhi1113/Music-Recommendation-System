# Emotion-based Music Recommender System 

[![Spotify](https://img.shields.io/badge/Spotify-1ED760?&style=for-the-badge&logo=spotify&logoColor=white)](https://open.spotify.com/)

## Abstract

- Song recommendations have existed for a long time, but in most scenarios, the recommendation is determined after learning the user's preferences over a period of time, like looking at their past song preferences, the time they listen to music, etc.
- In this project, we propose a new approach to song recommendation, where the mood of a person is determined from their picture, and based on the predicted mood, song recommendations are made that best suit the predicted mood.

## Description

1. The image of the user taken as input is processed with the help of a Python library for Computer Vision called 'OpenCV'. This captured image is then made available for the CNN in combination with DNN to make a prediction whether the current mood of the user is 'Happy' or 'Sad'.
2. The second part involves the usage of Unsupervised Machine Learning techniques for clustering songs. The songs are clustered as either of the two classes - 'VERY ENTERTAINING' (class 0) and 'RELAXED' (class 1) using the popular K-means algorithm. Then the recommendation is made in order of the current popularity of the respective songs.
3. A unique approach is adopted in the way songs are recommended for each mood. For example, when other sites recommend sad songs when a person is sad or feeling bad, this system recommends users with songs that will cheer them up ('VERY ENTERTAINING'), and 'RELAXING' songs when they are 'HAPPY'.
4. The code to train the neural network can be found in the 'Emotion_detector_version2' iPython notebook. If anyone wants to modify the network to suit their particular needs or feels it is necessary to tweak the network, they can do so by making changes to the code present there. The model created is saved as 'final_model.h5'.

## Data

The data used in this project is from [Spotify Dataset 19.21.20 - 160K+ Tracks](https://www.kaggle.com/yamaerenay/spotify-dataset-19212020-160k-tracks). The file contains more than 160,000 songs collected from the Spotify Web API, and you can also find data grouped by artist, year, or genre in the data section. It has features like acousticness, energy, loudness, and danceability, which make the clustering algorithm work more effectively.

## Libraries Used

- OpenCV
- TensorFlow and Keras
- Scikit-learn
- LightGBM
- Spotipy
- Tkinter
- Pillow

## How to Use

1. This application can be used by executing the `run.py` file, which then opens up a GUI asking the user to enter the name of the artist.
2. This will then collect the required albums from the API and open up your webcam.
3. Click the 'q' button on the keyboard to stop capturing the image, and the GUI will guide you through the process.
4. Clicking on the 'Print' button will display the recommendations for you.
