# Pre-Authenticated Users In Ada

> This article will outline how to implement Ada’s Authentication functionality for your customers who are already logged in to your services on either a webpage, desktop application, or mobile application. Once enabled, a user who is already logged in to their account on your website, mobile app, or desktop app, will not be asked by the bot to log in again mid-conversation.

The core difference between this article and the original Authentication article is that this version does not leverage the Sign In blocks. Instead, this method of authentication relies on some simple Auth Token and/or Session ID generation. 

## Table of Contents

There are two different methods for achieving this. 

1. [Method 1 - Unique User Authentication Token Generation] (#method-1)

Generating unique user authentication tokens, is recommended if you have this capability. If this functionality is not available for you, then we have provided an alternate option.

2. [Method 2 - Setting a Session ID with Expiration Timer] (#method-2)

Setting session IDs with an expiration timer. Instructions for establishing both of these methods are available below.

## Method 1
### Passing a Unique User Authentication Token

*This method assumes that your backend uses tokens to authenticate users.
Furthermore, the instructions below are written for pre-authentication on the web. The process may look slightly different for mobile or desktop applications, however, the concepts and outcomes remain the same.

In this section, we explain how to create a unique authentication token for each user, and pass this token to us. As you proceed through the steps below you will be working to create a purple metavariable, similar to the one seen here:*

<img width="80" alt="User Auth Token" src="userauthtoken.png">

