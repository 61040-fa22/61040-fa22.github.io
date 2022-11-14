---
layout: assignment
title:  "Project Converge"
categories: assignments
due_date: 2022-11-20 23:59:00 -0400
date: 2022-01-10 23:59:00 -0400
---

**Overview**. This final project phase, like the previous one, involves activities that you already conducted in your individual assignments. It combines the VSD analysis from your very first assignment with the convergent design work you did later.

**Timing**. You will receive reviews from the staff by midnight on Monday, which should allow you to incorporate this feedback in your design selection. You will receive your peer reviews by midnight on Wednesday, which you can then incorporate in your detailed design work. The full design is due at midnight on Sunday. 

## Tasks

1. **Select a design**. Reflect on the options that you created during the divergent design phase, and the feedback you received in reviews, and finalize your choice of problem and solution, selecting elements (in whole or part) from your previous divergent proposals.

2. **Finalized project pitch**. Summarize your decision by writing a project pitch that summarizes the problem your app solves; outlines the concepts that your design uses; and explains how they work together to address the problem. We expect this to be around half a page of text. It should not include any detailed concept descriptions.

3. **Conceptual design**. Design the concepts of your app, and specify each of them in the standard form (name, purpose, operational principle, states and actions). The state should be defined using a textual relational data model. Specify any synchronizations between concepts; these need not include synchronizations that simply propagate creations and deletions. Write an application  definition as a list of concepts, with generic types instantiated appropriately. Take notes as you work on your design as input for your design tradeoff discussion, and incorporate the feedback you received in your reviews from staff and peers.

4. **Wireframes**. Create a collection of Figma wireframes that cover the essential views and interactions that a user would experience in using your app. Include a link to your live Figma models, and also some embedded screenshots (focusing on your most interesting concepts) with informative captions explaining them.

5. **VSD analysis**. Pick at least two [prompts](https://canvas.mit.edu/courses/16626/files/2668131?wrap=1) from the _Stakeholders_ dimension, and one prompt each from _Time_ and _Pervasiveness_, and apply them to your design, writing a paragraph for each prompt about aspects of the design that are relevant and how you’ve addressed them (or if not, what concerns remain).

6. **Tradeoffs**. Using the notes that you took during your design process, pick at least 3 design decisions that you made in which you had to choose between multiple options. For each one, provide (a) a pithy title naming the issue; (b) an outline of what the various options were; (c\) a rationale for why you chose one option over the others. We expect this to take about a page or two of text and sketches.

7. **Project plan**. Use the [project overview timeline](https://61040-fa22.github.io/assignments/assignment-p0-overview.html) to create a week-by-week plan of work. This plan should include three elements:
    * The functionality you plan to have completed for the three milestones. For the alpha release, we expect very minimal functionality akin to the A5/A6 milestones — sufficient to check that your development process is working, and that you are able to integrate work from all team members. For the beta release, you should be able to demonstrate that the core concepts of your app are ready for use by multiple users (but things do not need to be feature-complete nor fully polished). For the final build, we expect all features of your design to be fully implemented, polished, and deployed for the world to use. 
    * A list of implementation tasks to be completed, broken down into manageable chunks and assigned to a team member with a corresponding deadline. We expect roughly 10-20 such tasks. 
    * A brief paragraph explaining what you will do if something goes wrong. Your description should include some substantive ideas, such as particular tasks that may need to be dropped or functionality that will fall out of scope. 

<!-- Agendas for team mentoring meetings.-->

## Deliverables

Post your work to a Jekyll portfolio. You may choose to either designate a single person's site as your group's main portfolio, replicate the content across each group member's portfolio, or setup a separate Jekyll static site for your team. Whatever you choose, your project work accessible via a link from all of your personal portfolios.

Once your material has been posted, submit [this Google form](https://docs.google.com/forms/d/e/1FAIpQLSdfyJBcskVdzJDY9NrwMyIf_fE3q8-Skcd5I_RubUDILHXyyw/viewform?usp=sf_link) to finalize your submission, including a publicly-accessible URL to your submission, a Git commit hash, and other information.

## Rubric

| *Part* | Excellent | Satisfactory | Poor
| ----- | ----- |----- |----- |
| **Pitch** | Concise overview of app that convincingly explains what it offers and what problems it solves, making it sound new and exciting | Gives good idea of what the app offers, but is not persuasive or novel sounding | Hard to understand, rambling or doesn't hold together |
| **Design creativity** | Fresh ideas that distinguish app from existing apps and are well motivated by problems | Competent revision of existing apps motivated by problems but lacking novelty | Not substantively different from existing apps, or design has major flaws |
|**Concept design basics** | Informative name, compelling purpose, usable OP; defines all the essential actions; succinct and clear synchronization rules that enable some novel automation or synergy; concept list instantiates generics correctly | Reasonable name, purpose and OP, but purpose may not capture essence and OP may not be so usable; succinct and clear synchronization rules but no automation or synergies; concept list is complete but straightforward opportunities for making concepts generic and instantiating them have not been taken | Poor name, unclear purpose or confusing OP; missing actions; synchronization rules are unclear; essential rules are missing; or concept boundaries not cleanly defined; concept list is missing or wrong |
| **Concept behavior and data models** | State defined in data models is sufficient to support actions; data models are abstract and expressed using sets and relations rather than programming language types; no unnecessary components included; component names well chosen | State is sufficient to support actions; data models are mostly abstract and expressed using sets and relations, but may have a few flaws such as unnecessary components or poorly chosen names | Data model is unclear or not relational; state is insufficient to support actions |
| **Wireframes** | Concept actions and visible state are presented clearly; executing operational principles is straightforward and intuitive; interface teaches the underlying concepts effectively | Concept actions and visible state are available in the interface; executing operational principles is possible but not completely intuitive; concepts not inferrable from interface without additional help | Some actions or state that should be visible unavailable in interface; operational principle hard to execute; misleading image of concept projected |
| **VSD Analysis** | A crisp and thoughtful analysis of how your app affects a diverse range of stakeholders, highlighting tradeoffs, tensions, and issues that may arise as users engage over different time scales and due to widespread use. | A good analysis of your app's impact on diverse stakeholders, across different time scales, and through widespread use. However, additional research or reading around the subject would help push the analysis further by uncovering design tradeoffs or tensions. | A shallow analysis that considers only a narrow range of well-understood stakeholders or only a cursory not to broader stakeholder impacts. Provides only a brief, insufficient treatment of the implications of different timescales or wirespread adoption. |
| **Tradeoffs** | Identifies and thoughtfully addresses subtle issues that lack easy solution | Clear explanation of non-trivial decisions | Uninteresting issues, poorly explained decisions, or strawman options |

The qualitative judgments correspond roughly to grades of A (9/10), B (8/10), C (7/10).

## Advice

**Data models**. Some of you had trouble expressing state using relational data models, so we have written a short [document](/pages/data-modeling.html) to guide you. You may also want to review the [slides and video](/lectures/lecture-8.html) for the lecture that explained relational data models.