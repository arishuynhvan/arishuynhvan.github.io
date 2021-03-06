---
layout: post
title: 100 Days Of Code Day 2
---

## Today's focus

Select a well-supported nodejs CMS framework for Charchawale

Below are frameworks I tried out & the status of my attempts/ personal cons: 


- [PencilBlue](https://github.com/pencilblue/pencilblue) - mongodb, easy to set up, very elementary theme, has inbuilt comments & (unchecked) OAuth Google plugin
- [KeystoneJS](https://github.com/keystonejs/keystone) - mongodb, less easy to set up, very elementary theme, lack OAuth Google Plugin, but repo has 9k+ stars (big community)
- [Apostrophe](https://github.com/punkave/apostrophe) - beautiful, but I haven't set up locally, lack OAuth with Google
- [Cody](https://github.com/jcoppieters/cody) - use mysql, may or may not work since I ran the wrong server: jenkins (3000) instead. This was setup in my charchawale-keystone workspace on c9.io (yeah, the name :/) 

Also, I attempted to use a few PHP frameworks:

- [Open Source Social Network](https://www.opensource-socialnetwork.org/) - php steep learning curve, unable to install locally
- [Wordpress.org](https://wordpress.org/) - plugins are not working, PHP steep learning curve
- [Phundament](https://github.com/phundament/app) - can't set up without docker. docker is totally not for windows :(

## Learning points

- Free domains for student:
 - [Namecheap](https://www.namecheap.com/) - Only for certain US, Canada, Australia universities; free .me domains
 - [get.tech](http://get.tech/students/) - Free for all emails with ".edu"
 
Most of these free domains are only free for the 1st year, while the yearly fee is quite high. :( 

### Set up MongoDB for windows:

Follow the [official guide](https://docs.mongodb.com/manual/tutorial/install-mongodb-on-windows/), then create a data folder in the folder of the new CMS application (preferably at root where the main js file for starting the application stays)

Start the MongoDB server locally after installation `"C:\Program Files\MongoDB\Server\3.4\bin\mongod.exe" --dbpath data`

### Common errors

#### MongoError

Sample error message:

```
Mongoose connection "error" event fired with:
{ [MongoError: failed to connect to server [localhost:27017] on first connect]
  name: 'MongoError',
  message: 'failed to connect to server [localhost:27017] on first connect' }
```

Start the MongoDB server locally 

```
"C:\Program Files\MongoDB\Server\3.4\bin\mongod.exe" --dbpath data
```


#### Taken server port

Sample error message:

```
Uncaught Exception detected : Error: listen EACCES 0.0.0.0:8080
```
Check among the js files in the root folder (normally config.js or server.js), change the default port to another value (e.g. 3000, 3223, etc.) and relaunch the site locally

### What's next

1. Try installing Google OAuth [plugin](https://pencilblue.org/plugins/view/5616b3f82f320df86ff3a13f) for pencilblue
2. Implement onsite registration for both Keystone & PencilBlue (esp if Google OAuth works)
3. Learn how to make a new theme for the CMS framework of choice
4. Learn how to make a new plugin (QR login) for the CMS framework of choice
5. Figure out how to stop my jenkins server from running? Probably by restarting my laptop after a super long duration
6. Check which one allows easy video upload, preferably from URL of videos in Google drive 
7. **Deploy with Firebase, Google App, or Heroku**
