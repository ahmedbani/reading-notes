# read 12
# OAuth

## What is OAuth?

>**Is an open-standard authorization protocol or framework that provides applications the ability for “secure designated access.”**

## Give an example of what using OAuth would look like.

>`Facebook apps are a good OAuth use case example. Say you’re using an app on Facebook, and it asks you to share your profile and pictures. Facebook is, in this case, the service provider: it has your login data and your pictures. The app is the consumer, and as the user, you want to use the app to do something with your pictures. You specifically gave this app access to your pictures, which OAuth is managing in the background.`

## How does OAuth work? What are the steps that it takes to authenticate the user?

* Step 1 – The User Shows Intent
* Step 2 – The Consumer Gets Permission
* Step 3 – The User Is Redirected to the Service Provider
* Step 4 – The User Gives Permission
* Step 5 – The Consumer Obtains an Access Token
* Step 6 – The Consumer Accesses the Protected Resourc

## What is OpenID?

>OpenID allows you to use an existing account to sign in to multiple websites, without needing to create new passwords (Like faceb[k you can open account in many phone or browsers).

# Authorization and Authentication flows

## What is the difference between authorization and authentication?

>Authentication and authorization might sound similar, but they are distinct security processes in the world of identity and access management (IAM). Authentication confirms that users are who they say they are. Authorization gives those users permission to access a resource.

## What is Authorization Code Flow?

>Authorization code flow is used to obtain an access token to authorize API requests. Authorization code flow is the most flexible of the three supported authorization flows and is the recommended method of obtaining an access token for the API.


## What is Authorization Code Flow with Proof Key for Code Exchange (PKCE)?

>The Authorization Code Flow + PKCE is an OpenId Connect flow specifically designed to authenticate native or mobile application users. This flow is considered best practice when using Single Page Apps (SPA) or Mobile Apps. PKCE, pronounced “pixy” is an acronym for Proof Key for Code Exchange.

## What is Implicit Flow with Form Post?

> Implicit Flow with Form Post flow uses OIDC to implement web sign-in that is very similar to the way SAML and WS-Federation operates. The web app requests and obtains tokens through the front channel, without the need for secrets or extra backend calls.

## What is Client Credentials Flow?

>The OAuth 2.0 client credentials grant flow permits a web service (confidential client) to use its own credentials, instead of impersonating a user, to authenticate when calling another web service.

## What is Device Authorization Flow?

>The OAuth 2.0 Device Authorization Grant (formerly known as the Device Flow) is an OAuth 2.0 extension that enables devices with no browser or limited input capability to obtain an access token. This is commonly seen on Apple TV apps, or devices like hardware encoders that can stream video to a YouTube channel.

## What is Resource Owner Password Flow?

>The Resource Owner Password Credentials flow allows exchanging the username and password of a user for an access token and, optionally, a refresh token. This flow has significantly different security properties than the other OAuth flows. The primary difference is that the user’s password is accessible to the application. This requires strong trust of the application by the user.

## Things I want to know more about

