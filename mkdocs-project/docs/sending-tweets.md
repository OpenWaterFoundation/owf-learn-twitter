# Sending Tweets #

This page describes different ways that an organization can send out tweets,
either using a single organizational account or multiple accounts.

This page also covers the different ways of contacting an account's followers,
either by public tweet, or private direct messaging.

* [Organizational Account](#organizational-account)
* [Multiple Accounts](#multiple-accounts)
* [Personal Accounts](#personal-accounts)
* [Public Tweets](#public-tweets)
* [Direct Messaging](#direct-messaging)

--------------

## Organizational Account ##

### Overview ###

The simplest solution to sending out tweets is to
[Create an Organizational Account](twitter-account-setup#create-organizational-account),
from which all tweets are posted. This approach requires the overhead of setting up a single twitter account,
which is convenient in only needing a single email associated with that account.  
The single organizational account can be used to post updates to all of followers using a message
related to a whole system.

Messages related to a specific location, such as location on a river, reservoir, etc.,
can also be posted and can be filtered based on hashtags.
Followers can then use Twitter's search to filter through tags.

### Search Options on Twitter ###

Twitter users cannot control what tweets they are sent once an account is followed.
Following many accounts or following an account that sends many tweets can therefore result in a large volume
of tweets being received.
It is possible to filter reading the tweets.

#### Search Bar ####

There are a several ways to narrow results through Twitter search.
A basic search can be done by typing in the name of a page or a hashtag into the Twitter search bar.
Searches can also combine a hashtag with a Twitter account name,
which will limit results to only posts from that Twitter account with the associated hashtag.
For example:  `openwaterfoundation #snodas`.

#### Advanced Search ####

The left side of the results page provides more search filters by clicking ***show*** next to ***Show filters***.
From here different filters can be added, or select ***Advanced search*** for access to several more search options.
Specify the account/accounts to filter by, as well as listing one or more hashtags.
Other options are also available to further narrow your result.

## Multiple Accounts ##

Another option is to set up multiple Twitter accounts, such as a separate account for each specific location.
This approach has the benefit of allowing your followers to follow only the accounts that are of interest to them.
Instead of having to search through all the information on the main organizational account,
followers can get notifications only from the account with the specific location they desire.  

The disadvantage of setting up multiple accounts is the amount of maintenance required for each account.
Setting up multiple accounts also requires also setting up multiple emails to link to each account,
and this may have an ongoing cost if purchasing email services.

## Personal Accounts ##

A third option for setting up twitter accounts to communicate with followers is to create
individual personal accounts for people associated with the organization.
This requires setting up each person with a professional twitter account and emails to attach to each of those accounts.  

In this situation followers would need to follow the personal accounts of those associated with the organization,
or the organization would need to retweet posts from the personal accounts.  

There may be a way to automate this retweet process, but this will require more research,
and is not obvious how to accomplish using TwitterOAuth.

## Public Tweets ##

The most obvious and straightforward method of communicating with followers is by posting public tweets on an account,
whether that be on a general organizational account or specific accounts.  
The tweets will be displayed on the organization's twitter account page and any followers will receive the tweets.

Hashtags can be used to specify what type of tweet the post is,
or to label the tweet with related information, such as a specific location.

If there is a need to develop code to post tweets in an automated fashion,
there are many [libraries](https://developer.twitter.com/en/docs/developer-utilities/twitter-libraries)
available for different programming languages.  

Posting a tweet using [TwitterOAuth](https://github.com/abraham/twitteroauth):

```php
$twitteroauth->post('statuses/update', array('status' => 'status text here'));
```
See [Twitter Mobile Notifications](/twitter-mobile-notifications.md) for how followers can configure their cell phones to receive updates from your account/accounts.

## Direct Messaging ##

**Do direct messages control only who receives the messages (the sending side)?
Or does it require that something different occur on the receiving end?**

**Would you send direct messages from the same account as public messages?
Or would a separate account devoted to direct messages be needed for full control of sending and receiving?**

Another option for communicating with followers is by sending direct messages.
The messages will not be public and will only be seen by the indicated followers,
essentially providing a private communication channel. **Is this true?**
Direct messaging requires more set-up.
To send a direct message through any of the [twitter libraries](https://developer.twitter.com/en/docs/developer-utilities/twitter-libraries)
or through using the [Twitter API](/twitter-api.md) requires obtaining Twitter ID's of all of the users to contact
and using the information to configure the tool being used to send messages.  

See direct messaging using [TwitterOAuth](https://github.com/abraham/twitteroauth):
```php
$twitteroauth->post('direct_messages/new', array('text' => 'dm text here', 'screen_name' => 'recipients screen_name'));
```

See [Twitter Mobile Notifications](/twitter-mobile-notifications.md) for how followers
can configure their cell phones to receive direct messages with special handling such as unique ring tones.
