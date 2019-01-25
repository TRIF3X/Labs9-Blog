---
title: Labs 9 - Week Three
date: '2019-01-25'
---

[Backpaca team contribution graph](https://github.com/Lambda-School-Labs/labs9-map-scratcher) | Github handle: TRIF3X

![Apollo + GraphQL](/GraphQL-Apollo.jpg)

Week three is finally here which means the application has to be feature complete, with some bugs being acceptable. This week was completely all front end work, I would start by converting our styling to use our LESS preprocessor which would come at sort of a challenge integrating with the semantic-ui we have chosen for our styling framework. I would also come to creating the profile component which was a very basic rough draft for now as we decide on how we want to style our application. Next we needed to make our application mobile friendly so I would need to create a responsive design from both the profile page and the landing page which was more time consuming than difficult. Last the real challenge came with the country modal component. Using Apollo client and being a completely new technology to all of us create quite a bit of head ache since a lot of our time was spent peer programming with trial and error trying to determine how exactly Apollo client expected the mutations to be laid out.

[PR 1 - Covert components to LESS](https://github.com/Lambda-School-Labs/labs9-map-scratcher/pull/71) | [Trello Card 1](https://trello.com/c/iHnPAKcL/91-convert-inline-styles-to-less) <br>
[PR 2 - Profile component](https://github.com/Lambda-School-Labs/labs9-map-scratcher/pull/73) | [Trello Card 2](https://trello.com/c/HsBwAeu8/96-profile-create-profile-component) <br>
[PR 3 - Country view modal refactor](https://github.com/Lambda-School-Labs/labs9-map-scratcher/pull/77) | [Trello Card 3](https://trello.com/c/zKTbU8lm/99-countryviewmodal-refactor-country-modal-into-smaller-components) <br>
[PR 4 - Country modal friends list query](https://github.com/Lambda-School-Labs/labs9-map-scratcher/pull/80) | [Trello Card 4](https://trello.com/c/2IrJPSvH/102-country-modal-friend-list) <br>
[PR 5 - Profile page responsive design](https://github.com/Lambda-School-Labs/labs9-map-scratcher/pull/86) | [Trello Card 5](https://trello.com/c/vZvpooIR/107-profile-page-fix-styling-make-responsive) <br>
[PR 6 - Landing page responsive design](https://github.com/Lambda-School-Labs/labs9-map-scratcher/pull/87) | [Trello Card 6](https://trello.com/c/AhQVRHWS/109-landing-page-responsive) 
<br>

### Detailed analysis of Apollo client queries

In my analysis for the Apollo client queries I will show how I designed a query to get the friends from a specific user and display them on the friends list. First we will need to create our request to the client cache to retrieve the current user.

![Query user from client cache](/queryUser.PNG)

We can now use this within our component. After Retrieving the user we will then query the travels based on that user.

![Query travel by user](/queryTravel.PNG)

Once we have the travels by the user we can now insert them into our semantic-ui component. We will insert the name into the first table cell and the type of visit in the next table cell. We had defined our visits in the database by a number system, so we will also need to map over our visits and convert each number to their actual visit.

![Map our data to the table](/queryMap.PNG)



### Milestone reflections

<!-- As a part of your journal entry, write ¼ to ½ a page reflecting on your experiences working with a team to convert a disparate set of components into a single, cohesive, and complete product. Describe the challenges you faced and the steps you took to overcome them. -->

This week was all about the different components and the functionality they would need. The main component that I worked on was the country modal. I began by breaking down the country modal I wrote in week 2 into multiple different components. After everything was broken down we were able to go in and add the mutations and queries to each component that would make up the modal component. A lot of the difficulty came from using Apollo client. Apollo client wouldn't allow for us to have conditional rendering within a component that needs several mutations. After hours of trying to determine how this would be possible, Kyran would find that using conditionals that would render different components would be the best method to have everything work together. This project has been an incredible learning experience, working with multiple individuals to create a complex web application and being able to using new technologies like GraphQL and Apollo client.