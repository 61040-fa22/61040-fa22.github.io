---
layout: assignment
title:  "Project Beta"
categories: assignments
due_date: 2022-12-04 23:59:00 -0400
date: 2022-01-12 23:59:00 -0400
---

*Due 11:59pm, Sun Dec 4 and 11:59pm Tue Dec 6*

**Overview**. The beta release of your final project should be a working implementation that realizes the bulk of the design (i.e., all core/novel concepts) that you developed in the converge phase, and includes necessary styling and layout to achieve a usable experience. You will likely have made some changes to your envisioned design during the implementation, perhaps finding holes or flaws in your ideas, or discovering opportunities for streamlining or simplifying them. As you write code and make changes to the design, you should track all changes carefully, so that you can summarize them in your revised design. When you have completed your implementation, you will conduct some user testing to find ways in which your app might be further improved (at all levels, physical, linguistic and conceptual). You will address these improvements in the next and final phase of your project.

## Tasks

**Working and deployed implementation.** Implement the functionality of your design, apply necessary styling, and deploy it to a publicly accessible URL. Your code, committed to your team's repository, should be appropriately formatted and commented; although code quality will not be an explicit part of your grade, the code must be easily understandable so that TAs, in grading your project's functionality, can easily map observed behaviors in the deployed app to the underlying code. Your implementation should also reflect aesthetic decisions your team has made to produce a pleasant, intuitive, and usable user experience. 

**Design revision.** List the changes you have made to the design you had envisioned in the previous "Converge" phase. For each change, provide a brief (~3 sentence) rationale for making it. 

**User testing.** Once you have completed your implementation, conduct a simple one-hour user study as follows:

1. **Prepopulate data.** Ensure that your app is populated with appropriate data for your domain (i.e., no Lorem Ipsum, Alyssa P. Hackers, or other dummy text), so that your user will get a realistic impression.

2. **List tasks.** Create a list of tasks that cover the key concepts of your app, where a task should typically involve executing a sequence of user interaction steps. You should include at least five tasks, from simple one-action tasks to more complex multi-action tasks, that will test how easily the user can cross the gulfs of execution and evaluation discussed in lecture. Format your task list as a table, putting the tasks in an appropriate order so that any application state required by subsequent tasks has been correctly setup by earlier tasks. Give each task (1) a short title; (2) a succinct goal (in words that can be given to the user); and (3) a rationale for inclusion (a sentence explaining why this is a task worth testing, namely what  you hope to learn or uncover about your design when testing this task with a user versus executing it yourselves via a cognitive walkthrough).

