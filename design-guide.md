---
layout: page
---

## Principles for Making Transparent Algorithmic Systems

### Make Explanations About a Decision Useful and Actionable

Not all explanations have the same utility for stakeholder goals. This is particularly true for transparency mechanisms that are implemented for the purposes of of __recourse__ or redress by an affected individual against an algorithm’s output.

For example, consider an algorithm that determines whether or not an applicant will be accepted or rejected for a loan based on factors like income, age, and credit score. If an applicant is denied a loan and explanations are generated automatically by SHAP, it may tell the individual that the most important feature impacting the decision was their age – which is something that the individual can do nothing about. Similarly, a counterfactual explanation telling the applicant that they must increase their income 10-fold may be comparatively much more difficult than a small improvement in credit score.

> Key question: is the way transparency has been implemented actually useful in meeting the goals of the stakeholders? Note that involving stakeholders in the design process may be critical to avoid implementing useless and in-actionable explanations.

### Less May be More

One’s initial instinct when implementing transparency for automated decision systems is to provide as much information as possible about the system. While it’s important to be open about many aspects of automated decision systems (especially with respect to how fair or trustworthy they are), overloading stakeholders with information may actually have the counterintuitive effect of making a system seem __more__ opaque. This is not always the case, but there are notable research studies showing negative impacts on the perceived understanding of decision systems by users due to information overload.

> Key question: has too much transparency been implemented into the system in such a way that stakeholders may be confused or misled? Note that involving stakeholders in the design process may be critical to avoid implementing useless and inactionable explanations.

### Don't Manipulate Users

While it should go without saying, transparency mechanisms should not be implemented in a way that deceives or manipulates the stakeholders of automated decision systems. Researchers have uncovered __"dark patterns"__ of transparency that can create a false sense of security for users, and trick them into believing the system is trustworthy or fair when the underlying model is biased against minority groups.

Here are two more examples of dark patterns: first, in one context, researchers found that giving users large volumes of information may arbitrarily make a model appear more fair or trustworthy, even when the additional information has nothing at all to do with the relative fairness of the model. Second, research has shown that data visualizations can successfully be used to misrepresent a message through techniques like exaggeration or understatement.

A taxonomy of dark patterns can be found [here](https://arxiv.org/pdf/2109.12480.pdf). It’s important for those implementing transparency to be aware of dark patterns and pitfalls in transparency so they can be audited for and removed from their work.

> Key question: is the way transparency has been implemented fair, honest, and ethical?

### Consider the Performance-Use Paradox.

The performance-use paradox is a phenomena that was observed for an automated decision system implemented in a public employment setting wherein the users of the system claimed that while they rarely used the output and explanations generated by the system, they preferred having the system as opposed to having it removed. The reason for this phenomena was that users felt more confident in their own decision-making, but liked having the system’s output and explanation as a "potential backup".

For designers of transparent automated decision systems, the performance-use paradox provides an important lesson in understanding that the system may not be the primary means for decision-making, but at worst should be providing explanations that can be used to support and back-up decisions made by human users.

> Key question: is the way transparency has been implemented supporting decision-making in a way that users will be comfortable having the system as a potential backup?

### Transparency is Not Inherent to any System or Algorithm.

Many practitioners and researchers in the machine learning community have created a list of algorithm types that are commonly accepted as being transparent (also called “interpretable”), which consists of linear models, decision trees, and rules-based models. These algorithms are those with __intrinsic transparency mechanisms__, like their linear formula, tree diagram, and rules-list, respectively.

However, recent research has called into question the inherent transparency of these algorithms. For example, it was shown that tree diagrams offer very poor transparency when it comes to having stakeholders identify the most important attribute used in the system’s decision process.

Furthermore, it is important to consider the complexity of these algorithms. If a linear model or rules-list is made up of hundreds or thousands (or more) of rules it will likely no longer be inherently transparent to stakeholders. In fact, one could make an argument that a small neural network with only a few nodes may be more transparent than large rules-lists.

The implication of this design principle is that designers must always consider the value of additional transparency mechanisms even when working with simple algorithms like linear models, decision trees, and rules-based models.

> Key question: is the way transparency has been implemented robust beyond intrinsic transparency mechanisms?