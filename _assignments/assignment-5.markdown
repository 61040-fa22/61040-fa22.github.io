---
layout: assignment
title:  "Assignment 5: Fritter Backend"
categories: assignments
due_date: 2022-10-23 23:59:00 -0400
date: 2022-01-04 23:59:00 -0400
---

**Overview.** Congratulations! In the last few weeks, you developed a design for Fritter, your Twitter clone, comprising a coherent and refined set of concepts. In the next few weeks, you'll realize your design as a  working implementation.

In this assignment, you'll focus on Fritter's server-side functionality. We will give you starter code that implements the functionality for two basic Fritter concepts: User (including login and sessions) and Freet (i.e., posts). Your job is to extend this code— adjusting these concepts as need be and adding additional concepts—so that you have a working implementation of your refined design.

As you work through this assignment, you are likely to find that translating your abstract design ideas into code surfaces issues with your design that you had not previously seen. For example, perhaps you made some assumptions about how a concept would be used, or perhaps there are some ambiguities in your design. Feel free to make any changes to your conceptual design that you feel are necessary, but you do take careful notes on changes that you make. These notes will inform a brief design reflection that you'll also submit, summarizing the changes you made and their rationales.

<!-- An application's backend should be thought of as an interface in its own right—enabling future developers to build a variety of different frontend clients for Fritter (e.g., a website, a mobile app, etc), or even to use Fritter's services in other apps. 

As a result, implementation will continue to involve making design decisions. For instance, you are likely to find that translating your abstract ideas into code imposes a different set of pressures on your concepts than those you had considered thus far (i.e., end user needs or ethical considerations via VSD). How you account for these new design questions will be a central challenge of this assignment. -->

**Purpose.** This assignment helps you practice: (a) formulating concept states with abstract data models; (b) translating abstract data models into concrete data representations; (c\) designing web service endpoints that conform to RESTful design principles; (d) implementing a client-server architecture using Node.js and Express.

**Deadlines.** The final version of this assignment is due in two weeks' time (11:59pm on Sun Oct 23), but you must also submit an intermediary milestone halfway through (11:59pm on Sun Oct 16) containing deliverables specified below. This milestone will only be graded for completion (i.e., have you submitted the required materials), and the assignment will be graded as a whole after the conclusion of the final deadline.

## Your Tasks

