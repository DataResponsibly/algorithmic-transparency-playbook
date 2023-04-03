---
title: Plan and design for transparency
---

## Plan & design transparency for your algorithms
_Suggested time: 10 minutes_

Once you have identified all the algorithmic decision-making systems within your organization, it is time to begin planning and designing how transparency will be used in those algorithms. In the case of procured tools, these steps will likely involve engaging with the organization that owns the algorithm.

This second step is broken up into 4 sub-steps and is based on our **stakeholder-first approach** to developing transparency that begins with thinking about algorithmic stakeholders first, and ends with creating transparency features for your algorithms that meet stakeholder needs.

> A _transparency feature_ is any artificat accompayning an algorithm that helps increase its ability to be understood by a human user. Some examples include a dashboard, graph, report, paper hand-out, or even an informational pop-up window on a web page.

<br>

### Consider all the relevant stakeholders of each algorithm

Earlier in the course we discussed several important stakeholders of algorithmic systems. These included **managers** within an organization and the **affected persons** who are impacted by the outcome of the stakeholder. Notably, stakeholders may be both internal and external to your organization.

Another stakeholder group is **humans-in-the-loop**, or those who are actually responsible for using the algorithmic tool. These are often distinct from those developing the algorithm, and some examples include an underwriter using an algorithm to determine if loan applicants should be accepted or rejected, or hospital staff using an algorithm to predict the risk a patient will develop a disease.

Importantly, **not every stakeholder has the same needs when it comes to algorithmic transparency, and so those implementing transparency should be thoughtful about each type of stakeholder.** There are 5 categories of stakeholders that you should consider (note that every algorithm will have all 5 stakeholders):

| **Stakeholder**         | **Definition**                                                                                                                                                                        |
|-------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Practitioners**       | The technical practitioners that are developing, implementing, and maintaining algorithmic systems. They include _data scientists, engineers, programmers, developers, and analysts._ |
| **Managers**            | The individuals at many different levels in an organization that oversee algorithmic decision-making tools. They include _project managers, business developers, and executives._     |
| **Affected persons**    | The people who are impacted by the algorithm. For example, if an algorithm is being used to assess job applicants, the job applicants are the affected persons.                       |
| **Humans-in-the-loop**  | The individuals who are responsible for using the algorithm. Humans-in-the-loop may also be called _algorithm managers or users._                                                     |
| **Compliance officers** | Persons who oversee the legal compliance of algorithms, and may include _auditors and policymakers._                                                                                  |

For each algorithm you identified during the inventory phase, you should consider **each of the stakeholder categories above.** Furthermore, you may want to prioritize your list of stakeholders and weigh their needs differently. For example, it may be more meaningful to meet the transparency needs of affected persons over managers or compliance officers.

> **DELIVERABLE:** A list of stakeholders for each algorithmic decision-making system in your organization.

<br>

### Create a list of the potential goals of each stakeholder

After you have determined the stakeholders of each system in your organization, you should consider their goals for transparency. Remember that transparency goals always start with a stakeholder since transparency is always ultimately intended for a human audience.

Broadly, the goals of transparency are ensuring validity, building trust, assisting in learning and support, supporting recourse, and ensuring fairness and privacy. These goals are below:

| Goal                 | Definition                                                                        | Example                                                                                                 |
|----------------------|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| Validity             | Making sure the system is constructed correctly, debugging a system               | The programmers, engineers, and managers may use transparency to ensure the system is valid and correct |
| Trust                | Knowing "how often the system is right"                                           | A policymaker or auditor may use transparency to gain trust in the ADS                                  |
| Learning and Support | Increasing general understanding about how an algorithm reaches a decision        | A doctor may use transparency to better understand an algorithms predicted diagnosis of a patient       |
| Recourse             | Allowing affected persons to take action against a decision                       | An individual may use transparency about an algorithm to appeal a loan rejection                        |
| Fairness             | Ensuring that an algorithm is ** making decision biased against a minority group | An auditor may use transparency to make sure that an algorithm is ** biased                            |
| Privacy              | Ensuring that an algorithm respects the data privacy of individuals               | An auditor may use transparency to make sure that an algorithm is ** violating data privacy laws       |

One critical goal for transparency is the idea of **algorithmic recourse** (sometimes called **redress**), which is the ability of a person affected by the outcome of an algorithm to see why that decision was made and what they can do to change that outcome. For example, if an algorithm is used to determine whether or not an individual is accepted or rejected for a loan, that individual should be able to see why that decision was made so they can take actions to change the decision in the future (ex. improve credit score). <!---Notably, recourse has become a popular idea among policymakers, and there is proposed legislation in both the United States and Europe that would mandate designing algorithms that allow recourse for affected persons.-->

