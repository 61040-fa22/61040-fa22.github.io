---
layout: assignment
title:  "Assignment 3: Fritter Converge"
categories: assignments
due_date: 2022-10-02 23:59:00 -0400
date: 2022-01-02 23:59:00 -0400
---

**Overview**. In your remaining individual assignments, you'll design and implement Fritter, your own version of Twitter. Fritter won't have the breadth of functionality or the scalability of Twitter itself, but it will be a coherent and polished product that is complete enough to demonstrate your novel design ideas convincingly.

In this assignment, you'll design your Fritter application. In subsequent assignments, you'll implement this design. You won't be tied to implementing exactly what you specify here, and you will in fact have an opportunity to revise your design in a later assignment. For now, however, you should assume that your initial implementation will hew closely to the design that you specify here.

In the last assignment, you engaged in "divergent design," generating a collection of exciting conceptual design ideas that were promising but not fully developed. In this assignment, you'll do "convergent design." Whereas divergent design aims at breadth and diversity of ideas, convergent design aims to winnow the ideas down and solidify them. So you'll now revisit your ideas, selecting the strongest concepts (and perhaps combining, augmenting and adjusting them); specifying them more precisely; and fitting them together into an overall application design. 

This assignment also includes wireframing, as you start considering how to turn your conceptual ideas into a concrete application, moving your attention from purely conceptual concerns to physical and linguistic aspects of user interface design.  Your wireframes will serve as an initial blueprint for later assignments in the class that will focus on frontend design and implementation. In this assignment, the focus will not be on the detailed layout and mechanics of your user interface, but on the more basic questions of whether the interface provides access to the underlying concepts and reflects the concepts in a clear way.

**Purposes**. The purposes of this assignment are to give you practice in three broad areas: (a) designing a software application with concepts, elaborating the concepts and fitting them together with appropriate synchronizations; (b) translating conceptual designs to concrete user interfaces, and representing them with wireframes; (c\) approaching design decisions in terms of tradeoffs.

## Tasks

Here is an overview of the design work you'll do in this assignment. We expect this to be an iterative process, with each of you approaching it in your own way. So take this section as an outline of roughly what we expect, and make sure to check the next section for the exact deliverables.

- **Design your concepts**. Starting with the concept ideas from your previous assignment, select your favorite concepts, and figure out how they will work together. You might want to think about a variety of user scenarios, and what they suggest about the connections between the concepts (in terms of synchronization and shared object references). As you do this, you can adjust the concepts in any way you please; combine or split concepts; and include additional concepts that you did not mention there, whether known or invented. As you consider the detailed design of each concept, and how the concepts will fit together, you'll anticipate problems that you had not previously considered. You should fix all the problems that you anticipate (at least as much as possible). During this process, you may want to construct additional sketches.
- **Design your user interface**. When you are satisfied that you have a plausible design, you'll construct wireframes for the app. Doing this may reveal additional problems, so don't be surprised if you have to go back and modify your concepts.
- **Taking notes**. Make sure throughout to take careful notes of any design insights you have or problems that you see. You'll use these notes in your discussion of tradeoffs.

## Deliverables

- **Pitch**. Write a succinct (100 to 300 word) product pitch for your Fritter app, which explains in a concrete and compelling way what it offers, both to its immediate users and in terms of the larger social and ethical impacts that you identified in your first assignment. Your pitch should mention the concepts you have selected for your design, but should not describe them in any detail, and should mention any particular problems or flaws with Twitter that your app addresses.
- **Concepts**. Specify each of your concepts separately, with a name, purpose, operational principle, states and actions. For each action, provide a succinct informal spec that says how the action updates the state (and if relevant, under what conditions, as a property of the state, it is allowed to occur). Indicate which concepts are intended to be familiar, known concepts, and which are novel. These concepts will likely include some kind of user authentication concept, and some kind of posting concept; you can adopt the known concepts in their familiar form for these (or adjust them, as you please). In addition, we expect at least three additional concepts, of which at most one may be a known concept without adjustment. 
- **Synchronizations**. Specify any synchronization rules that define how concepts are linked together (usually to produce automation). Each rule should specify that the occurrence of an action in one concept is tied to the occurrence of an action in another concept (perhaps only when some condition on concept states holds).
- **Wireframes**. Create a collection of wireframes that cover the essential views and interactions that a user would experience in using your app. Include a link to your live Figma models, and also some embedded screenshots (focusing on your most interesting concepts) with informative captions explaining them.
- **Tradeoffs**. Using the notes that you took during your design process, pick at least 3 design decisions that you made in which you had to choose between multiple options. For each one, provide (a) a pithy title naming the issue; (b) an outline of what the various options were; (c\) a rationale for why you chose one option over the others. Try to keep your analysis below 300 words in total (for all the decisions).

