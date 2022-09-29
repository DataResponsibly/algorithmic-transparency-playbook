---
title: FAQ on algorithmic transparency
---

# Commonly asked questions about algorithmic transparency

By the time you finish this course, you should have a deep understanding of algorithmic transparency. But to begin, consider the following commonly asked question about algorithmic transparency:

<br>

## Why should one care about transparency?

There are many reasons why algorithmic transparency is important. We will cover many reasons throughout this playbook, but here are three: first, transparency can help build trust in your algorithmic systems among managers, engineers, and those individuals impacted by the system. Second, transparency is one part of preventing accidental or misuse risks, like creating unfair algorithmic systems that are biased against minorities. Third, implementing transparency may be necessary for compliance as governments around the world (especially in the US and the EU) draft and sign legislation regulating the transparency of algorithmic systems.

<br>

## Who is transparency for?

Transparency impacts many stakeholders both internally and externally of an organization. We have already mentioned a few thus far, like \textbf{building trust among managers.} Another important stakeholder is an individual affected by the outcome of an algorithmic system. For example, if an individual is deciding whether or not to apply for a job, it is advisable to make them aware that they will be assessed by an algorithmic system and what criteria will be used for assessment.

Other stakeholders may also include the public and public administration, like policymakers. Later in this playbook we give a complete list of potential stakeholders of transparency.

<br>

## Is it easy to implement transparency?

The short answer is yes. It is trivial to add basic transparency features for algorithmic decision-making systems. For example, a first step could be as simple as telling people about your algorithmic decision-making, and telling them what factors it considers.

The long answer is that, while it can be easy to create basic transparency features, one should be thoughtful about _how_ they implement these features and _what_ these features are. This is discussed in detail throughout the course, inclduing content for both technical and non-technical audiences. 

<br>

## I've heard of "black-box" algorithms. Can they be made transparent?

Yes. In recent years, researchers and practitioners have made significant developments in "opening up" complex, opaque systems called **black-boxes** There are many powerful, free, and easy-to-use tools that can be used to gain insight into how underlying black-box algorithms work. The most popular tool is called SHapley Additive exPlanations (SHAP).

This topic will be unpcaked extensively later in this course.

> **Black-box** is a blanket term used to describe __any system__ in which a human cannot see the inner workings of the algorithm.

<br>

# Does implementing transparency mean sacrificing efficiency or accuracy?

Not necessarily.

Many managers are concerned that implementing transparency means reducing the sophistication of their algorithmic systems, thereby decreasing their efficiency and accuracy. However, recent developments in the field have challenged this idea. First, as described previously, there are a number of transparency tools that can be used to "open up" even the most complex, sophisticated black-box systems. Second, there is a growing number of case studies showing that under many conditions, simpler, more transparent algorithmic systems can perform the same (or even better than) complex systems. Overall, implementing transparency does not necessarily result in sacrificing efficiency–it’s not that simple!