When possible, ideas from **participatory design** should always be used to determine stakeholder goals. Participatory design, also called _co-operative design or co-design_, is an approach to design wherein those stakeholders identified earlier are _actively involved in the design process_to help ensure the result meets their needs. In one promising example, designers used participatory design to successfully create better explanations about an algorithmic tool in the field of communal energy accounting by having conversations with directly with the tool's users.

> **DELIVERABLE:** A list of goals for each stakeholder of each algorithmic decision-making system in your organization. At this point, your running inventory might be quite long --- but you can be assured that you have thoughtfully considered all the important aspects of algorithmic transparency.

### Design transparency features for your algorithms given stakeholders and their goals.

Once you have inventoried your list of stakeholders and their needs, you are ready to begin thinking about and designing transparency features for your algorithmic systems. As a reminder, transparency featuers are those artificats that you create to increase the ability of an algoirhtm to be understood by humans. **Importantly, whenever possible, this should be a collaborative design process between _technical and non-technical__ persons within your organization.** <!---Technical experts like practitioners, data scientists, data engineers, programmers, and analysts also have their own set of knoweldge on how to implement transparency features for algorithms (this is further detailed later in the course).-->

<!---Importantly, there are two levels of transparency you need to consider, called the **scope of transparency.** The first is **local** transparency, which provides understanding about a single decision made by an algorithm (ex. a single loan applicant), and second is **global** transparency, which explains how an algorithm works overall. Global transparency can give a "bird’s-eye view" of an algorithmic decision-making system, whereas local transparency focuses in on a particular bird or set of birds.-->

> **Levels of transparency** <br><br> **Local transparency** refers to understanding how an algorithmic system makes a decision about a single case or instance, and **global transparency** refers to understanding how an system works overall (a bird's-eye view). For example, for an algorithmic system that predicts whether or ** an applicant is accepted for a loan, global transparency would describe how the entire system works, and local transparency would describe the system’s prediction for a single loan applicant.

#### Examples of transparency features

- **Transparency labels and model cards** for algorithmic tools are similiar to nutritional labels found in the food industry.  Nutritional labels are designed to be transparent and understandable, and their contents are perceived as a highly credible source of information by consumers, who use them to guide decision making.

There are several examples of transparency labels for algorithms that have been designed by researchers, and like nutritional labels, they often contain the "ingredients" that make up an algorithm. For example, the labels may include descriptive information about the factors considered by the algorithm (the ingredients), how they are ranked in terms of their importance in the decision-making (ingredient ranking), and attributes related to fairness, which could be useful for meeting stakeholder goals related to validity, trust, privacy, and fairness.

> **When is this useful?** To provide a global, high-altitude view of the algorithmic system for aspects like (1) what data is being used by the system, (2) how the system weighs that data, (3) metrics on the performance or fairness of the system overall.

- **Data visualizations** can be used to show information about the data used in to create an algorithmic decision system, or facts about the system itself, like how many decisions an algorithm makes per day, and how many people are affected by those decisions.

Visualizations have proved useful for informing users and making complex information more accessible and digestible, and have even been found to have a powerful persuasive effect. Visualizations are often an advisable tool for transparency as they can easily convey lots of information in a simple manner, and organizations commonly staff analysts who specialize in visualizations.

It's also important that visualizations are designed thoughtfully, as they have the ability to be abused and can successfully misrepresent a message through techniques like exaggeration or understatement.

> **When is this useful?** Useful for presenting complex information in a digestable way, particularly for non-technical users. This could include both internal and external stakeholders, like humans-in-the-loop for the former and affected individauls for the latter.

- Some (but not all) algorithms have built in **intrinsic transparency mechanisms** _(also called intrinsic explainability mechanisms)_ that simply need to be surfaced to offer transparency into how they work.

For example, two common algorithm types are **decision trees** and **rules-lists.** For the former it is possible to print out and display the tree diagram for the user. For the latter, one can list out all the rules used to make a decision for. Another type of commonly used algorithm are **linear models**, which can produce formulas that explain their decision-making. These formulas are sometimes very easy to understand.

Unfortunately, many highly sophisticated algorithms like **random forests** and **neural networks** do ** have intrinsic transparency mechanisms. Importantly, the practitioners who designed the algorithm will be aware of whether or ** intrinsic transparency mechanisms are available.

> **When is this useful?**  To answer the question ``how does the system work, to the extent that given a new input to the algorithm, I could anticipate the output with a high degree of accuracy?'' Generally for providing a deeper understanding of how the underlying algorithm in the system functions.

> _Decision trees^, rules-lists^, linear models^, random forests, and nueral networks_ are all examples of types of AI algorithms. If you are non-technical, it is *not* important that you understand what they do or how they work -- your technical team will! For now, just know that the algorithms marked with the carrot _^_ are _more transparent_ than others.

- The **attribute importance** _(also called feature importance or factor importance)_ of an algorithm is a list that shows all the different attributes (sometimes called features or factors) that are considered by an algorithm, and their relative weights. It offers **global transparency** for an algorithm.

For example, consider an algorithm that makes predictions on whether or ** an individual should receive a loan. The attribute importance could be made up of three attributes: an individual's income, their credit history, and their education level. The weights for these attributes in the algorithm’s decision-making may be 40% income, 40% credit history, and 20% education level.

There are three benefits of attribute importance:
- Attribute importance can be created for any algorithm, no matter how complicated it is.
- There are a lot of interesting ways to display attribute importance to a human user through data visualizations.
- From a technical perspective, it is easy to extract the attribute importance from an algorithm. This makes it _low cost_.

> **When is this useful?** Provides a global understanding of how an algorithmic system is processing data at a slightly deeper level than what is often found in transparency labels. Useful for __learning and support__ and to some extent __recourse__. Useful to practitioners for checking the __validity__ of an algorithmic system.

- The **attribute influence** _(also called feature influence or SHAP factors))_ of an algorithm is similar to the attribute importance, except that it shows how the attributes of a single instance or individual impacted the algorithm's output. In contrast to attribute importance, the influence shows the **local transparency** for a particular case. Like with attribute importance, the attribute influence can be created for _any_ algorithm. 

