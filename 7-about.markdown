---
layout: page
title: Class Guide
permalink: /about/
---

# A Guide to Software Studio
This guide tells you the main things you need to know about the class and how it runs.

## Admin details

**Prereqs and credits.** 6.1040 is a 15-unit junior/senior level class, and offers AUS2, DLAB2, and II credit. You can use this class to provide all of these credits at once. Prerequisites are 6.1020 Elements of Software Construction (6.031) and 6.1200[J] Mathematics for Computer Science (6.042). From 6.1020, we rely on the ability to think about a program in an abstract and code-independent way (using notions such as specifications, interfaces, representation independence, abstraction functions and invariants), and on some practical skills (knowledge of JavaScript; basic familiarity with Node/Express; programming maturity, notably the ability to deal with sometimes messy and under-documented frameworks). If you have these skills from internships or other classes, you should be fine. From 6.1200, we rely on students being familiar with basic notions of logic (especially nested quantifiers) and sets and relations (join, closure, reachability, relation properties, etc.). We don't enforce the prerequisites strictly but students are warned that without the background they provide, this class can be extremely challenging.

**Lectures**. There are two 80-minute lectures each week, from 2:35pm to 3:55pm on Mondays and Wednesdays in room 1-190. Lectures will focus on fundamental ideas and skills. During each lecture, there will be short exercises and class discussions to help you solidify your understanding. Video recordings will be available (typically a day after the lecture) for students who wish to review the lecture or were unable to attend. Regular in-person lecture attendance is mandatory. 

**Recitations**. There is one 50-minute recitation each week. Recitations are taught by teaching assistants; each will be centered on a particular technology. Recitations are optional, and you can choose which one to attend.

**Studio hours.** The TAs will be available for consultation during open hours each week at times that will be posted on the Canvas site’s main page. These are likely to change in response to student demand, so be sure to check when you make your plans for the week. Studio hours are intended to provide a place where several students and TAs will be working so that you can get help as you need it. Studio hours will be phased out when the team project begins; after that, TA meetings will be made by appointment.

**Individual assignments.** In the first half of the term, students will work on individual assignments. There are six assignments, of which four are focused on design and two on implementation. 

**Team project.** The second half of the term is spent on a team project. Teams will generally have four members; you will be able to choose your teammates. You will also be able to choose what to build. We expect you to build _authentic apps_ that bring real value to real users, ideally serving communities beyond the student community at MIT. It’s never too early to start brainstorming!

