# Twitter API

Twitter offers a range of different APIs for developers. The following is a brief overview of these different APIs.
API usage is [rate limited](https://developer.twitter.com/en/docs/basics/rate-limiting.html),
with additional account-based [fair use limits](https://help.twitter.com/en/rules-and-policies/twitter-limits)
on write/create/delete endpoints, to protect Twitter from abuse.

[Twitter API reference index](https://developer.twitter.com/en/docs/api-reference-index)

* [API Libraries](#api-libraries)
* [Different APIs Offered](#different-apis-offered)

-----------

## API Libraries

Twitter highly encourages the use of various libraries to access twitter's API functionality. To see a list of the different libraries see
[Twitter API Libraries](https://developer.twitter.com/en/docs/developer-utilities/twitter-libraries.html). Below are a couple libraries OWF is familiar with.

* **TwitterOAuth**: The most popular PHP library for Twitter's OAuth REST API.
See documentation at [https://twitteroauth.com](https://twitteroauth.com/).

* **Twurl**: [Twurl](https://github.com/twitter/twurl) is like curl, but tailored specifically for the Twitter API.
It knows how to grant an access token to a client application for
a specified user and then sign all requests with that access token.
It also provides other development and debugging conveniences such
as defining aliases for common requests, as well as support for
multiple access tokens to easily switch between different client
applications and Twitter accounts.

## Different APIs Offered

There are three kinds of Twitter APIs:

1. [Free and Public APIs](#free-and-public-apis): These are best to work with, if there is no need for complicated requests.
2. [Twitter Premium APIs](#twitter-premium-apis): Might be used if sending more complex requests and trying to build a big platform on Twitter.  
3. [Enterprise APIs](#enterprise-apis-gnip): Used for large corporations.

### Free and Public APIs:

* Provide basic query functionality and foundational access to twitter data.  
* Consist of a REST (Representational State Transfer) API and a Streaming API.  
* Twitter APIs use the JSON data format for responses (and in some cases, for requests).
* Methods to retrieve data from the Twitter API require a **GET** request. Methods that submit, change, or destroy data require a **POST**. A **DELETE** request is also accepted for methods that destroy data.

#### REST API:

Using the [secure tokens obtained via OAuth](http://localhost:8000/authentication/#access-tokens), your application makes requests to Twitter for specific data, e.g. the user's home timeline or their own statuses, or a request to post a tweet for a specific user.

![REST API](https://cms-assets.tutsplus.com/uploads/users/317/posts/22192/image/streaming-intro-1_1.png)

Twitter includes APIs that "can be used to programmatically create, retrieve and delete Tweets, Retweets and Likes." [Post, retrieve and engage with Tweets](https://developer.twitter.com/en/docs/tweets/post-and-engage/overview)

Twitter REST API allows capability to update statuses on a users Twitter page through their POST request.
[API Reference](https://developer.twitter.com/en/docs/tweets/post-and-engage/api-reference/post-statuses-update)

#### Streaming API

The Twitter Streaming API allows you to receive tweets and notifications in real time from Twitter. However, it requires a high-performance, persistent, always-on connection between your server and Twitter.

### Twitter Premium APIs:

New products that scale access and price to fit needs. Built to enable innovation:  

 * more tweets per request
 * higher rate limits
 * a counts endpoint that returns time-series counts of Tweets
 * more complex queries
 * meta-data enrichments such as expanded URLs and improved profile geo information.

### Enterprise APIs (Gnip):

Real-time and historical data to power businesses at scale.