For example, consider again an algorithm that makes predictions on whether or not an individual should receive a loan. If an individual is rejected for a loan, the attribute influence could tell them _your high income and education level were influencing the loan decision from the algorithm positively, but ultimately your low credit score caused the algorithm to reject your loan application._

<!---Generally, when attribute influence is implemented as a transparency measure for an algorithm, individuals are shown the top 3 to 5 attributes that are influencing the algorithm’s output. Importantly, since attribute influence offers local transparency, it is extremely useful in offering **recourse** to affected persons of an algorithm. It is also very useful for human-in-the-loop users who need transparency for the purposes of decision support.-->

> **When is this useful?** To provide local transparency about a single instance, generally an affected individual. The attribute influence is one of the best ways to answer the question, ``why did the algorithmic system have this output for \emph{this specific person}?'' Extremely useful for __recourse__ for affected individuals. Very useful for __learning and support__ for humans-in-the-loop.

### Where do I begin?

Given all these options, it can be hard to find the best path forward for implementing transparency. **In fact, because transparency is so intrinsically tied with design and the human experience, there are no objectively correct answers.** Research has even revealed some counter-intuitive ideas about transparency, like offering too much information to users can actually confuse them due to information overload. This emphasizes the importance of thoughtful design, and when possible, participatory design.

<!--As another guideline, it is not sufficient to try and apply general, one-size-fits-all design like simply implementing a transparency label. First, it is unlikely to achieve all stakeholder goals for transparency. Second, it will likely not be regulatory compliant: both the proposed Algorithmic Accountability Act in the United States and the Artificial Intelligence Act in the European Union specifically mention that algorithmic transparency should allow individuals to have recourse against a system’s outcome, which implies the use of local transparency like attribute influence. Many other countries around the world have also begun considering similar legislation. -->
    
As a baseline, if you are unsure which transparency features to choose your algorithm, you should strongly consider implementing transparency labels, attribute importance, and attribute influence for algorithms impacting people and their lives, and tailor them to meet your stakeholders’ needs.
    
#### What is the difference between a good transparency design and a bad transparency design?
    
Unfortunately, there are currently no ways of objectively measuring the quality of transparency in algorithmic decision systems. There is also no research consensus on best practices for transparency. As a result, the quality of algorithmic transparency within your organization is subjective and ultimately up to the algorithm’s’ stakeholders and whether or not they feel the transparency designs you create meet their transparency goals.

<!--- > **DELIVERABLE:** Ideas and designs for which transparency features you want to implement for the algorithms in your organization, and how those features will meet stakeholder goals. -->

<br>

#### Speak with your technical team to review your design ideas.

After deciding on a set of transparency features to implement, it’s important to loop-in your technical team (like practitioners, data scientists, data engineers, programmers, and analysts). In fact, you may want to include them in earlier steps if their bandwidth allows.

The technical team is critical for brdiging the gap between what is technically feasible in terms of transparency, and what is ideal for stakeholders. For example, your technical team will be aware of whether or not intrinsic transparency mechanisms exist for your algorithms, or if other transparency tools can be applied to your algorithms.

<!---In general, it is the responsibility of those who design algorithms to understand how they can be made transparent. Luckily, many of those who build algorithms are already aware of transparency features through their experience debugging algorithms and testing their validity. -->

> **DELIVERABLE:** A refined idea and design for implementing transparency for your organization’s algorithms.