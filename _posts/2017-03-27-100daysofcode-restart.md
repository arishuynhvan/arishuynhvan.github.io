---
layout: post
title: Restart 100 Days of Code
---

## Motivation

So it's quite obvious that I gave up on the previous iteration of 100 days of code (which started in Jan 2017).
Yet, I don't want to give up this training, so I'll try again

## Structured programs to follow

30 days, 30 sites - [techwithtris](http://www.techwithtris.com/)

[30 days Vanilla JS coding challenge](https://javascript30.com/) - wesbos

[freecodecamp](https://www.freecodecamp.com)

[Daily UI Design Challenge](http://www.dailyui.co/)


## Side projects

Charchawale for [makerwala.in](http://makerwala.in/)


## Day 1

### What I've achieved

<iframe height='300' scrolling='no' title='Freelance Portfolio' src='//codepen.io/arishuynhvan/embed/RpBXBz/?height=265&theme-id=0&default-tab=html,result&embed-version=2' frameborder='no' allowtransparency='true' allowfullscreen='true' style='width: 100%;'>See the Pen <a href='http://codepen.io/arishuynhvan/pen/RpBXBz/'>Freelance Portfolio</a> by Aris Huynh (<a href='http://codepen.io/arishuynhvan'>@arishuynhvan</a>) on <a href='http://codepen.io'>CodePen</a>.
</iframe>


- I revamped my about page in codepen by following the [bootstrap tutorial on w3schools for company website](https://www.w3schools.com/bootstrap/bootstrap_theme_company.asp)
- I also set up my own free domain with .tech using my student (.edu) email. It's free for a year, so it's good enough for me to use now


### What's next?

- Fix errors of the about page
- Update my website titles for this repo (new title: T.An Elegant Tech)
- Make about page the landing site of the domain link instead of the blog
- Major revamp for the structure of this site
- Post my portfolio on FB (in the far future when my other sites of portfolio are more ready)
- Make this site progressive so I can view it on my phone
- Find a more user-friendly way to edit the site

#### Actionables on About Page errors

- Change the units of fonts on about page back to em or px according to w3schools tutorial since vw is very horrible for full page view
- Update the form & buttons in my about page for collecting real email addresses & send clients' emails to me
- Stop the "contact" on navbar from being always in the hover state 

### Learning points

- "vw" (viewport width) units for scaling with page width
- Adding Google map to my site
- Splitting rows for responsive display of big & smal screen sizes
- How to set up free email with my free domain & direct it to my gmail account
- How to link my domain to Github pages
- How to get a [free .edu email](https://www.quora.com/How-can-I-get-an-edu-email-without-being-in-school)

#### More on how to link my free .tech domain with Github pages

Adapted from [Namecheap article](https://www.namecheap.com/support/knowledgebase/article.aspx/9645/2208/how-do-i-link-my-domain-to-github-pages)

1. Go to settings 

![github-repo-setting](../images/posts/github-repo-setting.PNG)

2. Scroll down to GitHub Pages section
3. Type in custom domain in the Custom domain textbox and hit Save (remember the "www")

![github-custom-domain](../images/posts/github-custom-domain.png)

After this step, usually Gihub will automatically add/modify CNAME file to the root of Github repo. Check if this CNAME exists. Then, check if the first line is the custom domain.

4. Sign into the control panel of the custom domain with username & password
5. Find the setting for managing DNS (it can be "Manage DNS" or "Advanced DNS")
6. Add a CName record with "www" as the host and your "username.github.io" (where this username is github username) as the value. Save this record.
7. Now launch the site at the custom domain to test if GitHub page has been properly linked with the custom domain
