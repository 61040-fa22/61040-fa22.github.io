---
layout: assignment
title:  "Assignment 4: Fritter review and refinement"
categories: assignments
due_date: 2022-10-10 23:59:00 -0400
date: 2022-01-03 23:59:00 -0400
---

**Deadlines**. This assignment has an unusual structure. Your review of your fellow students’ work is due **mid-week** (at 11:59pm on Thursday Oct 6), and will be forwarded to them immediately, prior to any grading. We **cannot allow** any slack days to be used for these submissions, since other students are depending on them to complete their work. The final version of your assignment is due at the usual time (at 11:59pm on Sunday Oct 9), and will then be graded as a single piece of work.

**Overview**. In this assignment, you’ll have an opportunity to refine the conceptual design that you developed in your previous assignment, based on your own review and reviews by some of your peers. This is the last step in your conceptual design of Fritter. You’ll be able to make additional modifications if you choose to, but you should expect that you will be implementing the design you settle on here.

**Purposes**. The purposes of this assignment are: (a) to give you practice in reviewing the work of others, in providing feedback, and in receiving it; (b) to solidify your grasp of conceptual design by applying principles you’ve been learning about in class; (c\) to acclimatize you to the iterative nature of software design work.

## Tasks

Each of these tasks involves a summarization, whose structure is described in the Deliverables section below. The details of where to find the designs you will be reviewing and how to submit your reviews are in the Mechanics section below.

**Peer review (DUE on Thursday)**. Conduct a review of the designs of three of your fellow students. For each one:

- **Read** through the design and check you understand it, noting any unclear aspects.
- **Apply** the design principles discussed in class (see Advice section below for a list), and note any problems you find. 
- **Summarize** your findings in a brief review, and **submit** the review.

**Self-review**. Conduct a review of your own design:

- **Apply** the same design principles, and note any problems you find.
- **Read** the peer reviews of your design.
- **Summarize** the results of your self-review, along with the peer reviews that you received.

**Design modification**. Modify your design in response to the peer reviews and self-review:

- **Decide** for each review observation what change (if any) you want to make to your design in response.
- **Summarize** your changes to the design.
- **Make the changes** to a copy of the original design.

## Deliverables

**Peer reviews**. Each of your peer reviews should consist of some bulleted lists of observations: **compliments** about good qualities;
**criticisms** about problems that you found; and, optionally, **speculations** about how the design might be improved. Each observation should (a) **point** clearly to the relevant part of the design; (b) **explain** succinctly what the observation is; (c\) **reference** the appropriate design principle. (Observations about lack of clarity need not reference a design principle.)

**Self-review**. Your self-review should follow the same structure as your peer reviews; feel free to include self-compliments too! Include, following your own observations, those that you received from your peers, modifying them (if need be) to eliminate repetitions and improve clarity.

**Modifications**. Your design modifications should consist of a bulleted list of changes. For each change, give a very brief overview of the change, and its justification (by reference to the review observations). Add to each of the critical observations in your self-review an annotation (eg, as a final sentence in italics) either noting that the criticism has been addressed by a change, or a reason not to address it (which might be that you just regard it as not sufficiently important, or too burdensome to address).

