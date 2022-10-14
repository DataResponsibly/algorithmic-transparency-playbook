---
title: Plan and design transparency features (part 2)
---

### Step 2C: Design transparency features for your algorithms given stakeholders and their goals.

Once you have inventoried your list of stakeholders and their needs, you are ready to begin designing transparency features for your algorithmic systems. As a reminder, transparency featuers are those artificats that you create to increase the ability of an algoirhtm to be understood by humans. Importantly, this should be a collaborative design process between _technical and non-technical__ persons within your organization. Technical experts like practitioners, data scientists, data engineers, programmers, and analysts also have their own set of knoweldge on how to implement transparency features for algorithms (this is further detailed later in the course).

Importantly, there are two levels of transparency you need to consider, called the **scope of transparency.** The first is **local** transparency, which provides understanding about a single decision made by an algorithm (ex. a single loan applicant), and second is **global** transparency, which explains how an algorithm works overall. Global transparency can give a "bird’s-eye view" of an algorithmic decision-making system, whereas local transparency focuses in on a particular bird or set of birds.

> **Local transparency** refers to understanding how an algorithmic system makes a decision about a single case or instance, and **global transparency** refers to understanding how an system works overall. For example, for an algorithmic system that predicts whether or not an applicant is accepted for a loan, global transparency would describe how the entire system works, and local transparency would describe the system’s prediction for a single loan applicant.

There are many types of transparency features you want to consider that extend even beyond the scope of this playbook, but here we detail 5 ideas:

- **Transparency labels** for algorithmic decision-making systems are modeled after the kind of nutritional labels found in the food industry.  Nutritional labels are designed to be transparent and understandable, and their contents are perceived as a highly credible source of information by consumers, who use them to guide decision making.

There are several examples of transparency labels for algorithms that have been designed by researchers, and like nutritional labels, they often contain the "ingredients" that make up an algorithm. For example, the labels may include descriptive information about the factors considered by the algorithm (the ingredients), how they are ranked in terms of their importance in the decision-making (ingredient ranking), and attributes related to fairness, which could be useful for meeting stakeholder goals related to validity, trust, privacy, and fairness.

> _When is this useful?_ To provide a global, high-altitude view of the algorithmic system for aspects like (1) what data is being used by the system, (2) how the system weighs that data, (3) metrics on the performance or fairness of the system overall.

- **Data visualizations** can be used to show information about the data used in to create an algorithmic decision system, or facts about the system itself, like how many decisions an algorithm makes per day, and how many people are affected by those decisions.

Visualizations have proved useful for informing users and making complex information more accessible and digestible, and have even been found to have a powerful persuasive effect. Visualizations are often an advisable tool for transparency as they can easily convey lots of information in a simple manner, and organizations commonly staff analysts who specialize in visualizations.

It's also important that visualizations are designed thoughtfully, as they have the ability to be abused and can successfully misrepresent a message through techniques like exaggeration or understatement.

> _When is this useful?_ Useful for presenting complex information in a digestable way, particularly for non-technical users. This could include both internal and external stakeholders, like humans-in-the-loop for the former and affected individauls for the latter.

- Some (but not all) algorithms have built in **intrinsic transparency mechanisms** _(also called intrinsic explainability mechanisms)_ that simply need to be surfaced to offer transparency into how they work.

For example, two common algorithm types are **decision trees** and **rules-lists.** For the former it is possible to print out and display the tree diagram for the user. For the latter, one can list out all the rules used to make a decision for. Another type of commonly used algorithm are **linear models**, which can produce formulas that explain their decision-making. These formulas are sometimes very easy to understand.

Unfortunately, many highly sophisticated algorithms like **random forests** and **neural networks** do not have intrinsic transparency mechanisms. Importantly, the practitioners who designed the algorithm will be aware of whether or not intrinsic transparency mechanisms are available.

> _When is this useful?_  To answer the question ``how does the system work, to the extent that given a new input to the algorithm, I could anticipate the output with a high degree of accuracy?'' Generally for providing a deeper understanding of how the underlying algorithm in the system functions.

> _Decision trees^, rules-lists^, linear models^, random forests, and nueral networks_ are all examples of types of AI algorithms. If you are non-technical, it is not important that you understand what they do or how they work -- your technical team will! For now, just know that the algorithms marked with the carrot _^_ are "more transparent" than others.

- The **attribute importance** _(also called feature importance or factor importance)_ of an algorithm is a list that shows all the different attributes (sometimes called features or factors) that are considered by an algorithm, and their relative weights. It offers **global transparency** for an algorithm.

