# kwa
import tweepy

# Twitter API credentials
consumer_key = 'your_consumer_key'
consumer_secret = 'your_consumer_secret'
access_token = 'your_access_token'
access_token_secret = 'your_access_token_secret'

# Authenticate to Twitter
auth = tweepy.OAuth1UserHandler(consumer_key, consumer_secret, access_token, access_token_secret)

# Create API object
api = tweepy.API(auth)

# Your tweet content
tweet_content = "Hello, world! This is a test tweet from my Python script."

# Post a tweet
try:
    api.update_status(tweet_content)
    print("Tweet posted successfully!")
except tweepy.TweepError as e:
    print("Error posting tweet:", e)