**Mechanics**.
- **Who am I reviewing?** For links to the designs you are reviewing, see the [spreadsheet](https://docs.google.com/spreadsheets/d/1M12151UPE0FXmE-73IvsRLQsytmWpRjko4MZj05DmDE/edit#gid=0).
- **How do I submit reviews?** Just add each peer review as a separate post in your portfolio.
- **How do I see reviews of my design?** The same spreadsheet has a tab that shows reviewers for each reviewee, so you just look the review up there sometime after the reviewing deadline.
- **How do I submit the rest of my work?** Add a single document to your portfolio that includes your **review summary** (comprising your self-review and your summary of the peer reviews of your design), your list of **design modifications** and your **updated design**. Submit the URL to this document using [this form](https://forms.gle/KhBzoARBuA4dwxTv5).

## Rubric

| *Part* | Excellent | Satisfactory | Poor
| ----- | ----- |----- |----- |
| **Exposing flaws** | Peer reviews exposed multiple flaws that would adversely affect user experience | Peer reviews exposed at least one flaw that would adversely affect user experience | Peer reviews did not expose any flaws that would impact a user |
| **Balance** | Each peer review includes a valid compliment, criticism and speculation | Each peer review includes a valid criticism | One or more peer reviews lacks any criticism |
| **Principles** | Your peer reviews and self-review together demonstrate ability to apply a variety of concept design principles in a focused and effective way | Your peer reviews and self-review together demonstrate familiarity with a variety of concept design principles but their application is not yet strong | Little evidence of understanding of concept design principles |
| **Modifications** | Design modifications are clearly tied to review observations and will improve user experience | Modifications to design are clearly tied to review observations, but may not improve user experience | Modifications to design are not clearly tied to review observations |

The qualitative judgments correspond roughly to grades of A (9/10), B (8/10), C (7/10).

## Advice

**Review style and tone**. Your observations should be as succinct and to the point as possible, but still in full sentences. About half a page of writing (a few hundred words) should more than suffice for each review. The tone of your peer reviews should be candid and straightforward, but also helpful and generous. Some people find it helpful to prefix compliments comments with “I like,” criticisms with “I wish,” and speculations with “I wonder.”

**Scope**. Focus on quality rather than quantity in your reviews. Three thoughtful observations well grounded in design principles are sufficient for a review, but if you have more good observations to make, do include them! Place your strongest observations first, to draw attention to them. 

**Time**. We expect you to spend 30-60 minutes in total on each of your reviews, including the review of your own design, and to spend an hour or so modifying your design. So this is likely to be a lighter assignment for most students than previous ones (and an opportunity for those who have not assimilated the class material on concept design to look over it again).

**Concept design principles**. Here are some examples of the principles and rules of thumb that we’ve talked about in lecture and that you might apply in your heuristic evaluation: 

- **Concept specificity** (Simplicity lecture). Looking at the application overall, concepts and purposes should be in one-to-one correspondence, with no **redundancy** (in which two concepts have the same or very similar purposes) and no **overloading** (in which a concept attempts to fulfill two different purposes).
- **Concept synchronization** (Automation lecture). Looking at the application overall, concepts should be synchronized tightly enough to ensure consistency and to provide needed automation, but loosely enough to give users the flexibility they need.
- **Concept independence** (Modularity and automation lectures). Each concept should be defined independently of any other concept, so that concepts can be understood separately and reused in other applications. No concept should rely on another concept. Concepts should, as much as possible, treat their target objects as generic types; for example, a Freet concept should ideally be independent of the type of freet contents (eg, whether plain text, markdown, RTF, or whatever).
- **Concept efficacy**. Each concept should have a readily understandable purpose, and an operational principle that convincingly and straightforwardly fulfills it. The concept’s actions should be sufficient to handle likely use cases, and its state should be rich enough to provide users with adequate feedback.
- **Concept simplicity** (Simplicity lecture). Each concept’s operational principle should be simple for the user to execute without needless cost or complexity. Looking at the application overall, a concept should not be included if it adds to the user’s burden without providing corresponding benefit.

If you’re unsure about some of the design principles, you might want to return to the lecture videos and associated material (linked from the [schedule](https://61040-fa22.github.io/schedule)). You can also find longer explanations in the [recommended text](https://61040-fa22.github.io/4-reading-group.html).

**Scenarios**. In applying the design principles, it may help to start by inventing some scenarios of usage, and checking that they result in the expected behavior. Including a concrete scenario is a great way to make a criticism clear. 

## Sample Observations

Here are some sample observations, based on examples discussed in class, to give you a sense of the form and length that is appropriate.

- **A compliment, about Apple’s Finder**. I like how the synchronization of the *Folder* and *Trash* concepts brings a synergy, reducing the complexity of the interface. For example, the trash folder does not need a special *date deleted* column since the regular *date added* column can play this role.  (Concept synchronization)

- **A criticism, about Fujifilm cameras**. I wish the  *ImageSize* concept were not overloaded to handle aspect ratios too. This means that a custom aspect ratio can only be set when JPEG files are being generated, even though non-destructive crops already appear in raw files. (Concept specificity)

- **A speculation, about Discourse**. I wonder if the *ExternalLink* concept might be extended to include not only link text and a URL but also a preview of the linked text (as Wikipedia does for internal links). This may make it easier to read posts that point to external pages. (Concept efficacy)