For example, consider an algorithm that makes predictions on whether or not an individual should receive a loan. The attribute importance could be made up of three attributes: an individual's income, their credit history, and their education level. The weights for these attributes in the algorithm’s decision-making may be 40% income, 40% credit history, and 20% education level.

There are three advantages to using attribute importance. First, attribute importance can be created for any algorithm, no matter how complicated it is. Second, there are a lot of interesting ways to display attribute importance to a human user through data visualizations. Third, from a technical perspective, it is easy to extract the attribute importance from an algorithm.

> _When is this useful?_ Provides a global understanding of how an algorithmic system is processing data at a slightly deeper level than what is often found in transparency labels. Useful for __learning and support__ and to some extent __recourse__. Useful to practitioners for checking the __validity__ of an algorithmic system.

- The **attribute influence** _(also called feature influence or SHAP factors))_ of an algorithm is similar to the attribute importance, except that it shows how the attributes of a single instance or individual impacted the algorithm's output. In contrast to attribute importance, the influence shows the **local transparency** for a particular case. Like with attribute importance, the attribute influence can be created for _any_ algorithm. 

For example, consider again an algorithm that makes predictions on whether or not an individual should receive a loan. If an individual is rejected for a loan, the attribute influence could tell them "your high income and education level were influencing the loan decision from the algorithm positively, but ultimately your low credit score caused the algorithm to reject your loan application."

Generally, when attribute influence is implemented as a transparency measure for an algorithm, individuals are shown the top 3 to 5 attributes that are influencing the algorithm’s output. Importantly, since attribute influence offers local transparency, it is extremely useful in offering **recourse** to affected persons of an algorithm. It is also very useful for human-in-the-loop users who need transparency for the purposes of decision support.

Given all these options, it can be hard to find the best path forward for implementing. In fact, because transparency is so intrinsically tied with design, there are no "objectively correct" answers. Research has even revealed some counter-intuitive ideas about transparency, like offering too much information to users can actually confuse them due to information overload. This emphasizes the importance of thoughtful design, and when possible, participatory design.

As another guideline, it is not sufficient to try and apply general, one-size-fits-all design like simply implementing a transparency label. First, it is unlikely to achieve all stakeholder goals for transparency. Second, it will likely not be regulatory compliant: both the proposed Algorithmic Accountability Act in the United States and the Artificial Intelligence Act in the European Union specifically mention that algorithmic transparency should allow individuals to have recourse against a system’s outcome, which implies the use of local transparency like attribute influence. Many other countries around the world have also begun considering similar legislation.

> _When is this useful?_ To provide local transparency about a single instance, generally an affected individual. The attribute influence is one of the best ways to answer the question, ``why did the algorithmic system have this output for \emph{this specific person}?'' Extremely useful for __recourse__ for affected individuals. Very useful for __learning and support__ for humans-in-the-loop.

#### What if I don’t know where to begin?
    
As a baseline, if you are unsure which transparency features to choose your algorithm, you should strongly consider implementing transparency labels, attribute importance, and attribute influence for algorithms impacting people and their lives, and tailor them to meet your stakeholders’ needs.
    
#### What is the difference between a good transparency design and a bad transparency design?
    
Unfortunately, there are currently no ways of objectively measuring the quality of transparency in algorithmic decision systems. There is also no research consensus on best practices for transparency. As a result, the quality of algorithmic transparency within your organization is subjective and ultimately up to the algorithm’s’ stakeholders and whether or not they feel the transparency designs you create meet their transparency goals.

> **DELIVERABLE:** Ideas and designs for which transparency features you want to implement for the algorithms in your organization, and how those features will meet stakeholder goals.

<br>

#### Step 2D: Speak with your technical team to review your design ideas.

After deciding on a set of transparency features to implement, it’s important to loop-in your technical team (like practitioners, data scientists, data engineers, programmers, and analysts). In fact, you may want to include them in earlier steps if their bandwidth allows.

Including your technical team in design discussions is critical for designing and implementing strong transparency measures because of the information asymmetry that exists between what is technically feasible in terms of transparency, and what is ideal for stakeholders. For example, your technical team will be aware of whether or not intrinsic transparency mechanisms exist for your algorithms, or if other transparency tools can be applied to your algorithms.

In general, it is the responsibility of those who design algorithms to understand how they can be made transparent. Luckily, many of those who build algorithms are already aware of transparency features through their experience debugging algorithms and testing their validity.

> **DELIVERABLE:** A refined idea and design for implementing transparency for your organization’s algorithms.