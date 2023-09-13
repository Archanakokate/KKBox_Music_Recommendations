## LetsGrowMore Internship Project - DataScience
### Task-3
## KKBox Music Recommendations

The primary goal of this project is to develop a robust predictive model that accurately identifies the likelihood of users listening to a song repetitively on KKBOX. By understanding user behavior and preferences, we aim to improve the music recommendation system and enhance the overall user experience on the platform.

The dataset is from KKBOX, Asia’s leading music streaming service, holding the world’s most comprehensive Asia-Pop music library with over 30 million tracks.
In this task, we predict the chances of a user listening to a song repetitively after the first observable listening event within a time window was triggered. If there are recurring listening event(s) triggered within a month after the user’s very first observable listening event, its target is marked 1, and 0 otherwise in the training set. The same rule applies to the testing set.

KKBOX training data set consists of information of the first observable listening event for each unique user-song pair within a specific time duration. Metadata of each unique user and song pair is also provided. The train and the test data are selected from users listening history in a given time period.

### Dataset link: 
  https://www.kaggle.com/c/kkbox-music-recommendation-challenge/data

### Dataset Description

### 1) train.csv
  msno: user id
  song_id: song id
  source_system_tab: the name of the tab where the event was triggered. System tabs are used to categorize KKBOX mobile apps functions. 
  source_screen_name: name of the layout a user sees.
  source_type: an entry point a user first plays music on mobile apps. An entry point could be album, online-playlist, song .. etc.
  target: this is the target variable. target=1 means there are recurring listening event(s) triggered within a month after the user’s very first observable listening event, target=0 otherwise .

### 2) test.csv
id: row id (will be used for submission)
  msno: user id
  song_id: song id
  source_system_tab: the name of the tab where the event was triggered. 
  source_screen_name: name of the layout a user sees.
  source_type: an entry point a user first plays music on mobile apps. An entry point could be album, online-playlist, song .. etc.

### 3) songs.csv
  song_id
  song_length: in ms
  genre_ids: genre category. Some songs have multiple genres and they are separated by |
  artist_name
  composer
  lyricist
  language
  
### 4) members.csv
  msno
  city
  bd: age. Note: this column has outlier values, please use your judgement.
  gender
  registered_via: registration method
  registration_init_time: format %Y%m%d
  expiration_date: format %Y%m%d
  song_extra_info.csv

### 5) song_id
  song name - the name of the song.
  isrc - International Standard Recording Code, theoretically can be used as an identity of a song.  
