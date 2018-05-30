# OAuth
Twitter uses OAuth to provide authorized access to its API.

1. **User Authentication**: A signed request identifies an application's identity in addition to the identity accompanying granted permissions of the end-user the application is making API calls on behalf of, represented by the user's access token.
2. **Application-only authentication**: A form of authentication where an application makes API requests on its own behalf, without a user context. API calls are still rate limited per API method, but the pool each method draws from belongs to the entire application at large, rather than from a per-user limit. API methods that support this form of authentication will contain two rate limits in their documentation, one that is per user (for application-user authentication) and the other is per app (for this form of application-only authentication). Not all API methods support application-only authentication, because some methods require a user context (for example, a Tweet can only be created by a logged-in user, so user context is required for that operation).

## Using OAuth
To Use OAuth with Twitter API an application must:

1. [Obtain access Tokens](#access-tokens) to act on behalf of a user account
2. [Authorize all HTTP requests](#authorize-http-request) it sends to Twitter's API. 

#### Access Tokens:
There are 4 keys needed to use OAuth for Twitter's API: Consumer Key, Consumer Secret, Access Token, and Access Token Secret.

To obtain these keys:

1. Go to [https://apps.twitter.com/app/new](https://apps.twitter.com/app/new). Log in if necessary.
2.  Enter your desired Application Name, Description and your website address making sure to enter the full address including the http://. You can leave the callback URL empty.
3.  Accept the TOS and submit the form by clicking the **Create your Twitter Application**.
4.  After creating your Twitter Application click on the tab that says **Keys and Access Tokens**, then you have to give access to your Twitter Account to use this Application. To do this, click the Create my Access Token button.
5.  Lastly copy the Consumer key (API key), Consumer Secret, Access Token and Access Token Secret from the screen into our plugin's Twitter Options page and test.

#### Authorize HTTP Request:
To allow applications to provide this information, Twitter's API relies on the OAuth 1.0a protocol. At a very simplified level, Twitter's implementation requires that requests needing authorization contain an additional HTTP Authorization header with enough information to answer the questions listed above. A version of the HTTP request shown above, modified to include this header, looks like this (normally the Authorization header would need to be on one line, but has been wrapped for legibility here):

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
