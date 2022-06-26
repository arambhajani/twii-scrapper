# Twii-scrapper
twitter scrapper to scrap top 15 hashtags and visualize using the tweet count and also develop word cloud
-------------------------------------------------------------------------------------------------------------------------------------------------------------------------

## Library used 
1 advertools
2 matplotlib.pyplot
3 seaborn 
4 pandas 
5 wordcloud
## Authentication
auth_params = {<br>
//Use your api key here <br>
'app_key': "twitter_app_key",<br>
'app_secret': "app_scret_by twitter" ,<br>
'oauth_token': "Secret_Token",<br>
'oauth_token_secret':"Secret_token_key",<br>
}<br>
adv.twitter.set_auth_params(**auth_params)
## Vizulization
### Top 15 hashtag for date 26/06/2022 (Bar Graph)
![top 15 bar graph](https://user-images.githubusercontent.com/94845722/175822521-349dc7eb-27e9-483b-b248-cd0260a3a926.png)

### Top 15 hashtag for date 26/06/2022 (Word Cloud)
![word cloud](https://user-images.githubusercontent.com/94845722/175822601-f48e7090-76d8-4313-8869-88980ddc6591.png)
