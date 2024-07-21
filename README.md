# Record Label Manager Strategic planning (EDA-Spotify-2024)

## Executive Summary
Hypothetical manager of record label is interested in artist portfolio and nature of pop music scene. Wants to know what is currently popular and what factors to consider when pushing out a strategy for their artists. 
To do this I used a Spotify dataset from [kaggle](https://www.kaggle.com/datasets/nelgiriyewithana/most-streamed-spotify-songs-2024/data) to consolidate learnings on EDA techniques involving:
<li>Data cleaning and string transformation</li>
<li>Initial analytics and scoping</li>
<li>Visualisation of insights

After the analysis of the dataset I then provided a recommendation of what plan of action to do in order for their artist to succeed in popularity and charting.

#### Tool used: Python| Pandas| Seaborn| Matplotlib| Data Manipluation| Data Visualisation

## Insights looking to uncover were:
1. [Who has the most albums released in spotify? ](#who-has-the-most-albums-released-in-spotify?)
2. [Do most albums released equate to most streamed artist? ](#do-most-albums-released-equate-to-most-streamed-artist?)
3. [Is there a correlation between explicit songs and artist popularity? ](#is-there-a-correlation-between-explicit-songs-and-artist-popularity?)
4. [What is the most streamed song on different platforms? ](#what-is-the-most-streamed-song-on-different-platforms?)
5. [Are the top ranked songs one hit wonders/from new artists? ](#are-the-top-ranked-songs-one-hit-wonders/from-new-artists?)

## Findings 

### Who has the most albums released in spotify? 

From a top level perspective we can see that Drake holds the most albums released on Spotify, followed by KAROL G and Peso Pluma. Knowing this, the next step is to determine if these artists are also the highest streamed on the platform to answer the question "Do most albums released equate to most streamed artist?".

![image](https://github.com/user-attachments/assets/4eefa658-9737-463c-a070-224c2aa69acb)


Assumptions carried from this is that Singles, EPs, and Collab Albums are also defined as Albums

### Is there a correlation between explicit songs and artist popularity?

Alongside figuring out this question, it would also be interesting to note if the level of explicity also correlates to the success of the artist. Using proportion of expliit songs we can then map out the percentage of which an artist is explicit and visualise this below 

![image](https://github.com/user-attachments/assets/94ed73ee-d80b-4443-a327-b0ad0e0570b9)

From here we can see that while there are artist such as Drake who has a high explicity rate who has a high level of songs streamed, Taylor Swift also has a low level of explicity and high streams. Interesting insight from this is The Weeknd is bang on in the middle and leading as most streamed artist on Spotify insinuating a balanced explicit artist would result in large amounts of streams.

Assumptions from this is that all Artists operate under the same genre as there is no genre datafield to source out

### Do most albums released equate to most streamed artist?

A cleaner visualisation of Top streamed artist can be seen here displaying the top 3 artist are: The Weeknd, Drake, Taylor Swift

![image](https://github.com/user-attachments/assets/d742aaea-c8df-4da1-baec-250ec56a8980)


Comparing this against our most albums released artists, only Drake is one of the top 3 streamed artist with Peso Pluma and KAROL G on the lower end of the top 10 streamed artists. This concludes the thought that most albums released does NOT equate to being a top streamed artist.

### What is the most streamed song on different platforms?

Initial analysis on this was to work on the most streamed platforms for: Spotify, Soundcloud, Pandora, Tidal. However after observing the amount of nulls on the dataset we saw a large amount of nulls on the different platform streams 

```
spotify_df.isnull().sum().sort_values(ascending=False)
```
![image](https://github.com/user-attachments/assets/7fc57ea0-6c73-4921-8858-19955db6085e)

So from here the new fields to analyse instead are playlist counts for: Spotify, Amazon, Deezer, Apple Music

![image](https://github.com/user-attachments/assets/c45c3f8e-361b-4f94-a7de-01da0832dba0)


From here we can see that both Apple and Spotify have the same track for number one song on playlist. To have a steady visualisation, we ommited Spotify as the playlist count is significnalty higher than the other platforms

![image](https://github.com/user-attachments/assets/12798df7-0983-4ebc-a597-56dd810d898f)



### Are the top ranked songs one hit wonders/from new artists?

Looking at the year of 2024, we see within the top 10 track sof all time ranking, 30% being from Artists who have only released less than 6 songs that have charted 
![image](https://github.com/user-attachments/assets/1fd31f56-4111-4653-ae81-0002ca103e6b)

Artists such as Tommy Richman, Artemas, FloyyMenor and Benson Boone are new to the scene. One hypothese for a source of popularity for up and coming artists is TikTok so we can visualise their popularity from this aswell. 

![image](https://github.com/user-attachments/assets/385a8e01-b9be-425a-984e-27dbd4708d47)

We can see that from this TikTok contributes heavily to arttists charting well onto the top 10 all time ranks.

### Artist Recommendations
Looking at the insights gained, the best plan of action for artists to performn well in popularity is to conduct these strategies: 
1. - Focus more on quality of tracks rather than quantity of albums released.
     - A mixtured portfolio of explicit songs and non explicit songs seem to performn best. </li>
2. - TikTok has a strong positive correlation to `All time Rank` for tracks so creating marketing campaigns with TikTok can help songs perform well in the charts</li>
     - To add to the above leverage TikTok by influencing users in using your songs that you want to chart

### Additional Steps
- A/B Test on tracking marketing assets for TikTok campaigns
- Deeper analysis on artist profile by genre (sourcing data fields with regards to additional musical fields) 