1. **Starter Code.** Fork this [GitHub repository](https://github.com/61040-fa22/fritter-backend) by clicking the green "Use this template" button and selecting your _personal GitHub account_ (we cannot use the `61040-fa22` GitHub organization due to limitations with the free tier of the deployment platform, Vercel). This repository contains starter code for the assignment, and the `README.md` file describes its structure. Read through this file, follow the initial steps to install Node.js, Express and other necessary packages as well as register for the cloud-based services for MongoDB (your persistent data store) and Vercel (the deployment platform). Verify that you're able to get the Fritter backend service running locally. Familiarize yourself with what this starter code provides, and how it is structured and written as it can helpfully guide you as you implement your novel concepts. 

2. **Data Modeling.** For each of the concepts in your  design (the final, modified version from the previous assignment), create an **abstract data model** of the state, comprising, for each concept, a list of state variables, each declared to be a set, or a relation from one set to another. Make each concept as **generic** as possible, and create a new concept header to show (after the concept name) any type parameters. Write a definition of your app as a **list of concepts**, with type parameters instantiated appropriately, and **draw a diagram** showing the state of the entire app, with contours showing which subdiagrams belong to which concepts.

4. **Data Representation.** Convert each of your data models into concrete data types (i.e., a `[concept]/model.ts` file) and functions for interfacing with the database (i.e., a `[concept]/collection.ts`). As you build out the rest of your web service, you might find it beneficial to add additional controller functions (or refine existing ones) to better capture common querying patterns. You will probably want to iterate on your data representations as you work on the assignment. 

5. **RESTful Routes.** For each of your concepts, expose their actions as routes that follow the RESTful principles discussed in lecture and recitation. In particular, URL paths should correspond to different _resources_ and [HTTP methods](https://restfulapi.net/http-methods/) should indicate the _operations_ that can be performed on the resource.   When designing and implementing your routes, consider how to make your web service robust to malformed or erroneous requests, or access violations. Remember, too, that your web service is itself an interface (i.e., for frontend developers). So, how might you use appropriate [HTTP status codes](https://en.wikipedia.org/wiki/List_of_HTTP_status_codes) and error messages to communicate why a request was rejected? **Document your routes** in the `README.md` file, following the format the starter code already provides. To test your routes, and to demonstrate their functionality, you will need to **extend the lightweight frontend** following the instructions provided in the starter code `README.md`.

8. **Deployment.** Deploy your code so that your Fritter service (and the provided GUI) can be accessed at a public URL. See the deployment guide in the `README.md` file for more instructions.

9. **Design Reflection.** Once you have a working Fritter service, reflect on how implementing it affected your original conceptual designs. What ambiguities or omissions did you discover in your designs that needed to be resolved? What design decisions did you make to resolve them, and what was your rationale? What alternatives did you consider, and why did you reject them? Would you have done anything differently? Write a succinct summary (i.e., no more than 300 words) of your reflection, and post it to your portfolio. 

## Deliverables

You have two weeks to work on this assignment. After two weeks (i.e., by 11:59pm on Sun Oct 23), you should have a fully implemented and deployed Fritter service that is accessible at a public URL.  

However, one week in (i.e., by 11:59pm on Sun Oct 16), we would like you to make a milestone submission to signal you are making adequate progress. This milestone will only be graded for completion (i.e., only to determine that you have submitted the required materials). Your milestone materials should include the following:

* A complete abstract data model for _all_ concepts in your Fritter design posted to your portfolio.
* A full working implementation for _one_ concept in your Fritter design. For the milestone, you do not need to worry about deployment; the implemented concept need only work locally.
* An initial outline of the design of your RESTful routes for your remaining concepts. Add this outline to the `README.md` file, following the format the starter code already provides.

To help make all parts of this assignment accessible, your portfolio should also provide prominent links to your Fritter backend code repository and deployed service.

## Submission

For the milestone submission, follow the two-step process from previous assignments (i.e., post necessary material to your portfolio, and submit the [Google form](https://docs.google.com/forms/d/e/1FAIpQLSeS0cKbhu0JGUy1as6ObkDzvLoGnMdHPVht-os1uz7E0Vmbuw/viewform) to confirm your Git commit hash).

For the final submission, update or add new material to your portfolio. Then, submit the [Google form](https://docs.google.com/forms/d/e/1FAIpQLSeS0cKbhu0JGUy1as6ObkDzvLoGnMdHPVht-os1uz7E0Vmbuw/viewform) **_twice_**: once with your portfolio URL and its Git commit hash, and second with your deployed Fritter URL and the corresponding Git commit hash for your backend repo.

## Rubric

| Component | Excellent | Satisfactory | Poor
| ----- | ----- |----- |----- |
| **Data models** | Simple and compact relational model of state for each concept that has no redundancies, and is sufficient to support actions | Relational model of state for each concept that is sufficient to support actions but may be needlessly complicated and include small redundancies | Models of state are insufficient to support actions or not clearly relational |
| **Genericity** | Concepts are generic when possible, and genericity is clearly indicated by parameterized data models, and instantiated appropriately | Concepts are generic when possible and genericity is clearly indicated, but some opportunities for genericity are missing or instantiation is unclear | Concepts are not generic when they might be, or genericity is not clearly indicated |
| **Functionality** | The deployed web service reflects all the functionality described by the operational principles and actions of the Fritter concept designs | Most of the functionality described the operational principles and actions can be found in the deployed web service, but some actions or other parts are missing | Even the operational principles are not fully implemented in the deployed web service |
| **RESTful Design** | All API endpoints are well-designed: paths map to resources and reflect appropriate hierarchical relationships, and HTTP methods indicate actions that can be performed resources | Most API endpoints follow RESTful principles, but some paths or HTTP methods are used in ways that might violate a developer's expectations about RESTful endpoints | Several API endpoints violate RESTful principles |
| **Robustness** |  Where appropriate, API endpoints anticipate malformed or erroneous input, or access violations; informative error messages and corresponding HTTP status codes are returned | API endpoints largely account for erroneous input or access violations, but some missed opportunities to improve robustness. Error messages and status codes are returned, but could be better chosen or more informative | Several API endpoints are not robust against malformed input or access violations (e.g., web service may crash). Custom error messages and appropriate HTTP status codes are not used, or are uninformative
| **Design Reflection** | A crisp and thoughtful summary of design issues that surfaced during implementation, discussing why they occurred, how they were resolved, and/or any tradeoffs or tensions involved | A clear identification of non-trivial design ambiguities or omissions, with a brief discussion of how they were addressed. However, design tradeoffs and/or tensions are not richly described. | A terse reflection that describes strawman issues or poorly explains design decisions

## Advice

### Abstract data models

- **Reviewing lecture**. You may want to review the data model lecture slides and video for examples of state variable declarations and global data diagrams.

- **Relations over more than two sets**. You don't need to have relations that involve three or more sets, because you can always introduce a "tuple set" (like `Entry`, the set of entries in the UnixFolder example). 

- **Multiplicities**. A relation can map an object in one set to any number of objects in another set: exactly one (in which case it represents a total function); zero or one (a partial function); or anu number (a general relation). Use the keywords `one`, `lone` and `set` for these three cases.

- **Sequences**. There's no need for a special sequence constructor. A sequence of objects of some type `T` can be viewed as an ordering (a relation `T -> T`), or as a mapping from indexes to `T` (a relation Int -> T).

- **Examples**. Here are some examples of declarations illustrating you the various forms they can take:

```
root: Folder // root of file system is a single folder
trash: set Object // the deleted objects in the trash
upvoters: Item -> set User // for each item, user that upvoted
upvotes: User -> set Item // for each user, items they upvoted
password: User -> one Password // one password for each user
hint: User -> lone Hint // each user may have a password hint
```

- **Instantiaton of generics**. In your application declaration, you should list each concept in the app, along with a list of types corresponding to its parameters. These types should be types that come from other concepts, and should be referred to as `C.T`, where `C` is the concept and `T` is the type. For example, if your app included a generic Favorite concept in which the items being favorited were the freets from the Freet concept, and a Follower concept in which the parties following and being followed were the users of the User concept, and the published items were freets, you might write something like:

```
app Fritter
concepts
  Freet
  User
  Favorite [Freet.Freet]
  Follower [User.User, Freet.Freet]
```

### Web Service Implementation

* **Attend recitation.** We have devoted three recitations (Thu Sep 29, Thu Oct 6, and Thu Oct 13) to discussing ideas pertinent to this assignment. If you missed recitation, be sure to look through the relevant material on the class website (including slides and exercise code and solutions).

* **Extended studio hours.** To make sure you have plenty of technical and design support throughout this assignment, we will be using lecture time on Mon, Oct 17 as an extended set of studio hours with several TAs available to help.

* **Collaboration.** As a reminder, our class guide encourages you to collaborate with one another as long as you actually write up your work by yourself and note the set of people you collaborated with. To help you find partners to collaborate with, you can use the MIT [psetpartners app](https://psetpartners.mit.edu/). 

* **Third-party code.** Similarly, as per our class guide, you are free to use any third-party code (whether as libraries, [Node packages](https://www.npmjs.com) or code snippets) provided that it is publicly available and appropriately cited (see the [section on code](http://integrity.mit.edu/handbook/writing-code) in the MIT [handbook](https://integrity.mit.edu/) on academic integrity for more details).

* **Consult documentation.** [Express](https://expressjs.com) and [Mongoose](https://mongoosejs.com) are both widely used packages, with extensive documentation that provide useful references. 

* **Code quality.** While we will not be grading your code, we expect you to organize your code thoughtfully, with appropriate structure, names, comments, etc. If you write sloppy code, you will likely find it harder to achieve reliable functionality (which we _will_ be grading).

* **Code modularity.** Try to ensure that each concept is implemented in its own module (including models, collections, routes, middleware, etc.), and that concept modules have as few dependences on each other as possible.

* **Keep detailed notes.** In our experience, it's often hard to look back on your design and implementation process and "un-see" the solution you've crafted. Once you're done with your implementation, your web service will feel like the only or most obvious way to address any design problems that cropped up. And, chances are, you will have a difficult time remembering the alternatives you had considered. 

  Consider keeping a lightweight notebook to document your progress. This might comprise just a collection of bullet points that describe what you're currently working on, what issues you are hoping to address, why you believe an idea might work, and what limitations or problems you encounter along the way. You can then synthesize your design reflection from your notebook, and doing so will feel easier, more productive, and yield a more compelling reflection.