3. **Find a tester.** Now find a friend or fellow student to be your test subject, and obtain their consent for participating in your test. Prep them by explaining their role (and how you'll use the test results) and the general purpose of your app.

4. **Execute the test.** Sit your tester down in front of the app and ask them to attempt to perform the tasks in turn while thinking out loud. If they fall silent, prompt them to keep thinking out loud. If they get stuck, you may intervene but give them a chance to get unstuck first. Try to say as little as possible, and avoid explaining the user interface to them.

5. **Observe their usage.** Throughout the study, watch what your test subject is doing, saying, and even feeling (e.g., watch for facial expressions, sighing, etc. which often signal frustration or other emotions). Take careful notes throughout. You might also consider capturing a screen recording, as well as audio/video of your participant (all with their consent, of course) for further analysis after the session is complete. 

6. **Reflect and debrief.** After your participant has completed the tasks, spend 10-15 minutes interviewing them to capture any overall thoughts or impressions they have about your application. What did they think worked well versus could be improved? If you noticed them hesitate, get confused or stuck on certain screens, now is your chance to dig into that more—what did they find confusing, what were they hoping to do, how did they figure things out?

7. **Summarize the test results.** Turn the notes that you took into a list of observations about the app, each of which either identifies a flaw or suggests an opportunity for improvement. Classify each observation by level (physical, linguistic, conceptual) and a degree of severity (minor, moderate, major, critical). For instance, minor issues introduce some friction to the experience that, while annoying, a participant can recover from and move on; critical issues, however, bottleneck participants so severely that they required your intervention to make further progress. Moderate and major issues fall along that spectrum.

## Deliverables

Create two separate documents, as follows: (1) for the revised design and (2) for the user testing tasks and results. Include these documents in your portfolios.

Your working implementation and design revisions document will be due 11:59pm on Sunday, Dec 4. Your user testing document will be due 11:59pm on Tuesday, Dec 6. 

Submit these deliverables using [this form](https://docs.google.com/forms/d/e/1FAIpQLSdfyJBcskVdzJDY9NrwMyIf_fE3q8-Skcd5I_RubUDILHXyyw/viewform?usp=sf_link) once for your whole team by the appropriate deadline. The form will ask you to include links to your working deployment and the Git repo you are deploying from, and to one of your portfolios for the design and testing documents.

## Rubric

| *Component* | Excellent | Satisfactory | Poor
| ----- | ----- |----- |----- |
| **Functional Completeness** | Functionality includes and goes beyond core concepts (i.e., nearly feature complete) | All functionality covering core concepts of the app is implemented | Some functionality related to app’s core concepts is missing |
| **Robustness** | App operates smoothly. Where appropriate, client-side or backend validation anticipate malformed or erroneous input, or access violations, and show or return informative error messages | App usually operates smoothly, but some missed opportunities for client-side or backend validation to handle erroneous input. User-friendliness of error messages could be improved. | App suffers from non-trivial robustness issues when malformed or erroneous data is input. Error messages are missing or opaque. |
| **User interface design** | User interface gives a pleasant and intuitive user experience| User interface gives an intuitive user experience, but occasional rough edges undermine cohesion | User interface is only minimally designed, and fails to provide a usable experience |
| **Design revision** | Design revision is clear and comprehensible, and rationales for changes are succinct and well argued | Design revision is clear and comprehensible but rationales for changes need more explanation or are too wordy | Design revision is unclear and rationales are hard to follow | 
| **Populated data** | Deployed app is populated with plausible data that gives a good impression of realistic use | Deployed app is populated with plausible data but of insufficient quality or volume to give a good impression of realistic use | Deployed app is populated with insufficient or implausible data that makes it look like a toy |
| **Task list** | Task list covers a broad range of functionality and complexity. Goals are well-justified, succinctly but compellingly describing how insights might differ from cognitive walkthroughs | Task list covers much of the functionality across a nice range of complexity, but some aspects are still lacking. Goals begin to offer some initial rationale but could go further in hypothesizing insights  | Task list misses important functionality, or does not span a range of complexities. Goals do not justify why it is necessary for a _user_ to be testing this task.|
| **Observations** | User testing revealed several substantive insights that are well summarized | User testing revealed at least a few substantive insights that are reasonably summarized | User testing revealed little of value, or summary is hard to follow |


## Advice

**Scoping and polish.** For this milestone, we are expecting you to have sufficiently implemented the core concepts of your design—i.e., the functionality that distinguishes your app from others that may exist—and styled them to produce a usable experience ready for user testing. While you are welcome to also begin working on polishing your interface and interaction design, note that your user testing is likely to turn up flaws that you will want to fix as part of the final build.

**Build rapport.** Like the interviews you constructed in A1, we recommend building rapport with your test subject so that they feel comfortable thinking out loud and making mistakes in front of you. Emphasize that you are testing your application, not the participant—their performance (including when they get stuck, confused, etc.) does not reflect poorly on them.

**Prompting thinking aloud.** Thinking out loud will feel very strange to most participants, and they will be prone to fall silent. When they do, prompt them to keep talking. Remind them to tell you what they are thinking, what they are trying to do, what questions come up when they try to do a task, and even reading out the things they see on the screen (which can be an important signal of the order in which participants read things on screen, including whether they miss certain things!.

**Pre-decide where to help.** You are going to be very tempted to jump in to help the participant every time they get stuck—resist that temptation. Instead, come up with a pre-determined set of criteria for when you will intervene, and try to stick to that. Of course, if participants are completely unable to make progress, that is a good time to intervene.