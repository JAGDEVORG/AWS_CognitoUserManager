# Cognito User Manager

<b>Cognito is a User Identity Management service provided by AWS in its Cloud suite. Cognito provides user identity and authorization management for applications, while applications can use the solutions in granting access to their functionalities.</b>

Introduction
AWS Cognito provides OAuth2 auth flows such as Authorization Code where the application can redirect to AWS Cognito hosted login screens where the user credentials are validated against Cognito data store and is redirected to the configured landing pages on the application side with an idToken which represents user authorization.

While it is the most recommended approach for applications, some designs prefer having a layer of their API that would communicate with Cognito for authorization, as a matter of decoupling Cognito with the Client (so as to have flexibility or better control).

In this article, let’s look at how we can design and build such an API that encapsulates all of User Identity Management functionalities such as Login, Signup, Password Reset, Update profile and so on, while internally communicating with Cognito for respective flows.

Keep in mind that to run such an API, we need the API to be deployed in a resource that has all the IAM permissions for Cognito access.

1. Setup the UserPool 
2. When setup the client then do not generate the "App client secret"
3. AccessKeyId & AccessSecretKey is the IAM users credentials.

What we can do with this project
1. Signup the user
2. Get the token 
3. Forgot password 
4. Login the user
