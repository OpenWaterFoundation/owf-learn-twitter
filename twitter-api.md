# Twitter's API
Twitter offers a range of different APIs for developers. The following is a brief overview of these different APIs.  
[Twitter API reference index](https://developer.twitter.com/en/docs/api-reference-index)

API usage is [rate limited](https://developer.twitter.com/en/docs/basics/rate-limiting.html), with additional account-based [fair use limits](https://help.twitter.com/en/rules-and-policies/twitter-limits) on write/create/delete endpoints, to protect Twitter from abuse.

#### Table of Contents:
* [Different APIs Offered](#markdown-header-different-apis-offered)
* [API Libraries](#markdown-header-api-libraries)
* [Applications of Twitter's API](#markdown-header-applications-of-twitters-api)

## Different APIs Offered
There are three kinds of Twitter APIs:

1. [Free and Public APIs](#markdown-header-1-free-and-public-apis)  
    * [REST API](#markdown-header-rest-api)  
    * [Streaming API](#markdown-header-streaming-api)   
2. [Twitter Premium APIs](#markdown-header-2-twitter-premium-apis)  
3. [Enterprise APIs](#markdown-header-3-enterprise-apis-gnip) 

### 1. Free and Public APIs:
* Provide basic query functionality and foundational access to twitter data.  
* Consist of a REST(Representational State Transfer) API and a Streaming API.  
* Twitter APIs use the JSON data format for responses (and in some cases, for requests).
* Methods to retrieve data from the Twitter API require a **GET** request. Methods that submit, change, or destroy data require a **POST**. A **DELETE** request is also accepted for methods that destroy data.

##### REST API:
Using the secure tokens obtained via OAuth, your application makes requests to Twitter for specific data, e.g. the user's home timeline or their own statuses, or a request to post a tweet for a specific user.

![REST API](https://cms-assets.tutsplus.com/uploads/users/317/posts/22192/image/streaming-intro-1_1.png)

Twitter includes APIs that "can be used to programmatically create, retrieve and delete Tweets, Retweets and Likes"  
[Post, retrieve and engage with Tweets](https://developer.twitter.com/en/docs/tweets/post-and-engage/overview)

##### Streaming API
The Twitter Streaming API allows you to receive tweets and notifications in real time from Twitter. However, it requires a high-performance, persistent, always-on connection between your server and Twitter. 

### 2. Twitter Premium APIs:
New products that scale access and price to fit needs. Built to enable innovation:  

 * more tweets per request
 * higher rate limits
 * a counts endpoint that returns time-series counts of Tweets
 * more complex queries
 * meta-data enrichments such as expanded URLs and improved profile geo information.

### 3. Enterprise APIs (Gnip):
Real-time and historical data to power businesses at scale.


## API Libraries
Twitter highly encourages the use of various libraries to access twitter's API functionality.

To see a list of the different libraries see
[Twitter API Libraries](https://developer.twitter.com/en/docs/developer-utilities/twitter-libraries.html).

#### TwitterOAuth:
> The most popular PHP library for Twitter's OAuth REST API. 
> 
> See documentation at [https://twitteroauth.com](https://twitteroauth.com/).

#### Twurl:
> [Twurl](https://github.com/twitter/twurl) is like curl, but tailored specifically for the Twitter API.
It knows how to grant an access token to a client application for
a specified user and then sign all requests with that access token.

> It also provides other development and debugging conveniences such
as defining aliases for common requests, as well as support for
multiple access tokens to easily switch between different client
applications and Twitter accounts.

## Applications of Twitter's API
**//TODO**: This section could use a little work

#### Update Statuses with Twitter API:
Twitter REST API allows capability to update statuses on a users Twitter page through their POST request. 

[API Reference](https://developer.twitter.com/en/docs/tweets/post-and-engage/api-reference/post-statuses-update)

#### Direct Messaging with Twitter API:
Twitter allows users to receive mobile notifications to your phone for a number of different reasons. To edit your mobile notifications on Twitter Desktop go to `Settings and Privacy` > `Mobile` and then you can select various text notifications you wish to receive. 

For the sake of receiving important alerts from an organizational account the two options you might want to turn on are `Tweets from people you've enabled for mobile notifications` and `Direct Messages`.

After selecting "Tweets from people you've enabled for mobile notifications" navigate to the organizations page you wish to receive updates from. Once there select the three dots in next to 'Following' and select `Turn on mobile notifications`.

Now you will receive text notifications of any direct messages or updates from the organization or user profile you turned on mobile notifications from. 
