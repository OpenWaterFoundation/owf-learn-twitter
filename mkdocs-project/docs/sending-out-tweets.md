# Sending Out Tweets #
This page is dedicated to outlining different ways that an organization can send out tweets, either using a single organizational account or multiple accounts.

This page also covers the different ways of contacting your followers, either by public tweet, or private direct messaging.

## Organizational Account ##

### Overview ###
The simplest solution to sending out tweets is to [create a general organizational twitter account](http://localhost:8000/twitter-account-setup/#create-official-business-account), where all tweets are posted from. This approach requires the overhead of setting up a single twitter account, which is convenient in only needing a single email associated with that account.  
With a single organizational account you can post updates to all of your followers, that can either be related to a whole system, or can be related to a specific location, such as location on a river, reservoir, etc.  

Hashtags can be used to label tweets as either being related to a specific location, or the whole system. Followers can then use Twitter's search to filter through tags:

### Search Options on Twitter ###
#### Search Bar ####
There are a several ways to narrow your results through Twitter search. The most basic search can be done by typing in the name of a page or a hashtag into the Twitter search bar. If you'd like to have more specific results you can combine a hashtag with a Twitter account name. This limits results to only posts from that Twitter account with the associated hashtag.  

#### Advanced Search ####
On the left side of the results page you can select more search filters by clicking **show** next to **Show filters**. From here you can add different filters, or you can select **Advanced search**, for many more search options. On this page you can specify the account/accounts you want to filter by, as well as listing one or more hashtags. There are plenty of other options to further narrow your result.


## Multiple Accounts ##

Another option is to set up multiple Twitter accounts for each specific location. This approach has the benefit of allowing your followers to follow only the accounts that are of interest to them. Instead of having to search through all the information on the main organizational account, followers can get notifications only from the account with the specific location they desire.  
The disadvantage of setting up multiple accounts is the amount of maintenance required for each account. Setting up multiple accounts requires also setting up multiple emails to link to each account.

## Personal Accounts ##
A third option for setting up twitter accounts to communicate with followers includes creating separate individual personal accounts for people associated with the organization. This requires setting up each person with a professional twitter account and emails to attach to each of those accounts.  
In this situation followers would need to follow the personal accounts of those associated with the organization, or the organization would need to keep up on retweeting posts from the personal accounts.  
There may be a way to automate this retweet process, but this will require more research, and is not obviously apparent how to accomplish using twitterOAuth.

## Public Tweets ##
The most obvious and straight forward method of communicating with your followers is through the posting of public tweets on your account, whether that be on a general organizational account or on specific accounts.  
Hashtags can be used to specify what type of tweet the post is, or to label the tweet with related information, such as a specific location.
Posting a tweet using [twitterOAuth](https://github.com/abraham/twitteroauth):
```php
$twitteroauth->post('statuses/update', array('status' => 'status text here'));
```

## Direct Messaging ##
Another option for communicating with followers is by sending out direct messages. This approach will require a bit more set-up to accomplish. To send a direct message through any of the twitter libraries, or through using the [Twitter API](/twitter-api.md) will require obtaining all of the users you want to contact and configuring this information in whatever development tool you are using.  
Direct messaging using [twitterOAuth](https://github.com/abraham/twitteroauth):
```php
$twitteroauth->post('direct_messages/new', array('text' => 'dm text here', 'screen_name' => 'recipients screen_name'));
```
See [Twitter Mobile Notifications](/twitter-mobile-notifications.md) for how followers can configure their cell phones to receive direct messages and updates from your account/accounts.
