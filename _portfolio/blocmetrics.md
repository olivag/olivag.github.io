---
layout: post
title: Blocmetrics
thumbnail-path: "img/blocmetrics.png"
short-description: An analytics service to track events on websites.
---

{:.center}
![]({{ site.baseurl }}/img/blocmetrics.png)

## Summary

[Blocmetrics](https://olivag-blocmetrics.herokuapp.com) is an API tracking service and reporting tool that you can use with web apps to track user activity and report results. View repository on [GitHub](https://github.com/olivag/blocmetrics).

## Explanation

There are plenty of good analytic services, but that doesn't mean you can't build a better one. Blocmetrics will offer a few key features:
  * A client-side JavaScript snippet that allows a user to track events on their website.
  * A server-side API that captures and saves those events to a database.
  * A Rails application that displays the captured event data for a user.


## Problem

- Allows users to sign up for a free account by providing a user name, password and email
- Blocmetrics' authentication system should allow users to sign up and send emails for account confirmation
- Allows users to sign in and out of Blocmetrics
- Allows users to register an application with Blocmetrics for tracking
- Uses URL as unique attribute
- Associate events with registered applications
- Generates an event model
- Should receive incoming events in an API controller
- Allows users to use JavaScript to capture client-side events in the application
- Displays a graph of events for each registered application

## Solution

I incorporated the Devise gem for authentication. It allowed users to sign up and send emails for account confirmation. It also gave users a way to sign in and out of the app. I included the Pundit gem for authorization, which allowed me to set up scopes for different controllers that would only allow certain users with the specified user roles to access specific areas of the app. 


I generated a Registered Application model that was associated with the user as well as an Event model to associate it with the registered application. Generated an API controller and routes in order to give Blocmetrics the ability to recieve incoming events from registered applications. Used Cross-Origin Resource Sharing (CORS) to allow cross-origin requests in a controlled manner without opening up security vulnerabilities. Incorporated the Chartkick gem to generate an events pie chart.

## Results

Blocmetrics fulfilled all the requirements it promised. It allows users to keep track of any event on their website and display it in a very readable pie chart. Blocmetrics also prevents security vulnirabilities such as cross-site scripting through CORS.

## Conclusion

This project was a great learning experience for me. I now understand how Google tracks events from web apps. They have more advance feautres im sure but this project showed me the fundamentals of how it gets done. I was also impressed on how easy it was to add a pie chart with only a few lines of code.

