---
title: Labs 9 - Week Four
date: '2019-02-01'
---

[Backpaca team contribution graph](https://github.com/Lambda-School-Labs/labs9-map-scratcher) | Github handle: TRIF3X

![Tech Stack](https://files.slack.com/files-pri/T4JUEB3ME-FF8NK38TX/screenshot__121_.png)

This week has be an exciting but challenging one. I was able to learn a lot more about how the data was flowing through out our app and was able to learn exactly how to update the back end and add new fields to our database. I was introduced to a new picture saving application called Cloudinary which is where I would store our new user profile pictures. GraphQL and Apollo client were definitely a massive challenge coming into the project but as I worked with these new technologies on a daily basis, I was able to really understand how the data would flow. We have our resolvers which I would be able to call mutations or queries from that would talk to Yoga on the backend.


[PR 1 - User dropdown, filter](https://github.com/Lambda-School-Labs/labs9-map-scratcher/pull/100) | [Trello Card 1](https://trello.com/c/uGiigJ4u/115-profile-page-implement-add-friend-button-in-drop-down-make-removal-from-friends-list-look-cleaner) <br>
[PR 2 - Route to user, conditional render add/remove friend](https://github.com/Lambda-School-Labs/labs9-map-scratcher/pull/113) | [Trello Card 2](https://trello.com/c/6f1ae9Tc/121-friend-profile-page-clicking-on-a-user-will-route-to-their-profile-page-where-you-can-now-add-them-as-a-friend) <br>
[PR 3 - Add bio to database, create mutation, update schema & user](https://github.com/Lambda-School-Labs/labs9-map-scratcher/pull/117) | [Trello Card 3](https://trello.com/c/hR6oVOOA/125-friend-profile-page-add-bio-to-database-create-mutation) <br>
[PR 4 - Ability to upload an image to profile](https://github.com/Lambda-School-Labs/labs9-map-scratcher/pull/123) | [Trello Card 4](https://trello.com/c/I1eOn5bz/126-ability-to-upload-images-to-profile) <br>
[PR 5 - Add header component, ability to add and edit bio](https://github.com/Lambda-School-Labs/labs9-map-scratcher/pull/127) | [Trello Card 5](https://trello.com/c/fY5qzAib/127-profile-page-add-bio-edit-bio-add-header-component) <br>

### Detailed analysis of Adding a profile picture

This week I'm going to share on exactly how you would add the ability to upload photos to Cloudinary which is the service I used to store our profile pictures. First you will set up an account at [Cloudinary](https://cloudinary.com/). 

![Cloudinary sign up](/cloudinary.PNG)

After sign up you're ready to add the widget into your code. I'm using NextJS so it may look a little bit different but you will add a script tag which imports cloudinary into your application.

> src="//widget.cloudinary.com/global/all.js" type="text/javascript"

If you were working in a plain JS codebase you could insert this at the bottom of the page as normal, but I'm using NextJS so here's an example on how to add a script tag. 

![Meta](/meta.PNG)

You will want to enter this into a Meta component which will then be placed in your pages as:

>_app.js

After you have your script tag loaded into your meta you can now add your code for the button into the component of your choosing.

![picture code](/uploadcode.PNG)

You will need to use your own cloud_name and upload_preset which is available on the home screen. Be sure to set your pictures to UNSIGNED when creating your preset. What this code is doing is after a successful upload we will grab the result and the url of the uploaded image from the response. Afterwards we will set that url onto our state which is submitted when we we submit our form.