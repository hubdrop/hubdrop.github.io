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

Each team can be assigned one of three possible permissions: "Pull", "Push & Pull",or "Push, Pull & Administrative".

I first created a team called "ProjectName Committers" and gave them Push & Pull access. Then I created a team called "ProjectName Administrators, and gave them "Push, Pull, & Administrative" permissions. 

HubDrop now can add those with "Write to VCS" on drupal.org to the "Project Committers" team, and those with "Edit project" will be added to "Push, Pull, & Administrative".

## Too Much Freedom

Being on the "Project Administrators" team allows you to quite a few things, but not the one thing we need it to do the most: allow the project maintainer to edit the Team.  

Some of the powers it grants are too much. We don't have control over this.  The problem is, we want to allow some things, but not others:

Things we don't want to allow:
1. The ability to change the repo name & the default branch
2. Edit the short description and link, 
3. Enter the DangerZone™: Make the repo private, transfer ownership, or delete the repo!
4. Add deploy keys.

Things we do want to allow:

1. Turn wikis, issues, and pages on and off.
2. View all collaborators.  You cannot edit them.
3. Administer Service Hooks

The only two ways around this are:

1. Moving the project to another user or organization, owned by the module maintainer.
2. Using HubDrop.io and the GitHub API as a wrapper for turning wikis and issues on and off.

Both tasks will require much more programming.

## "Official Mirrors" vs "Development Repos" vs Both?
If the ability to set a project's source to the github organization of choice were implemented, then perhaps every repo at github.com/drupalprojects could just be an "official mirror", just as https://github.com/drupal/drupal does it. It was an idea originally to reach out to the owners of the "drupal" organization on github to see if hubdrop could provide those mirrors, and to see if github would mark them as "official mirrors".

Letting module creators use their own github organization to own their modules would probably be a welcome feature.

This would empower the developers by putting them in the "owners" team. This would let maintainers decide on github who has push or pull access, avoiding the need for maintaining that info on drupal.org.

