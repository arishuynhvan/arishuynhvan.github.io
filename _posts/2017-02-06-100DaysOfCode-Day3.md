---
layout: post
title: 100DaysOfCode Day 3 - Restart
---

## Restart 100 Days of Code
What a shame that I have stopped my quest in coding for a month!
Nevertheless, I will restart my coding journey again today. Probably define proper goals & projects will help boost my motivation.

Also, I will adopt the scrum project management & arrange my goals into sprints.
Each project will have a separate backlog on its github repository.
Every day, the standup time will be 15 minutes for writing the log & posts for learning content


## Goals

### Personal Brand
It's essential to establish a personal brand. I have a lot of ideas floating around in my mind, but currently find it hard to
incorporate them into a unified theme for my site design

Things I really want to have in my brand:

- Personal blog featuring my learning journey, with subscription option
- Personal newsletter
- Design projects
- Mobile-first, responsive, accesible web-app
- Mobile cross-platform native apps

Thus, I've come up with a few project lists:

#### Portforlio
Blog about:

- Algorithm solutions
- Front-end learning journey
- Android app development trainings
- User experience & graphical design practices
- Data science self-study
- Neuroscience topics
- Language learning journey (English, French, German, Chinese, Italian, Spanish, Korean)
- Software engineering practices & experience
- Startup ideas
- Entrepreneurship journey (focus: social enterprise)
- Volunteer experience
- [Outreachy](https://wiki.gnome.org/Outreachy) & [GSoC](https://developers.google.com/open-source/gsoc/timeline) Application 
- Open-source Project Contribution from a newbie's perspective

Showcase:
    
- Project thumbnails
- Tutorials

#### Design Projects
- Personal Logo
- Personal Portfolio Blog
- Web-based projects with Free Code Camp
    - [Pomodoro Clock](https://www.freecodecamp.com/challenges/build-a-pomodoro-clock)
    - [JavaScript Calculator](https://www.freecodecamp.com/challenges/build-a-javascript-calculator)
    - [Tic Tac Toe Game](https://www.freecodecamp.com/challenges/build-a-tic-tac-toe-game)
    - [Simon Game](https://www.freecodecamp.com/challenges/build-a-simon-game)

#### Front-end Web Development
Web-based projects with Free Code Camp
    - [Random Quote Machine](https://www.freecodecamp.com/challenges/build-a-random-quote-machine)
    - [Local Weather](https://www.freecodecamp.com/challenges/show-the-local-weather)
    - [Wikipedia Viewer](https://www.freecodecamp.com/challenges/build-a-wikipedia-viewer)
    - [Twitchtv](https://www.freecodecamp.com/challenges/use-the-twitchtv-json-api)
    
    
#### Android App
- Todo-list for Codepath course application
- MakerWale:
    - An Android App that can track who uses which app
    - CharchaWale - minimalistic sharing & discussion Android App for non-English speaking students in rural India (esp makerWale)

### Open-Source Projects of Interest
- Fluid
- INCF
- Mifos
- OpenCV
- NRNB
- OpenMRS
- NUS TEAMMATES
- Wikimedia
- Syslog-ng

After all this planning, here's an update on today's coding progress:

## Day 3
So I took some time to venture in more dangerous zones of git. 

### Git
Firstly, I restarted my blog workspace in c9.io and realized I have changed my entire repo without upating it.
This error: `fatal: refusing to merge unrelated histories` showed up.Thus, I started with `git pull ----allow-unrelated-histories` [Source: StackOverflow](http://stackoverflow.com/questions/37937984/git-refusing-to-merge-unrelated-histories)

Secondly, I created a new branch for redesigning my landing page. I happened to commit the changes into this branch without updating it with master first.
So, I followed the instructions [here](http://stackoverflow.com/questions/7929369/how-to-rebase-local-branch-with-remote-master) and run `git rebase master` to update my branch with all the latest changes in master branch. It is definitely much cleaner
than merging master into branch, since it was fully compatible and didn't cause any merging conflicts.

Then, I tried to merge my branch into the master, but later had a second thought about it. Thus, I attempted `git reset --hard <commit>` to revert my merge,
but soon I realized it was useless since I have already pushed my merge to the remote repo. I also tried `git revert -m 1 <commit>`, but I failed to locate which is the right merging commit.
In the end, I just softly reverted my commits back to where I wanted with `git revert HEAD~2` (back 2 commits) and repush it as normal to my remote repo. I know that my history must be quite messy with this decision, 
but it will give me a good opportunity to practice rebase next.

### C9.io
As my blog has its template from the [Jekyll Now Project](http://www.jekyllnow.com/), the only way I can deploy it locally is by running `jekyll serve`.

However, the default ports are not servers for c9.io. Thus, I had to add the snippet below into `_config.yml` file.
```
# deployment
host: 0.0.0.0
port: 8080
```
The reason why I use C9.io workspace for my blog is because this jekyll project is still ruby-based although I wouldn't need much ruby to set it up. 
Honestly speaking, setting up a ruby project on Windows is a huge pain, so c9.io or any other cloud-based IDE is perfect.