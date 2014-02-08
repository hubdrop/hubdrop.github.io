---
published: false
---

# The future of HubDrop

This project is simply something I wanted to do.  No one paid for it. I built it in my spare time as a way to refine the knowledge I learned over the last few years about Symfony, Vagrant, and Chef.

I want to grow this tool, but it takes time (==money) and a server.

So I'm opening up a GitTip account and starting an IndieGoGo campaign to raise funding for development of hubdrop.io.

But before I do that, I wanted to formally introduce HubDrop to the Drupal aocmmunity.

## What is HubDrop?
HubDrop.io is currently a tool that mirrors Drupal projects on GitHub.  In the future it will do all sorts of magic things with your git repos.

It was also a learning experience for me, but hopefully for others.  hope to use HubDrop's code as a lesson in building web services.

In the future, I want put together a detailed case study and document the process of building the entire HubDrop service.

HubDrop is also a part of the Drupal community.  There is a lot of debate about the drupal.org tools, and the effort it takes to improve them.  There was a huge discussion of moving to github outright, years ago.  The idea for hubdrop was to act as a bridge, so we don't have to decide for everyone what tool they must use for development, and can maybe get the best of both worlds in the meantime.

## Principles
I've got some important ideas that I believe in.  This project is a tool for the community, and I've come up with these three principles to keep it that way.

1. HubDrop will always be 100% open source.
2. Mirroring of public open source code and site projects will always be free.
3. HubDrop will always strive to survive on community funding, plus revenue from mirroring private repos.

We'll see how it goes.  I am a cynic idealist.  If the funding comes in, there's so much that can be done.  

## Features
There are a number of features that I am sure everyone is thinking of.  Here is my priority list:

1. **GitHub to Drupal sync.**
  This will allow projects to move development to GitHub, while maintaining a mirror on drupal.org for releases, presence in the community, etc.

  This is already working for the "drupalprojects" organization, but I have to run a command on the server to do so.  This is a very tricky feature because you have to decide who gets commit access.

  I have this working as well, and I'll write more about it later, but the point is, the next step is letting developers create their own repos in any organization, and plug it into Drupal's git service.  This part will require some work because there is no database in hubdrop and I'd like to keep it that way. 

2. **Private 3rd Party Mirroring (and merging)**
  By which I mean, mirroring your Pantheon, Acquia, or other git host repo on your own GitHub account or organization, private or public.

  I already set this up as a test by messing with the pushUrl and it works, but its lumped in with the contrib projects.  Also this depends on feature #1 because we need some kind of authentication to set this up.  
  
  The merging part is mainly for Acquia Cloud.  We could let devs keep their drupal code in the root of their repo, and automatically sync it to your acquia cloud repo, which must keep drupal at`docroot`.

3. **Drupal Core Update Merging**
  What if you could give hubdrop access to your repo, and, whenever there was a core update, it could make a branch of your master and apply the update for your review?  Basically what Pantheon does but for *any* drupal repo.
3. **Drush Make and Distribution Repos**
  Using drupal/drush make-driven-drupal-development? Want to, but don't want to teach your devs to build the site all the time?  

  Got a distribution that drupal.org packages? 
  
  HubDrop could track changes to your makefile, and sync that with a full drupal site repo, making for more flexible development and distribution.

