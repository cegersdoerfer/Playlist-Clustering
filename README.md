# Playlist Clustering
This repository gathers Spotify user playlists and clusters songs by similarity based on audio features using a self organizing map

# Audio features
Spotify provides a set of audio features for every song on its platform. These audio features are used in this repository to calculate similarity of songs in a given playlist. To explore more information about each audio feature, spotify provides this resource: https://developer.spotify.com/documentation/web-api/reference/#/operations/get-several-audio-features

# Playlist analysis
Once the user has entered their spotify credentials and chosen the playlist to analyze, the playlist is analyzed given the audio features for each song contained in the playlist. A histogram is created for each audio feature to visulaize the general representation of that feature in the playlist

![graphs_analysis](https://user-images.githubusercontent.com/29511758/148264166-95041b4d-cd7a-4e5c-833f-39e845f51b1b.png)

# Self Organizing Map
Self organizing maps are simple, yet effective neural networks which constist of only an input layer and a two dimensional map of neurons as shown in the image below.

![SOM](https://user-images.githubusercontent.com/29511758/148267528-bd278751-0072-4bad-aee2-7534056a06a6.png)

It is simplest to imaging this network creating a mask over a given set as it learns, where a new input pulls the closest neuron (and some of it's neighbors) towards itself until the neurons effectively represent the input. This process is effectively represented in the gif below

![440px-TrainSOM](https://user-images.githubusercontent.com/29511758/148269536-5f841a5f-5795-46b5-b074-2e386908eeff.gif)

# Playlist clusters
Once the SOM has trained on the given playlist, the clusters (in this case 3) are created. The specific differences in audio features between all clusters is represented in the graphs below

![cluster analysis](https://user-images.githubusercontent.com/29511758/148269726-8a747118-85b0-405a-941a-8abd43d0650f.png)

And as a way of further visualizing the differences between clusters, this radial chart shows the emphasis on each feature by each cluster

![radial map](https://user-images.githubusercontent.com/29511758/148270391-d926dc30-610f-4c93-9fce-95bd335d0fd8.png)