**Design reading group**. A new book, [*The Essence of Software*](https://essenceofsoftware.com/), on which much of the class material is based, is a *recommended* but not required text. For students interested in delving more deeply into the ideas of the class, Daniel Jackson will host an optional weekly discussion group about software design based on assigned readings mostly from the book. Pizza will be served.

**Listeners**. Listeners for the class are welcome and will have access to all the materials. Listeners cannot join project teams or submit work for grading.

## What the class is about
This class is about _design_. You’ll learn how to design software that is  fit for purpose: that fulfills the needs of users, and is flexible, powerful and easy to use. 

Design happens at the meeting point of technology and people. It’s not just about the user interface, though; much of the class is about how to shape the underlying functionality that the user experiences.

The design material taught in the class includes classic material on user interface design (such as heuristic evaluation) and data modeling, and also cutting-edge material on shaping functionality (Concept Design) and ethics (Value Sensitive Design).

This class is not about technology, and we’ll assume you’re proficient in TypeScript, that you have a basic familiarity with HTML/CSS, and that you’ve done some programming in Node.js. The prerequisite class (6.031) teaches all these things and has helpful [notes]() for review.

Nevertheless, you will learn some new tools and technologies so that you have all the tools you need to be a proficient web stack developer. These include: GitHub for maintaining a repository and GitHub Pages for hosting a static website; Jekyll, a static website builder; Heroku, for deploying Node.js; Figma, for wireframing; SQL, for persistent storage; and Vue, a frontend reactive framework.

## Does the class meet industry standards?

Students sometimes ask if the design approach that we teach in the class is the standard approach used in industry. Of course it isn’t! If it was, you could learn it on the job and you wouldn’t need an MIT degree. Or to put it another way: the role of education is to shape the future (including yours!), not consolidate the present.

The class will indeed teach you several of the most effective techniques currently used in industry (needfinding, brainstorming, sketching, wireframing, heuristic evaluation of UIs, user testing) but it would be a pretty poor class if that was all. We teach [concept design](https://essenceofsoftware.com) and [value sensitive design](https://vsdesign.org) to empower you to a better designer than you could ever be just by learning on the job, or by taking a UX bootcamp.

MIT classes have a long tradition of teaching new approaches coming out of research that are adopted in industry sometimes only decades later. One of your lecturers was a TA for the original 6.170 class, in which the programming language was CLU, one of the first object-oriented languages (invented by Barbara Liskov, for which, amongst other things, she won the Turing Award). At the time, very few programmers knew about objects, and it wasn’t until decades later that languages started to have the features CLU had back then. Even when Java came along, its design had flaws (such as a distinction between "primitive" and "object" types) that CLU had eliminated twenty years before!

That lecturer also taught sections in 6.001 when the textbook was *Structure and Interpretation of Computer Programs*. Some students complained that the class was taught in Scheme, a functional language that nobody used, and not a sensible language like C. It’s amazing to think that Scheme is now about 50 years old (and LISP is even older), and only in the last few years have functional languages become the ones that all cool programmers want to know and use.

There's another take on this. While most people in industry haven't learned concept design or value sensitive design, the very best have been using ideas like these for a long time. Concept design in particular emerged from a detailed study of hundreds of apps, extracting the lessons for what makes some apps so good and others so bad. Both of these approaches are attempts to codify and make explicit best practices which people in industry may come to only after many years of learning by trial and error.

## A learning community

Our goal is for this class to for you to acquire skills, insights and sensibilities that will serve you well for your entire life. Knowing how to build a web app may help you get a summer job, but remember that’s not why you’re taking this class.

To make the class as effective as possible, we want it to be a _learning community_. We have explicitly designed the class such that you do not feel you are in competition with one another. Great design in a very social activity: it occurs when you're inspired by someone else's work, remix it into your own, or when someone else offers a generous and constructive critique of your work to help push it further. 

A healthy learning community is also centered on _trust_. We, the staff, will treat you, the students, as grownups. We won’t play tricks to get you to come to class, penalize you for small mistakes, or assign work just for the sake of it. Everything we ask you to do will be for your benefit and the benefit of your peers.

In line with this approach, we’re experimenting with a new idea. Instead of grading class participation, we’ll assign a portion of your grade to activities that you can engage in to actively support your peers and improve their work. More on that below.

## Attendance

Recitations are optional, but lecture attendance is required. We don’t track you, but we expect you to commit to attending lectures. Of course things come up, so we’ll understand if you miss a few. 

Why do we insist on this? First, we’ve found that students who attend lecture do better: they learn more, they’re happier, and they get better grades. Second, when students don’t attend lectures they often become a burden to the staff because, when the assignment comes and they discover they are unprepared, they try to learn the lecture ideas in TA office hours and by asking questions online. 

We put a lot of work into making lectures engaging and educational, and we don’t believe that watching a video is a substitute for being there in person, joining your peers on class activities and participating in discussions. If you have suggestions for how to improve lectures, we will of course be glad to receive them.

## Collaboration
Design is all about collaboration, so we encourage it in all aspects of the class. You can talk with anyone about anything; you can share ideas; and you can use other people’s ideas in your own submissions with appropriate credit. The only constraint is that you must write up your work by yourself (this ensures that you really understand it!) and note the set of people you collaborated with.

To help you find partners to collaborate with, you can use the MIT [psetpartners app](https://psetpartners.mit.edu).

The class will run on an honor code. We will assume that you are not cheating by copying text or code from other students in the class  or from work submitted in previous terms. If we discover that you have violated the honor code, you may fail the class and have a complaint deposited with the Committee on Discipline.

You are free to use any third-party code, whether as libraries or code fragments, and to adopt any idea you find online or in a book, so long as it is publicly available and appropriately cited (see the [section on code](http://integrity.mit.edu/handbook/writing-code) in the MIT [handbook](https://integrity.mit.edu) on academic integrity for details). 

## Class contributions
10% of your grade will be allotted to constructive contributions that you make that benefit each other and the class as a whole.

We’ll recognize these kinds of contributions:

- **Blog posts** (2%). Write a short blog post (of 200-500 words) about an idea or example that was presented in class. Your post must appear by midnight on the same day as the class, so it can be used by other students reviewing the class material. You’ll publish it on your portfolio website, and will post a link to the post on the class forum. Any medium is acceptable; in place of text, you could produce a sketchnote, draw a comic strip, make a TikTok video, write a poem, etc. Work that isn't word-based should be of equivalent effort to a 200-500 word blog post.
- **Share a design idea** (2%). Share a design idea you're working on in the class forum. Your forum post should include a short written summary of the ideas, as well as anything else that can help others understand what you're working on (e.g., an annotated screenshot, or quick screen recording). You might also choose to include specific prompts to help guide the critique — i.e., what specific things would you like feedback on?
- **Review a design idea** (2%). Offer a review of another student’s design idea and share it in the class forum. Ideally, your review follows the [I like / I wish / What if](https://public-media.interaction-design.org/pdf/I-Like-I-Wish-What-If.pdf) format and offers both generous and constructive, actionable feedback. 
- **Answer a design question** (0.5%). You write a substantive answer to a question on a design topic asked by a student in the forum, or provide help with a collection of short answers in a longer thread.
- **Answer a programming question** (0.25%). You help another student by answering a programming question, perhaps by debugging a short code sample, or explaining how to use an API function.

It’s up to you which of these you do, but note that the number of points for each contribution kind differs (because some involve more work than others). For example, you could get the full 10% from 2 blog posts (4%), one design idea (2%), one review (2%), two answers to design questions (1%) and four answers to programming questions (1%).

It’s your responsibility to list your contributions in your portfolio so the staff can track them easily. These contributions will not be graded, but we may ask you to edit or expand.

## Student design portfolios
All of your individual work for the term will be recorded in a static website that will act both as a design notebook and (when completed) as a portfolio of your work.

**Technology.** Your website will be implemented with [Jekyll](https://jekyllrb.com) and hosted on [Github Pages](https://pages.github.com). An advantage of using a static website generator like Jekyll is that you can use a predesigned theme, and write your content in markdown so no knowledge of HTML and CSS is needed. But you will also be free to design your own visual appearance if you want to (by editing the HTML of the layout files and the CSS rules).

**Submission of work**. No explicit submission process is needed for your assignments. You’ll provide the URL of your website early on, and your TAs will revisit the same URL to look at each piece of work. Comments and grades will be available on the class’s Canvas site. 

**Organization.** This is a design class, so we won’t specify how you organize or structure your site — that’s up to you! If your TA finds it hard to locate your work, you can expect your grade to be affected. One structural recommendation: if you choose to represent a large piece of work (for example, a whole assignment) as a single page, make sure that the sections have distinct URLs.

**Versioning.** Obviously, we want you to feel free to make changes to your website, to correct errors, add new ideas, respond to reviews, and so on. But it would wreak havoc if you were to edit a page your TA is grading. So we require that once a piece of work is submitted, it not be modified **ever** again. To make a change to a piece of work, you should first make a copy, and then provide links on your site to both the old and new versions. 

Modifying a page after submission is a violation of our honor code and will be taken very seriously.

## Grading and lateness policy

Your grade is allocated as follows:

- **Individual work**: 60%, comprising of six assignments worth 10% each. Some of the assignments stretch over two weeks, and have deliverables at the end of each week, but a two-week assignment is worth the same as a one-week assignment.
- **Team project**: 30%. Except in unusual circumstances, all members of the team will receive the same grade.
- **Community contributions**: 10%. 

Each student has 5 slack days to be used as you choose, with the following restrictions: slack days may not be used on the team project, nor for the submission of the design review (which is part of the Design Refinement assignment). You are responsible for requesting **before** an assignment’s deadline however many slack days you plan to use for it. Use [this form](https://forms.gle/CHheiJq4XhA88rjWA) to request slack days.

Once your slack days have run out, a late submission will cost 10% per day. So if you submit an assignment three days late that would have been worth 95% had you submitted it on time, you will receive 65% instead.

You should plan to use your slack days to deal with scheduling issues that you anticipate, such as interviews, conference trips or special family occasions.

In the case of emergencies or illness, we will obviously grant extensions. **It is your responsibility to obtain a letter from an [Student Support Services](https://studentlife.mit.edu/s3) (S3) dean that specifies explicitly how many days extension they believe you should be granted.**

Sadly, some students find that even with extensions they are unable to make adequate progress. If, just prior to the team project, your class grade is not a C or better, you will not be able to join a team project team. Instead, you will be able to use the rest of the term to complete the individual assignments, which must be handed in one week before the end of term. Your final grade will be one letter grade lower than what it would have been if all your assignments had been submitted on time.

## Advice

Some general advice:

- **Get started early**. We know that 6.1040 isn't your only obligation. You’re busy and have to juggle many other classes and other responsibilities. But don't underestimate the time 6.1040 assignments will take — they can look deceptively straightforward. don’t wait until the day an assignment is due to start thinking about it. That has will (a) make you stressed, (b) give you fewer chances to get help, and (c) lose the advantage of mulling a problem over in the back of your mind. So try and get started early on, and figure out what you’ll need to do, and what help you might need.
- **Ask for help**. Don’t be shy to ask the staff for help in office hours, or to post questions on the class forum. In our experience, students who ask for help get better grades.

## Getting Help

Do make good use of all the resources the class offers. We're here to help you!

- For **administrative questions** (eg, regarding due dates or interpreting assignment instructions); for **technical questions** about programming or the various platforms; for **questions about ideas** taught in lecture; for **larger questions** about design whether or not directly related to lecture content; for **questions and feedback about the pedagogy** of the class: post publicly in the appropriate category in the class forum.
- For help when you're **feeling confused** on a design or programming issue, and can't formulate a question, or would like advice on your design or code: go to TA lab hours. Please do not email the TAs individually to ask for help.
- For a **personal issue** about grading, attendance, or team issues: send an email to the staff mailing list, 61040-staff@mit.edu.
- For a personal problem or for **friendly life advice**: email a lecturer. We’d be delighted to chat with you.

Students are sometimes wary of posting basic questions on Piazza, but bear in mind:

- If you have a question or are confused about something, other students almost certainly are too, and you will be doing them a service by articulating a question.
- Learning how to be straightforward about what you don’t understand, and where you need help, is an important professional skill. People who confidently ask for help are better team members than those who struggle silently.

## Life at MIT

Life at MIT is intense, fast-paced and exciting. But it can also be exhausting, and almost all students have times when they feel demoralized or frustrated. And a campus can be a lonely place even when you’re surrounded by others.

MIT is committed to helping students deal with the pressures and challenges of student life. A good place to start is [ask.mit.edu](https://ask.mit.edu), which has pointers to many useful resources. If you are dealing with a personal or medical issue that is impacting your ability to attend class, complete work, or take an exam, you should contact a dean in [Student Support Services](https://studentlife.mit.edu/s3) (S3). S3 is here to help you. 

The staff of this class is deeply committed to making your experience this term one that will not only give you valuable skills and insights, but will also bring you confidence and joy in your work. We hope that if the class does not live up to our aspirations of supporting you effectively in any way, you will let us know. The lecturers are also keen to engage with students individually, so be in touch if we can help.


