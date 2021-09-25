# Song_Recommender_Project

![image](https://github.com/elesalgueiro/Song_Recommender_Project/blob/main/ReadMe_image.jpg)

### PROJECT DESCRIPTION
Most of us now use AI-based recommender systems every day: looking for a film o show on Netflix,  watching “up next” videos on YouTube, or listening to “Discover Weekly” playlists on Spotify.
The idea of this project was to create a song recommender based on characteristics of the user's input (a song they love)
I love music and I am one of those listeners that get excited on Monday morning to see what it´s new in my  Spotify Discover Weekly playlist so I enjoyed doing this project a lot. 
### THE DATA
Using Spotify’s Web API I create a data set of 10K songs with the artist, title, and Spotify audio feature characteristic for each one.
There are 12 audio features for each track, including confidence measures like acousticness, liveness, speechiness, and instrumentalness, perceptual measures like energy, loudness , danceability and valence (positiveness), and descriptors like duration , tempo , key, and mode
(Information about Spotify audio features in this link: 
By web scraping the Billboard website, I get a list of the TOP100 hot songs. I specifically retrieved the title and artist of those hits.
### WORKFLOW
After having our song lists I cluster the 10K songs I got from Spotify web API. I worked with K-means clustering which is one of the simplest and most popular unsupervised machine learning algorithms. 
Clustering the songs will allow the recommendation system to limit the scope of the recommendations to only songs that belong to the same cluster - songs with similar audio features.
Then I create a pipeline such that when the user enters a song :
1 -Check whether or not the song is in the Billboard Hot 100.
1.1 -If the song is in that list suggest the user another song from this list --> END
1.2 -If the song is not in the Billboard Hot 100 -->
1.2.1 -Collect the audio features from the song with the Spotify API.
   		1.2.2-After that,  send the Spotify audio features of the submitted song to the clustering model, which should return a cluster number.
   		1.2.3 -The system recommends another song to the user from the same cluster -->END
         
 ![](https://github.com/elesalgueiro/Song_Recommender_Project/blob/main/Recommender_engine/Flowchart.png)
 
 
### LINKS

Billboard web scrapping code
Spotify API code
Song Recommender code

