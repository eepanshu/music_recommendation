***Objective***
Create an unsupervised K-Means learning model that categorizes songs into a set number of groups, then evaluate the accuracy of the song recommendation function.

**Introduction**
Imagine it is after school and you are preparing for a study session. As you set up your study area, create a plan, and gather the necessary materials, you open a music streaming platform on your device. Initially, you contemplate playing your go-to study playlist, but you decide to explore the platform's personalized playlist recommendations instead.

This gets you thinking about the intricate process behind the platform's song suggestions. It's fascinating: With a vast catalog spanning millions of songs, the platform consistently recommends tracks that match your musical tastes. Music services like Spotify can do this with the help of artificial intelligence.

Artificial Intelligence (AI) is a branch of computer science focused on building tools that can solve problems and analyze information. Machine learning is a subdivision of AI. Its goal is to create tools that can learn and improve over time using data. Machine learning encompasses various techniques, including supervised learning, in which models are trained on labeled data to make predictions, and unsupervised learning, in which models uncover patterns and relationships within data without explicit labels.

K-Means is an unsupervised machine learning algorithm that groups similar data points together into clusters, with the goal of minimizing the differences within each cluster and maximizing the differences between clusters. It is commonly used for tasks like recognizing patterns and making recommendations.

K-Means outperforms manual data analysis because it is more efficient in terms of time and effort. It is great at finding complex patterns that might be hard for people to see. K-Means is consistent and works well with both small and large datasets. It can adjust to changes quickly and make decisions automatically. It is also good at handling data with many details.

However, K-Means has some limitations. Selecting the appropriate number of clusters (K) can be challenging and subjective. K-Means also struggles with datasets that contain outliers or features of varying importance. Despite these limitations, K-Means is a valuable tool when used carefully and in combination with preprocessing techniques that enhance its performance.

K-Means exemplifies the ability of machine learning algorithms to uncover patterns and make data-driven decisions. Companies and researchers are interested in K-Means for a variety of uses. Companies like Spotify or Netflix, for instance, may use K-Means to automatically generate recommendations for their users, enhancing user engagement and satisfaction.

In this project, we will give you the basic code for implementing the K-Means model. Your job is to use this code and see how well it can recommend songs that you will enjoy.

The dataset you will be using contains information about 24 features of songs on Spotify:

Artist: The artist's name
Track: The title of the track
Album: The name of the album
Album_type: The type of album (Album, Single, Compilation)
Danceability: A measure of how suitable a song is for dancing. It quantifies the rhythm, tempo, and beat strength of a track. Spotify uses machine learning algorithms to analyze these features and assign a danceability score to each song. The score typically ranges from 0 to 1, where higher values indicate more danceable tracks.
Energy: A measure of the intensity and activity level of a song. It reflects how dynamic and lively a track feels. Energy is calculated by analyzing its loudness and dynamic range. It is assigned a value from 0 to 1.
Loudness: The perceived volume or intensity of a song. Spotify quantifies Loudness using Loudness Units Full Scale (LUFS), a standardized unit of measurement used in audio engineering and music analysis. It takes into account human perception of loudness, making it suitable for music and audio content. The LUFS scale is designed to measure consistent loudness levels across different audio sources.
Speechiness: A measure of the extent to which a segment of audio or an entire song contains spoken words, vocalizations, or non-musical sounds, as opposed to instrumental music. It is a valuable metric for categorizing and understanding the nature of audio content. Speechiness is calculated by analyzing audio frames from a song and classifying them as speech or non-speech based on acoustic features, then calculating the proportion of frames classified as speech. The result is a Speechiness score ranging from 0 to 1, where higher values indicate a greater presence of spoken words or vocal content in the song compared to instrumental music.
Acousticness: A measure of the degree of acoustic instrumentation and arrangements in a song, distinguishing between music dominated by traditional acoustic instruments and that featuring electronic or synthesized sounds. It is calculated by dividing the song's acoustic frames by its non-acoustic (electronic) frames. The result is a numerical Acousticness score, typically ranging from 0 (highly electronic) to 1 (purely acoustic).
Instrumentalness: A numerical measure that quantifies instrumental content in a song, helping differentiate between purely instrumental tracks and those with vocals. To calculate Instrumentalness, the audio waveform is divided into frames, and machine learning algorithms or statistical models classify each frame as instrumental or non-instrumental based on acoustic features. The aggregated result is an Instrumentalness score typically ranging from 0 (vocal-heavy) to 1 (purely instrumental).
Liveness: A numerical measure that gauges the presence of live performance characteristics in a song, distinguishing between studio and live concert recordings. To calculate liveness, audio analysis considers features such as crowd noise, audience reactions, and instrumentation variations. Machine learning models classify audio segments as live or studio based on these features, resulting in a Liveness score typically ranging from 0 (studio recording) to 1 (live performance).
Valence: A numerical measure that quantifies the emotions or mood of a song, indicating whether it conveys positivity or negativity. It is determined through the analysis of various musical elements, including lyrics, melody, harmony, tempo, and instrumentation. Valence scores typically range from 0 (negative or sad) to 1 (positive or happy).
Tempo: A measure of the speed or pace at which a piece of music is performed. It is typically measured in beats per minute (BPM). It quantifies the rhythm and timing of a composition, with a higher BPM indicating a faster tempo and a lower BPM indicating a slower tempo. Tempo is calculated by detecting and counting the beats in music over a one-minute interval.
Duration_min: A measure of how long a song is in minutes
Title: The title of the music video
Views: The number of views a music video has on YouTube
Likes: The number of likes a music video has on YouTube
Comments: The number of comments a music video has on YouTube
Licensed: When a song is "licensed," it means that the rights to use that song for specific purposes or in certain contexts have been legally granted by the copyright holder (typically the songwriter, composer, or music publisher) to another party.
official_video: Whether or not a music video is official. An "official" music video is a video authorized and released by the copyright holders, such as the artist or record label. These videos are professionally produced, widely distributed through official channels, and subject to copyright protection, distinguishing them from unofficial or fan-made videos.
Stream: The number of times a track has been played on Spotify
EnergyLiveness: A custom feature for this dataset that combines the Energy and Liveness features
most_playedon: The platform that the track has been played the most on, either Spotify or YouTube
Taken together, these 24 features are intended to describe how a song sounds and its appeal to listeners. These factors are crucial for artists and music platforms in creating and recommending music that resonates with listeners.

Terms and Concepts
Artificial Intelligence (AI)
Machine Learning
Supervised Learning
Unsupervised Learning
K-Means
Noise
Normalization
Scaling
Dimensionality
Principal Component Analysis (PCA)
Cluster
