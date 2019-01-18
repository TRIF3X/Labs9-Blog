---
title: Labs 9 - Week Two
date: '2019-01-18'
---

[whiteboard week one](https://www.youtube.com/watch?v=CE9HS2gNtcA&feature=youtu.be) <br>
[Backpaca team contribution graph](https://github.com/Lambda-School-Labs/labs9-map-scratcher) | Github handle: TRIF3X

![Map component rough draft](/sample.PNG)

This week has been a very busy and productive week. I built out a lot of components and had the chance to use the react semantic-ui library to build out different UI components within the pages I had made. By mid week I was able to have a rough draft of what our main component, the map, would look like. 

![Seeding Prisma with country data](/databaseSeed.PNG)

With the backend I was able to seed the country data into the Prisma database. This came as a challenge since Prisma is a completely new technology to me for this project which meant I had to spend some time reading up on documentation and figuring out how data needs to be formated in order to be properly seeded into our database. We started with a big dataset that we use for our map component and from there I had to extract only the name and country code. After extraction I would then map over the data so that I could format it in the correct way so that Prisma would be able to understand it.

[PR 1 - landing page](https://github.com/Lambda-School-Labs/labs9-map-scratcher/pull/63) | [Trello Card 1](https://trello.com/c/ed8ndJbN/83-landing-page-rough-draft-for-a-presentable-landing-page) <br>
[PR 2 - map legend component](https://github.com/Lambda-School-Labs/labs9-map-scratcher/pull/50) | [Trello Card 2](https://trello.com/c/wV5kaFFj/62-map-view-map-legend-component) <br>
[PR 3 - country modal](https://github.com/Lambda-School-Labs/labs9-map-scratcher/pull/48) | [Trello Card 3](https://trello.com/c/HSoTllXh/78-country-modal-create-country-modal) <br>
[PR 4 - Search bar for country and friends](https://github.com/Lambda-School-Labs/labs9-map-scratcher/pull/40) | [Trello Card 4](https://trello.com/c/oJeFXanf/59-map-view-dropdown-of-friends-component) <br>
[PR 5 - Twitter button for Login](https://github.com/Lambda-School-Labs/labs9-map-scratcher/pull/31) | [Trello Card 5](https://trello.com/c/8pZ8iERY/52-twiiter-button-for-login-screen) <br>
[PR 6 - Seed country data](https://github.com/Lambda-School-Labs/labs9-map-scratcher/pull/42) | [Trello Card 6](https://trello.com/c/3Nc1FKej/21-seed-data) <br>
[PR 7 - Settings component](https://github.com/Lambda-School-Labs/labs9-map-scratcher/pull/16) | [Trello Card 7](https://trello.com/c/eV6EyffB/30-settings-component) <br>
[PR 8 - Fix Now deployment with LESS](https://github.com/Lambda-School-Labs/labs9-map-scratcher/pull/58) | [Trello Card 8](https://trello.com/c/tmwTEvYo/85-fix-now-deployment-with-less) <br>

### Detailed analysis of creating a Landing page

Since using NextJS is completely new to me I'll go ahead and go over how to create a page and components for that page. NextJS is a react framework that provides SSR for lightweight applications that is suprisingly very simple to build on. For a landing page I went ahead and used a file under the pages directory called index.js. The pages directory is where you do all the routing, each page would be a different page in your application.

![picture of pages directory](/pages.PNG)

Inside of the landing page you place components which is the actual content you will see when the page is rendered.

![picture of page format](/landing.PNG)

When writing the components that go inside your page you follow the same rules as you would when using react. You use JSX, wrap everything in a parent div, and use className instead of class.

![landing page component](/landingpagereact.PNG)

Once everything is written out, you can use [NOW](https://zeit.co/now) to deploy your awesome new website!

![Landing page rough draft](/landing-demo.PNG)


### Milestone relfections

<!-- As a part of your journal entry, write ¼ to ½ a page reflecting on your experiences working with a team to integrate several servers, pages, APIs, and services into one project. Describe how your pieces of the project interfaced with and integrated with your teammates. -->

Working with a team on a project came with its own set of challenges. One issue that would come up more often than I would like is merge conflicts. One person would be working on a component or page then someone else may come in and have to change one little thing that you're already editing causing a merge conflict. Thankfully most of the time these merge conflicts were so small we could easily solve them in a few minutes and have all our components and pages working again. Using [Trello](https://trello.com/b/32vtkJdc/labs9-map-scratcher), we were able to keep track of who was working on which files. This has helped us tremendously when choosing new tasks to work on and knowing exactly what everyone else may be doing at that point in time so that we don't edit their files while they're working and create a merge conflict. For the most part working with a team has been an exciting and wonderful learning experience, the communication has been really good which is key when working in the same folders. 