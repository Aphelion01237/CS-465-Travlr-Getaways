# CS-465-Travlr-Getaways
# Derek Paterson

## Architecture

**Compare and contrast the types of frontend development you used in your full stack project, including Express HTML, JavaScript, and the single-page application (SPA).**

The biggest differenece between the frontend development and the SPA is that the SPA isn'g designed to change often, it has simple, fast, accessible features that are there to add business value and update the content seen on the front page. We do this using Angular, which is a framework specifically for this. The frontend aspect is done in express, which is a separate framework that is build on node.js and is extremely lightweight and lets us make dynamic content for the customer side. Both of the frameworks heavily rely on javascript. 

**Why did the backend use a NoSQL MongoDB database?**

The backend used a NoSQL MongoDB database because they are incredibly easy to use, instead of setting up a whole SQL database, we can design a quick schema using mongoose and just throw it at the database, and it works. 

## Functionality

**How is JSON different from Javascript and how does JSON tie together the frontend and backend development pieces?**

JSON is set of specifically formated parameters that collectively describes an object that can be read and manipulated with javascript. In this case, the JSON is what holds our data, basically, and we use it as a message to tell the webpage what to load. The backend SPA can create new JSON objects by using the POST API route for whatever particular database schema, and the frontend reads those with a GET API call. 

**Provide instances in the full stack process when you refactored code to improve functionality and efficiencies, and name the benefits that come from reusable user interface (UI) components.**

The biggest way code was refactored in this project was using handlebars to cut down on the amount of hardcoded HTML and make things modular, so for example instead of coding out each aspect of a trip on the Travlr site, we could abstract that and reference the handlebars, which would in turn pull the information to fill the elements from the database (through the API). This is useful because that means we are able to dynamically update content without taking the server offline and it is much less likely mistakes will be made.

## Testing

**Methods for request and retrieval necessitate various types of API testing of endpoints, in addition to the difficulties of testing with added layers of security. Explain your understanding of methods, endpoints, and security in a full stack application.**

The way I went about testing was by heavily using the postman application and running POST/GET/ETC through the API on the express server. This worked really well, and once I verified that the API was working, I was able to launch the SPA backend and test the implementation of the API for things like adding trips, modifying them, and deleting them. When I implemented the security solution and had usernames/passwords, the way I made the app secure was to leverage the way angular can run a function in the html, so we called a simple function to check if the user was logged in order to make sure that destructive commands were not rendered or available unless logged in.

## Reflection

**How has this course helped you in reaching your professional goals? What skills have you learned, developed, or mastered in this course to help you become a more marketable candidate in your career field?**

This was an interesting project, although I have to say I'm not a huge fan of relying so much on node packages, there are a few recent examples of compromised packages or authors suddenly removing them from NPM that makes me sort of reluctant to use them. On the other hand, web design changes so fast that in order to implement modern features it's almost required that we use node packages to be able to keep up, so its a weird spot to be in.

That being said, this was the first time I really understood implementing a RESTful API, which was cool, and getting the mongoDB stuff working locally was interesting and informative. I also was glad to not completely abstract away the login process to something liek OAuth, so learning how that worked was very helpful as well.
