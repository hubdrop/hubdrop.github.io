---
layout: post
title: "Manual \"Move to GitHub\" now possible."
date: {}
published: true
---

hubdrop is now able to switch "source" from drupal.org to github.  It is also now able to lookup a module's maintainers, and grant those users push access to the github.com/drupalprojects repo.  

It does this by logging into Drupal.org, loading the project's maintainers page, then looking for a link to your github profile on your Drupal.org profile page.  

That means we have to ask module developers to do a few things:

1. Add "hubdrop" as a maintainer, with both "Write to VCS" and "Administer Maintainers" permission.
2. On your Drupal.org profile, add a link to your GitHub user profile.
3. Tell the other module developers to do the same.
4. Then, and only then, click "Move to GitHub" on your project's hubdrop.io page.

We don't have the "Move to GitHub" button yet, but I can easily do it manually on the server.

## Teams
HubDrop has to create github "teams" in order to grant push access to users. This is because "drupalprojects" is a github organization.

Each team can be assigned one of three possible permissions: Pull, Push & Pull, and" Push, Pull & Administrativ"e.

I first created a team called "ProjectName Committers", and then "ProjectName Admins"
I was able to create a team with "administrative" privileges, and added the users who can "edit" the project node, but, unfortunately, that does not grant you the ability to add other people to the ).

this makes me think that we might have to let module maintainers mirror from their own github organization. Many project maintainers would want that.

if that were implemented, then perhaps every repo at github.com/drupalprojects could just be an "official mirror". we could even try to convince the owner of the github.com/Drupal organization to become hubdrop's target.

I am at the point where I need feedback. let's discuss this.