---
title: Labs 9 - Week One
date: '2019-01-11'
---

[whiteboard week one](www.blank.com) | Note: not completed yet <br>
[Backpaca team contribution graph](https://github.com/Lambda-School-Labs/labs9-map-scratcher) | Github handle: TRIF3X

This week has been nothing short of exhausting, from the planning stages to getting something in the codebase. The first challenge this week came when I was tasked with deploying our very basic front-end website [Backpaca](https://backpaca.now.sh/). Deploying with a new service came with its own set of challenges, like how to use it. With very little documentation on how it works I would try to deploy from vscode in my terminal with no luck. Then came to mind, 'what if vscode just isn't at a high enough level to execute the commands I'm sending it?'. After switching to my command prompt in Windows, I was able to succesfully deploy the website by navigating to the frontend folder and typing the command 'now'. For the most part I lived in VScode, but when writing the backend using GraphQL I would use this IDE called GraphQL-Playground where I could send structured requests to the back end and in return receive only exactly what I was asking for. 

![deploying Backpaca](/deploy.PNG)

For the frontend we decided on Next.js and apollo client. This week I focused on devloping two of the components needed for Backpaca. I first built a very simple login page which would serve as our model next week when we finally connect the frontend to the backend and hook up apollo client which will be used to handle local state. And for the second component I built out our settings page to the point where we would need only need to style it and hook up our apollo client to handle the input fields.

![Settings page](/settingsPage.PNG)

[PR 1 - deployment](https://github.com/Lambda-School-Labs/labs9-map-scratcher/pull/4) | [Trello Card 1](https://trello.com/c/CEFwFKVa/12-deployed-to-the-web) <br>
[PR 2 - login page](https://github.com/Lambda-School-Labs/labs9-map-scratcher/pull/14) | [Trello Card 2](https://trello.com/c/yoGgPKY1/18-login-component) <br>
[PR 3 - settings page](https://github.com/Lambda-School-Labs/labs9-map-scratcher/pull/16) | [Trello Card 3](https://trello.com/c/eV6EyffB/30-settings-component) <br>
[PR 4 - user resolver](https://github.com/Lambda-School-Labs/labs9-map-scratcher/pull/21) | [Trello Card 4](https://trello.com/c/zDfsTLTg/44-user-needs-to-return-ch) <br>

### Detailed analysis of the user resolver

Creating the user resolver came to me as a bit of a challenge. As having no prior experience with GraphQL there was a massive learning curve, luckily I found [Howtographql](https://www.howtographql.com/) where they thouroughly explained the theory behind GraphQL as well as how to write it.

![GraphQL example query](/gqlexample.PNG)

How the user resolver works is that we have a root query which is called upon our database at the user table. We then query for that user with 
>user(id:"89udsgjkamf8ads9fj")

after we have our user from the table we can now query it for anything we would like which is defined in our schema

![Schema](/userschema.PNG)

using the User resolver we call on the Parent which refers back to the table at the id we passed in the arugment, we can then return any information we would like about the specific user that we predfined in our schema.

![Example GraphQL query](/gqlquery.PNG)

### Milestone relfections

Working with a team on a project of this size for the first time defintely was not as easy as I thought it would be. Everyone has their own needs as a developer and their own way of understanding of how things work. Trying to determine which technologies to use came at a cost, the pros and cons had to be discussed to ensure that it would meet the needs of our application. I believe originization was a huge factor in the process, at first we were working through a document and we didn't have a system in place to decide on how descions were going to be made which led to hours of discussion on the same topic. Not to mention the technologies we wanted to use for all relatively new to each and every one of us. After what seemed like all week I got to know the team a lot better and realized a lot of the friction actually came down to not know how all the procceses and communcation betweens each of the technologies worked.
