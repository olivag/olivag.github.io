---
layout: post
title: Blocipedia
thumbnail-path: "img/blocipedia.png"
short-description: A production quality SaaS app that allows users to create their own wikis.

---

{:.center}
![]({{ site.baseurl }}/img/blocipedia.png)

## Summary

Blocipedia allows users to create and collaborate on their own wikis privately or publicly.

## Explanation

Blocipedia is a great way to collaborate on community-sourced content. It allows users to create an account (either standard or premium memberships) and create wiki’s using markdown. As a premium member a user can create private wiki’s and add collaborators to help edit the wiki. This was my first project with Bloc, I was given user stories and asked to create features based on those stories.

## Problem

- Allows users to sign up for a free account by providing a user name, password and email
- Blocipedia's authentication system should allow users to sign up and send emails for account confirmation
- Allows users to sign in and out of Blocipedia
- As a developer, offer three user roles: admin, standard, or premium
- Users should default to the standard role when they are first created
- Allows users with standard accounts to create, read, update, and delete public wikis
- Allows users to upgrade their account from a standard (free) to premium (paid plan) account
- Private wikis should remain private as long as users maintain their premium service. If they downgrade, all of their private wikis should become public
- Allows premium users to create private wikis
- Allows all users to edit their wikis using Markdown syntax
 Allows Users to add and remove collaborators from a private wiki via its edit page

## Solution

I incorporated the Devise gem for authentication. It allowed users to sign up and send emails for account confirmation. It also gave users a way to sign in and out of the app. I included the Pundit gem for authorization, which allowed me to set up scopes for different controllers that would only allow certain users with the specified user roles to access specific areas of the app. I used the callback approach to implement default values for roles. I also used Stripe to charge users before switching their account role from standard to premium.

## Results

Blocipedia successfully allows users to create public and private Markdown-based wikis as well as enabling them to easily upgrade or downgrade their account. Blocipedia has proven to be simple and intuitive to use and is fully responsive. 

## Conclusion

As my first project working with Rails, Blocipedia provided many interesting challenges. Stripe integration was a helpful experience. The API offered by Stripe is an excellent tool for monetizing a subscription service. This project also provided opportunities to work on different levels of authorization for different users. The addition of collaborators stretched my understanding of joined tables. Building data relationships is sometimes difficult to conceptualize so I appreciated the opportunity to practice by relating wikis and users through collaborators.