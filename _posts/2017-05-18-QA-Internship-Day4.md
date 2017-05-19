---
layout: post
title: QA Internship Day 4 - Test Users Graph API
---

## Objectives

Today, I'll need to further come out with test scripts for automating the ShopBack's login process with FB accounts

## Plan

1. First, create test users with graph API (not manually)
2. Check if I can login with my app via this test user!!!!!!!! (*)
3. Write the script if 2 is verified
   a. Automate test user creation while storing essential info (app id, secret, access token, login URL, User ID, email & password) in the scripts.
   b. Automate test user login on ShopBack. 
   c. Check if user is added in ShopBack's database
   d. Automate test user deletion with Graph API, to avoid reaching the 2000 test user limit.

(*) To achieve this, I may need to build a simple form with FB authorization, using MongoDB for storing users, and deploy on heroku site. Then I'll need to write an automatic test script for this simple site, and substitute my app info like ID, access token, app secret with those of ShopBack. Since a FB app-ID is required for FB login through [FB SDK for JS] (https://developers.facebook.com/docs/javascript/quickstart), I should be able to get these info.

Question for 3a: How can I allow test user to see other apps? If it's possible, I can just directly make my test users visible to ShopBack without getting the FB account for ShopBack... But I still may need FB appID for ShopBack

### [Graph API](https://developers.facebook.com/docs/graph-api)

This is the official API from Facebook that allows third-party apps to read and write to the Facebook social graph. 

#### Jargons

- [Test users](https://developers.facebook.com/docs/apps/test-users): special Facebook accounts, invisible to real accounts, which can be created within an app for the purpose of manual or automated testing of that app's Facebook integration. Test user accounts cannot find real FB accounts either. Test users can be created automatically with the Graph API or manually via App Dashboard

- [Graph API edge](https://developers.facebook.com/docs/graph-api/reference/v2.9/app/accounts/test-users) is used for managing the entire test user pool, so mainly it functions at account level - test user creation, disassiciatin/associating test users with apps

- [Graph API node](https://developers.facebook.com/docs/graph-api/reference/v2.9/test-user) is used for managing activities for each specific test users like posting, liking, commenting and deleting the account.

#### Automate test user creation with Graph API

1. Login to [FB for developers](https://developers.facebook.com/) page with a real FB account.
2. Go to MyApps, choose the target app or create a new one.
3. Get AppID and App Secret ready.
4. **Go to [Graph API Explorer](https://developers.facebook.com/tools/explorer/), change the application dropdown to the target app**. 90% of the time this step is missed, so please remember to choose the correct app before proceeding to the next step.
5. Get your access token ready as well.
6. Use the following POST request in your automation script to create a new test user

```
https://graph.facebook.com/{app-id}/accounts/test-users?installed=true&name={any-valid-name}locale=en_US&permissions=email,user_birthday,publish_actions&access_token={app-access-token}
```

To just play around on Graph API Explorer, set the request type to POST for any version, then paste the string below in, sustituting in the correct values as well.

```
{app-id}/accounts/test-users?installed=true&name={any-valid-name}&locale=en_us&permissions=email,user_birthday,publish_actions&access_token={app-access-token}
```

All the {} brackets shouldn't be there when the string above is replaced with real values.

Feel free to adjust the POST request according to the syntax of your framework.

**References:**

[The 1st answer to this Stack Overflow question](http://stackoverflow.com/questions/24046772/how-to-add-test-friends-to-facebook-test-users-programmatically-using-facebook-i#)

[More about the Graph API request fields](https://developers.facebook.com/docs/graph-api/reference/app/accounts/test-users#publish)

[More about Graph API permission list](https://developers.facebook.com/docs/facebook-login/permissions/)


#### Automate test user deletion with Graph API
 
Use [DELETE request](https://developers.facebook.com/docs/graph-api/reference/v2.9/test-user#deleting) with test-user-id to delete the user.

#### Automate association of test user with another app

Could this be done without app-id of that other app?
