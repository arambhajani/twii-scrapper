from wordcloud import WordCloud, STOPWORDS
import matplotlib.pyplot as plt
import seaborn as sea
import pandas as pd
import advertools as adv
auth_params = {
'app_key': "Your app_key provided by twitter ",
'app_secret': "Your app_secret provided by twitter " ,
'oauth_token': "Your oauth_token  by twitter ",
'oauth_token_secret':"Your oauth_token_secret provided by twitter ",
}
adv.twitter.set_auth_params(**auth_params)
trend = adv.twitter.get_place_trends(ids = 2282863 ) #id is for india it may change according to countries
print(trend.shape)
j=trend[:15] #top 15 hashtags 
j.head()
df=j[['name','tweet_volume','local_rank']]
df
plt.figure(figsize=(10,5))
sea.barplot(data=df,x=df.tweet_volume,y=df.name ,orient='h',palette="spring")
plt.title("Importance to be given to",fontsize=15)
plt.ylabel("hashtags",fontsize=12)
plt.xlabel("Volume",fontsize=12)
plt.show()

comment_words = ''
stopwords = set(STOPWORDS)
for val in df.name:
     
    # typecaste each val to string
    val = str(val)
 
    # split the value
    tokens = val.split()
     
    # Converts each token into lowercase
    for i in range(len(tokens)):
        tokens[i] = tokens[i].lower()
     
    comment_words += " ".join(tokens)+" "
    
 wordcloud = WordCloud(width = 1920, height = 1080,
                background_color ='white',
                stopwords = stopwords,
                min_font_size = 10).generate(comment_words)
plt.figure(figsize = (10, 10), facecolor = None)
plt.imshow(wordcloud)
plt.axis("off")
plt.tight_layout(pad = 0)
 
plt.show()
