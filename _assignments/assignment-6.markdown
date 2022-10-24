---
layout: assignment
title:  "Assignment 6: Fritter Frontend"
categories: assignments
due_date: 2022-11-06 23:59:00 -0400
date: 2022-01-08 23:59:00 -0400
---

*Due Oct 30 and Nov 6*

**Overview.** In this assignment, you will turn the wireframes you produced in earlier assignments into a fully fledged reactive user interface. You will also work on integrating the interface with the Fritter backend service you developed in the previous assignment, to produce a complete _full stack_ Fritter application. <!-- As a final step, you will test your app out with potential end users to evaluate how well it addresses some of the needs and issues you had identified all the way back in A1. -->

**Purpose.** This assignment will help you: (1) gain more experience with HTML and the DOM; (2) practice the idioms of reactive programming and Vue.js, a widely-used client-side framework (note: we will be using [Vue v2](https://v2.vuejs.org) which, for now, has broader ecosystem support); (3) develop skills in the visual and interaction design of user interfaces<!--; (4) experience conducting user testing to evaluate your resultant application-->.

**Deadlines.** Like the previous assignment, you will have two weeks to work on this assignment. Your final submission will be due 11:59pm on Sun Nov 6. However, you will be expected to **submit an intermediary milestone half way through (i.e., 11:59pm on Sun Oct 30)** containing deliverables specified below. This milestone will only be graded for completion (i.e., whether you have submitted the required materials), and the assignment will be graded as a whole after the conclusion of the final deadline. This milestone will be [graded like the A5 milestone](https://61040.csail.mit.edu/t/clarification-on-assignment-5a-milestone-grading/558).

## Your Tasks

1. **Starter Code.** Fork this [GitHub repository](https://github.com/61040-fa22/fritter-frontend) by clicking the green "Use this template" button and selecting your _personal GitHub account_ (we cannot use the `61040-fa22` GitHub organization due to limitations with the free tier of the deployment platform, Vercel). This repository contains starter code for the assignment, and the `README.md` file describes its structure. Read through this file, and follow the initial steps to install the required packages via `npm install`. Verify that you're able to get the Fritter frontend running locally. Familiarize yourself with what this starter code provides, and how it is structured and written as it can helpfully guide you as you implement your frontend. 

2. **Heuristic Evaluation.** In contrast to A4, where you focused on reviewing and refining your *conceptual design*, this time conduct a heuristic self-evaluation to assess the *linguistic and physical* aspects of the design of the wireframes you constructed in A3 and A4. **Pick two heuristics from each of the three categories** found at [the bottom of this page](#heuristics-for-evaluation), and use them to generate a bulleted list of observations about what they suggest about your wireframes. For example, what design decisions do your wireframes make that support the heuristics? Or, do your wireframes violate them in particular ways? In either case, do the heuristics suggest improvements you might make? Finally, what tradeoffs exist between optimizing for some of these heuristics (e.g., have you had to make some sacrifices to learnability to boost efficiency)? Make sure to clearly identify the heuristics you are responding to, and keep your observations grounded by ensuring that you cite a specific aspect of your wireframes with every observation. 

    In total, you should aim to generate about three-quarters of a page of observations. Your final frontend implementation should reflect design improvements that emerged from your heuristic evaluation. 

3. **Reactive Components.** Implement your wireframe designs as a series of individual Vue.js components. These components should cleanly separate concerns — each component should be responsible for managing its own state/data and other behavior. Note: there may not be an exact one-to-one correspondence between your Fritter concepts and Vue components as some components may combine data from multiple concepts, or vice versa. Components may be nested within one another, and will need to pass data back and forth accordingly (i.e., via props when passing data from a parent component to a child, or by emitting custom events to pass data vice-versa). The resultant user interface should be _reactive_: the web page should not need to be refreshed or reloaded to see the effect of the user's action. 

     When implementing your components, consider how you might ensure your frontend interface is also robust to erroneous input and remains accessible to a broad range of users. For instance, can you validate the values of form widgets before submitting them to the backend service? Instead of [generic `<div>` tags](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/div), can you use more specific tags that convey [the semantics](https://developer.mozilla.org/en-US/docs/Glossary/Semantics#semantics_in_html) of their content?

     For this task, we recommend focusing exclusively on the _functionality_ of your components. Aesthetic concerns will come next. 

4. **Styling and Layout.** Once you have your component tree implemented, turn to the aesthetic aspects of your user interface design. Make choices for the layout of your components, as well as the colors and typography they use, to provide a usable, accessible, and pleasant experience for your users. Think about how you can use these different aspects of style to convey importance (e.g., using colors to indicate successes or errors) or an order of operations (e.g., left or right sidebars, or heading levels to suggest an outline). 

5. **Deployment.** Deploy your code so that your Fritter frontend and communicates with your previously deployed Fritter backend from A5. See the deployment guide in the `README.md` file for more instructions.

<!--
6. **User Testing.** At this stage, you now have a complete and working full-stack Fritter application — hooray! As a final step, evaluate your working application by conducting **two 30-minute user studies**. Your user study participants can be anyone of your choosing. But, each study should be conducted with a different participant, and these participants should not be taking 6.1040. The goals of these studies are two-fold: (1) how well does your Fritter address some of the needs and/or ethical concerns that you had surfaced? (2) how usable is your Fritter?

    Before conducting the study, spend a little time planning how you will use the 30-minute session. We recommend using 20 minutes to ask participants to complete simple tasks with your application, particularly focusing on the novel concepts you have introduced. Carefully observe how they use the interface, taking notes on any problems that they have. Try not to jump in and tell them what to do! In the final 10 minutes, conduct a brief debriefing interview asking participants to reflect on their experience with using Fritter — what worked well, and what could be improved?

    After the interview, look over and reflect on your notes. Synthesize a **two paragraph summary** of your user tests, thinking about what the results suggest in terms of Fritter's strengths, its ongoing limitations, and opportunities for future versions. For example, what did you observe your participants do that surprised you, or was unexpected? Post this summary to your portfolio.

-->

## Deliverables

You have two weeks to work on this assignment. After two weeks (i.e., by 11:59pm on Sun Nov 6), you should have a fully implemented and deployed Fritter frontend that is accessible at a public URL.  

However, one week in (i.e., by 11:59pm on Sun Oct 30), we would like you to make a milestone submission to signal you are making adequate progress. This milestone will only be graded for completion (i.e., only to determine that you have submitted the required materials). Your milestone materials should include the following:

* Completed heuristic evaluation and writeup.
* A fully working set of components corresponding to _one_ concept in your Fritter design. For the milestone, you do not need to worry about styling or deployment; the implemented concept need only work locally and can remain unstyled (i.e., using the default styles).
<!-- * A plan for your user testing. Post a brief one-paragraph description of who your participants will be (no need to name them, but instead explain why you have selected them as study participants by, for example, describing their demographics or other characteristics), what you will ask them to do, and what questions you might pose in the debriefing portion. -->

To help make all parts of this assignment accessible, your portfolio should provide prominent links to your Fritter frontend code repository and deployed frontend.

## Submission

For the milestone submission, follow the two-step process from previous assignments (i.e., post necessary material to your portfolio, and submit the [Google form](https://docs.google.com/forms/d/e/1FAIpQLSeS0cKbhu0JGUy1as6ObkDzvLoGnMdHPVht-os1uz7E0Vmbuw/viewform) to confirm your Git commit hash).

For the final submission, update or add new material to your portfolio. Then, submit the [Google form](https://docs.google.com/forms/d/e/1FAIpQLSeS0cKbhu0JGUy1as6ObkDzvLoGnMdHPVht-os1uz7E0Vmbuw/viewform) **_twice_**: once with your portfolio URL and its Git commit hash, and second with your deployed Fritter frontend URL and the corresponding Git commit hash for your frontend repo.

## Rubric

| Component | Excellent | Satisfactory | Poor
| ----- | ----- |----- |----- |
| **Heuristic Evaluation** | Application of heuristics suggests refinements to the frontend design that improves the user experience, and exposes tradeoffs. | The observations largely focus on how wireframes adhere to heuristics. Only relatively minor improvements are identified. Tradeoffs are shallow or missing. | Heuristics did not expose many substantive opportunities to improve the frontend design. Tradeoffs are missing. |
| **Functionality** | The frontend supports all the functionality described by the operational principles and actions of the Fritter concept designs.  | The frontend supports most of the functionality described by the operational principles of the Fritter concept designs, but some actions or other parts are missing. | Even the operational principles are not fully implemented in the Fritter frontend. |
| **Robustness** | Where appropriate, client-side validation and error checking is performed; informative error messages are shown | Client-side validation is performed to detect errors, but some missed opportunities to improve robustness or user-friendliness with regards to error messages. | Several parts of the frontend fail to perform client-side validation to catch errors. Error messages are missing or opaque. |
| **Component Construction** | Components cleanly separate concerns, and use semantic HTML tags wherever possible. Entire app is reactive, requiring no page refeshes. | Occasional components are monolithic or mix together several different purporses. Generic HTML tags are sometimes used when a semantic alternative is available. App is largely reactive, but occasionally requires a page refresh. | Many components are monolithic, and semantic HTML tags are rarely used. App is hardly reactive, requiring several page refreshes. |
| **Styling & Layout** | Layout and styling give a pleasant and intuitive user experience.  | Layout and styling give an intuitive user experience, but occasional rough edges undermine cohesion. | Layout and styling are minimal and fail to provide a usable experience. |

<!--| **Creativity & Polish** | You exceeded the parameters of designing and implementing the Fritter frontend. For example, through an especially creative or attractive use of typography, color, layout, etc. | You met all the parameters of designing and implementing the Fritter frontend. | You met most of the parameters of designing and implementing the Fritter frontend. |
| **User Testing** | A crisp and insightful description provides both a critical analysis of the current state of Fritter, and identifies compelling opportunities for future version.| A well-structured report of user testing but analysis focuses primarily on positive aspects of Fritter's design. Ideas for future versions large focus on refining the current experience. | A shallow reflection that offers only straightforward or trivial insights about Fritter and its future versions. |-->

In this assignment, we're offering an additional _optional_ category for **Creativity and Polish.** You may earn up to +0.5 points by demonstrating an attention to detail or particularly creative use of styling and layout to enable an intuitive, usable, and pleasant frontend experience. Note, this work is **not required**, but we offer this category because we know some of you will enjoy doing this work. These additional points will not take you over the maximum score of 10/10 — so there is no pressure to do this. Rather, these points can help make up for those lost elsewhere.

As in previous assignments, while rubric cells may not map to specific point scores, qualitative judgments correspond roughly to grades of A (9/10), B (8/10), C (7/10).


## Advice

* **Review 6.031 material.** This assignment builds on ideas covered in 6.031 including [callbacks and graphical user interfaces](https://web.mit.edu/6.031/www/fa21/classes/20-callbacks-guis/) and [asynchrony and Promises](https://web.mit.edu/6.031/www/fa21/classes/22-promises/). While we will briefly cover these ideas in lecture and recitation, we recommend working through the materials from 6.031 if these ideas are new to you, or you haven't seen them in a while.

* **Attend recitation.** We have devoted three recitations (Thu Oct 20, Thu Oct 27, and Thu Nov 3) to discussing ideas pertinent to this assignment. If you missed recitation, be sure to look through the relevant material on the class website (including slides and exercise code and solutions).

* **Extended studio hours.** To make sure you have plenty of technical and design support throughout this assignment, we will be using lecture time on Mon, Oct 31 as an extended set of studio hours with several TAs available to help.

* **Collaboration.** As a reminder, our class guide encourages you to collaborate with one another as long as you actually write up your work by yourself and note the set of people you collaborated with. To help you find partners to collaborate with, you can use the MIT [psetpartners app](https://psetpartners.mit.edu/). 

* **Third-party code.** Similarly, as per our class guide, you are free to use any third-party code (whether as libraries or code snippets) provided that it is publicly available and appropriately cited (see the [section on code](http://integrity.mit.edu/handbook/writing-code) in the MIT [handbook](https://integrity.mit.edu/) on academic integrity for more details).

* **Color palettes.** Finding colors that work together can be tricky business. We recommend using a color palette generator like [Coolors](https://coolors.co) or [Adobe Color](https://color.adobe.com). 

* **Typography.** You are not restricted to the basic fonts available in the browser. Instead, feel free to browse the large libraries of free fonts available via [Google](https://fonts.google.com) and [Adobe](https://fonts.adobe.com) — follow the instructions for how to include such fonts in your Vue app. If you Google around, you'll find lots of recommendations for which fonts are popular currently, and how you might mix fonts together (e.g., a serif font for body text, and a sans serif font for headings, etc).

* **Consult documentation.** [Vue.js](https://v2.vuejs.org) is a widely used package, with extensive documentation that provides useful references. Note, if you use third-party packages, or follow StackOverflow answers, be sure to double check compatibility: we are using **Vue v2 instead of v3** in this assignment. 

* **Code quality.** While we will not be grading your code, we expect you to organize your code thoughtfully, with appropriate structure, names, comments, etc. If you write sloppy code, you will likely find it harder to achieve reliable functionality (which we _will_ be grading).

## [Heuristics for Evaluation](#heuristics-for-evaluation)

The heuristics for task #2 are as follows (pick two from each category):

* **Usability criteria:** capture the broad overall goals that your visual and interactive designs might be trying to satisfy
    * _Learnability:_ how rapidly and easily can users understand how to operate the interface?
    * _Efficiency:_ once you know how to use an interface, can you use it to quickly and efficiently accomplish your goals?
    * _Safety:_ how does the interface guard against people making mistakes? 
    * _Error tolerance:_ how easily can a user recover from making mistakes?
    * _Security_: how does the interface ensure a user's privacy and integrity?
    * _Pleasantness:_ how aesthetically pleasing or calming is the interface?
    * _Accessibility:_ is the interface usable by people with disabilities (e.g., visual, auditory, and motor disabilities)?
* **Physical heuristics:** describe characteristics about the user interface that affect how users might operate it
    * _Fitt's Law:_ how quickly and easily can users reach for (or point to with their cursor) interface elements?
    * _Perceptual fusion:_ how does the interface account for time delays?
    * _Gestalt principles:_ does the layout of the interface elements convey conceptual structure?
    * _Mapping:_ does the layout of the interface elements match their function? 
    * _Situational context:_ how does the interface convey to a user their context (where they are, the app's state, etc.), and how does it adapt to their context?
    * _Accelerators:_ what shortcuts does the interface provide to speed up expert users?
* **Linguistic level:** describe cultural conventions and norms about the interface
    * _Speak a user's language:_ does the interface use simple, helpful informative messages? are there instances where messages might only be understandable by developers?
    * _Consistency:_ does the interface reuse the same names, symbols, and icons for the same concepts or actions? how consistent is the interface with others across the same application domain or platform?
    * _Information scent:_ how does the interface provide hints for navigation to aid a user in "foraging" for information?
    * _Recognition vs. recall:_ does the interface force a user to remember operations?