# Twitter / Account Set Up

This page summarizes guidelines for creating organization-related Twitter accounts.

* [Types of Accounts](#types-of-accounts)
* [Create Organizational Account](#create-organizational-account)
* [Create Personal Account within Organizational Account](#create-personal-account-within-organizational-account)
* [Create a Test Account](#create-a-test-account)
* [Managing Accounts Through Tweet Deck](#managing-accounts-through-tweet-deck)

------------

## Types of Accounts

Twitter can be used to send messages from different types of accounts, depending on need, for example:

1. Send from organizational account with general information (`@OWF Annual meeting is September 30 at location X`).
	 + This type of account can be easily configured and is described below.
2. Send from a personal account on behalf of an organization (`@OWF-Steve I'll be presenting at the XYZ conference`).
	 + This type of account can be easily configured and is described below.
3. Send from a personal account (`@someuser I love fishing`)
	 + This type of account can be easily configured as per normal Twitter conventions.
4. Send from an account associated with a place, such as a data collection station (`@Org-gage-100 flow is at dangerous level`)
	+ This case has been implemented by some but is not trivial,
	mainly due to the difficulties of obtaining unique email accounts.
	+ Twitter is working on this capability (?).  Or are they enhancing features to filter geographically?

The following sections focus on how to set up an organizational account and personal accounts within an organization.
It is also useful to set up a test account, for example to test automated messaging,
and this is explained below as supporting material.

## Create Organizational Account

An organizational account can be set up as described below.
It is also recommend that a [test account](#create-a-test-account) is created
to facilitate testing, such as automated notification software.
Once validated, processes that send messages from the test account can be switched to the organization account.

To create an organizational account:

1. Go to [https://twitter.com/signup](https://twitter.com/signup)
2. Enter the required information:
	* ***Full Name***: There is a 50 character limit. This will be the display name for the organization account.
	This should be relevant to your business name. Don't use numbers and avoid underscores.  
	For example: **`Open Water Foundation`**.
	* ***Phone or Email***: This will be the official email associated with the business account.
	* ***Password***: Enter a password.
3. Enter a valid phone number. Twitter requires an account be verified with a valid phone number
before allowing access to many developer features, such as gaining access to
[OAuth keys](http://localhost:8000/authentication/#access-tokens).
4. Create a username/twitter handle for the account.
As with the Full Name this should be relevant to the business name and similar to the display name that was chosen.
Again avoid numbers, and underscores. Use the upper case  naming convention.  
For example: **`@OpenWaterFoundation`**

## Create Personal Account within Organizational Account

* Does it even make sense to call it this?
* How is this done?  Is there a level within an organization or just use the organization email as if any account?

## Create a Test Account

Use the following instructions to create a test account.
When developing new tools it is a good idea to create a test account for testing purposes.
The test account can be used post updates to Twitter and ensure that nobody can see them (assuming that nobody follows the test account).

#### Create a Test Account:

Create a test account similar to creating a typical user account:

1. Go to [https://twitter.com/signup](https://twitter.com/signup)
2. Enter the required information:
	* ***Full Name***: This will be the display name for the test account.
	Since the test account is designed to never be viewed by the public, this can be anything.   
	For example: **Open Water Foundation Test**.
	* ***Phone or Email***: It is a good idea to create a fake email to be associated with the test account.
	It is suggested to make the email the same as the account name so that it is easier to remember.  
	For example, if planning on using the twitter handle **`@OWFTest`**, create an email such as **`owftest@gmail.com`**.
	This is only for convenience purposes, you can use any valid email for the test account.
	* ***Password***: Enter a password.
3. Enter a valid phone number. Twitter requires an account be verified with a valid phone
number before allowing access to many developer features,
such as gaining access to [OAuth keys](http://localhost:8000/authentication/#access-tokens).
4. Create a username/twitter handle for the account. As with the Full Name for the account.
Twitter users cannot see this because of settings described in the next section.
For Example: **`@OWFTest`**

#### Protect Your Updates:

A test account is set up with the intent of working through bugs,
and consequently it is common to avoid tweets going public (unless this needs to be tested).
By following the steps below, any tweets posted by the test account will only display to approved users.

To avoid people coming across test status updates:

1. Click on the user image or ***Profile and Setting***.
2. Select ***Settings and privacy*** from the drop-down.
3. Select ***Privacy and safety*** from the left hand navigation bar.
4. Check the box next to **Protect your Tweets**. This will prevent any future tweets from being available publicly.

## Managing Accounts Through Tweet Deck

[Tweet Deck](https://tweetdeck.twitter.com/) is a convenient online Twitter tool that offers the ability to connect separate twitter accounts without having to share any passwords among the separate users.

***Tweet Deck Teams***: allows multiple users to share a Twitter account without having to share the password.
There are three different Roles associated with Tweet Deck Teams:

1. **Owner**:
	* Can manage password, phone number, and login verification.
	* Can invite others to access the account as admins or contributors.
	* Can take action on behalf of the team account (Tweet, Retweet, Direct Message, like, etc.), schedule Tweets, create lists, and build collections.
2. **Admin**:
	* Can invite others to access the account as admins or contributors.
	* Can take action on behalf of the team account (Tweet, Retweet, Direct Message, like, etc.), schedule Tweets, create lists, and build collections.
3. **Contributer**:
	* Can take action on behalf of the team account (Tweet, Retweet, Direct Message, like, etc.), schedule Tweets, create lists, and build collections.

[https://help.twitter.com/en/using-twitter/tweetdeck-teams](https://help.twitter.com/en/using-twitter/tweetdeck-teams)
