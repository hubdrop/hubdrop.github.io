---
layout: post
title:  "GitHub Teams Limitations and questions"
date:   2014-01-06 18:34:00
---

hubdrop is now able to grant push access on github to the maintainers of a module.

it does this by logging into Drupal.org, loading the project's maintainers page, then looking for a link to your github profile on your Drupal.org profile page. 

it has to create a github "team" because "drupalprojects" is an organization. I was also able to create a team with "administrative" privileges, and added the users who can "edit" the project node, but, unfortunately, that does not grant you the ability to add other maintainers (in github).

this makes me think that we might have to let module maintainers mirror from their own github organization. Many project maintainers would want that.

if that were implemented, then perhaps every repo at github.com/drupalprojects could just be an "official mirror". we could even try to convince the owner of the github.com/Drupal organization to become hubdrop's target.

I am at the point where I need feedback. let's discuss this.