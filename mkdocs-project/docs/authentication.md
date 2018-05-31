# Twitter Authentication #
Twitter uses [OAuth 2.0](https://oauth.net/) to provided authorized access to its API. This authentication will need to take place at some level if developing using [Twitter's API](/twitter-api) or if using any of the libraries that build off their API.

## Using OAuth ##
To Use OAuth with Twitter API an application must:

1. [Obtain access Tokens](#access-tokens) to act on behalf of a user account
2. [Authorize all HTTP requests](#authorize-http-request) it sends to Twitter's API.

#### Access Tokens:
There are 4 keys needed to use OAuth for Twitter's API: Consumer Key, Consumer Secret, Access Token, and Access Token Secret.

To obtain these keys:

1. Go to [https://apps.twitter.com/app/new](https://apps.twitter.com/app/new). Log in if necessary.
2.  Enter desired Application Name, Description and your website address making sure to enter the full address including the http://. It is acceptable to leave the callback URL empty.
3.  Accept the TOS and submit the form by clicking the **Create your Twitter Application**.
4.  After creating your Twitter Application click on the tab that says **Keys and Access Tokens**. Click the Create my Access Token button.
6.  Lastly copy the Consumer key (API key), Consumer Secret, Access Token and Access Token Secret.

These keys will need to be passed to whatever library or code written to access Twitter's API.

For example, when using [twitterOAuth](https://github.com/abraham/twitteroauth):
```php
$consumerKey    = 'XXX';
$consumerSecret = 'XXX';
$oAuthToken     = 'XXX';
$oAuthSecret    = 'XXX';

// create a new instance
$tweet = new TwitterOAuth($consumerKey, $consumerSecret, $oAuthToken, $oAuthSecret);
```

#### Authorize HTTP Request:
To allow applications to provide this information, Twitter's API relies on the OAuth 2.0 protocol. At a very simplified level, Twitter's implementation requires that requests needing authorization contain an additional HTTP Authorization header with enough information to answer the questions listed above. A version of the HTTP request shown above, modified to include this header, looks like this (normally the Authorization header would need to be on one line, but has been wrapped for legibility here):

```
POST /1.1/statuses/update.json?include_entities=true HTTP/1.1
Accept: */*
Connection: close
User-Agent: OAuth gem v0.4.4
Content-Type: application/x-www-form-urlencoded
Authorization:
OAuth oauth_consumer_key="xvz1evFS4wEEPTGEFPHBog",
oauth_nonce="kYjzVBB8Y0ZFabxSWbWovY3uYSQ2pTgmZeNu2VS4cg",
oauth_signature="tnnArxj06cWHq44gCs1OSKk%2FjLY%3D",
oauth_signature_method="HMAC-SHA1",
oauth_timestamp="1318622958",
oauth_token="370773112-GmHxMAgYyLbNEtIKZeRNFsMKPR9EyMZeS9weJAEb",
oauth_version="1.0"
Content-Length: 76
Host: api.twitter.com

status=Hello%20Ladies%20%2b%20Gentlemen%2c%20a%20signed%20OAuth%20request%21
```

Many twitter libraries will handle this step on their own and allow the development to be simple and straight forward.  
For example, when using [twitterOAuth](https://github.com/abraham/twitteroauth):  
```php
$twitteroauth->post('statuses/update', array('status' => 'status text here'));
```
