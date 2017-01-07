---
layout: posts
title: 100DaysOfCode - Day 2
---
# What is the challenge today?
Enhance the interface of my Jekyll Blog

# How did I tackle this?
Decide on user stories to implement:
1. Viewers can follow and receive regular updates of my posts as they would like to
2. Posts can be automatedly tweeted as soon as they are published
3. Viewers can comment on my posts

# Was it solved?
User story #3 was resolved but not #1 & #2

# What did I learn?
RSS or Atom Feed are methods of tracking the contents of the blog with a summarised XML file. 
It is important for integration with automated publications on social media platforms like Twitter, FB, etc.

###How to integrate Disqus:
1. Login to disqus (or create a new account if needed)
2. Find the section that says:
'''Ready to install Disqus?
It only takes a few minutes and gets you access to all features. '''
Click on "Get Started"
If it's not in the landing page, try the steps below:
'''Click on the Avatar (the icon/pic in the top right corner) => Choose "Home" from the dropdown menu
Click on the gear icon in the top right corner (after landing in the Home page of Disqus) => Choose "Add Disqus to Site" 
The features page should show up so one can find the section above'''
3. Choose "I want to install Disqus on my site"
4. Enter the name of your website as prompted in this format:
'''example.com 
subdomain.example.com'''
Wrong format examples:
'''http://www.example.com 
example.com/my-blog-name'''
More on [troubleshooting here](https://help.disqus.com/customer/portal/articles/472007-i-m-receiving-the-message-%22we-were-unable-to-load-disqus-%22)
5. Upon comleting the creation of Disqus installation by accepting the policy & selecting Jekyll platform, 
find the "Universal Embed Code" in the installation instruction. Copy the entire code in section 1 only (2 and 3 are optional)
6. Go to the repo of the blog & add the Disqus username to `disqus` property in the `_config.yml` file
7. Go to `_includes\disqus.html` and add in the copied code (Universal Embed Cod) between`{% if site.disqus %}` and `{% endif %}`.
Delete any other thing in the middle of these 2 lines if available
8. Modify the md files of the posts expecting comments, or just modify the `_layouts\post.html` file if comments should be available for all posts as followed:
```
---
layout: #whateverwasthere-nochange
comments: true
#otherproperties
---
```


# What else should I try next (or next time)?
Finish up the Feed and automation

Delete the wrong shortname of my blog site on Disqus

# What did I help others with today?
None @gain

# How do I think/feel about that?
Sad