## Submission Process

Submitting your work is a two-step task. First, post it to your Jekyll portfolio by the assignment deadline. The specific structure and format of the submission (e.g., adding it as a [blog post](https://jekyllrb.com/docs/posts/) or [page](https://jekyllrb.com/docs/pages/), splitting the deliverables across multiple posts/pages or consolidating them as a single one, the [permalink/URL](https://jekyllrb.com/docs/permalinks/) format, etc.) is left entirely up to you and is part of the ongoing design exercise of developing an attractive and usable portfolio. Second, submit [this Google form](https://forms.gle/dGanRBvsFYFoQNGy8) to finalize your assignment submission, also by the deadline. You must do both steps for us to consider your assignment submitted. 

## Rubric

| *Part* | Excellent | Satisfactory | Poor
| ----- | ----- |----- |----- |
| **Pitch** | Concise overview of app that convincingly explains what it offers and what problems it solves, making it sound new and exciting | Gives good idea of what the app offers, but is not persuasive or novel sounding | Hard to understand, rambling or doesn't hold together |
| **Design creativity** | Fresh ideas that distinguish app from Twitter and are well motivated by problems | Competent revision of Twitter motivated by problems but lacking novelty | Not substantively different from Twitter, or design has major flaws |
| **Concept basics** | Informative name, compelling purpose, usable OP | Reasonable name, purpose and OP, but purpose may not capture essence and OP may not be so usable | Poor name, unclear purpose or confusing OP |
| **Concept state and actions** | All the essential actions; state clearly defined and well matched to action descriptions  | Sufficient state and actions but relationship between them may be unclear | Missing actions, insufficient state, unclear description|
| **Syncs** | Succinct and clear rules that enable some novel automation or synergy | Succinct and clear rules but nothing unexpected | Rules are unclear; essential rules are missing; or concept boundaries not cleanly defined|
| **Wireframes** | Concept actions and visible state are presented clearly; executing operational principles is straightforward and intuitive; interface teaches the underlying concepts effectively | Concept actions and visible state are available in the interface; executing operational principles is possible but not completely intuitive; concepts not inferrable from interface without additional help | Some actions or state that should be visible unavailable in interface; operational principle hard to execute; misleading image of concept projected |
| **Tradeoffs** | Identify and thoughtfully address subtle issues that lack easy solution | Clear explanation of non-trivial decisions | Uninteresting issues, poorly explained decisions, or strawman options |

The qualitative judgments correspond roughly to grades of A (9/10), B (8/10), C (7/10).

## Advice

- **Pitch**. Writing a draft of the pitch won't take you very long, and will be helpful in focusing your goals and ideas. So consider doing it several times. at least early on as you're formulating your ideas, and at the end when you're done. (You should only hand-in a single version.)
- **Tradeoffs**. Considerations that you might discuss in your tradeoffs include: basic usability issues, such as improving the clarity or flow of the user interface; addressing larger social and ethical implications; introducing automation or flexibility by tightening or loosening synchronizations between concepts; finding opportunities for synergy; using familiar concepts when possible; eliminating concept redundancies by factoring out shared, unifying concepts; handling concept overloading by splitting concepts.
- **States**. Even though only an informal description of concept state is required, you should make sure that it's clear, and that the state contains sufficient information to support the actions and no more. For example, the Upvote concept needs a state component that maps user to their votes, since otherwise it can't reject upvote actions that correspond to double votes. 
- **Actions**. Here is an example of an action definition for the upvote action:
```
user u upvotes item i
// add an upvote for item i
// associate that vote with user u
// update the ranking of items to keep sorted by number of upvotes 
```

