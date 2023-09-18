---
title: Case Study
---

## Algorithms Used in Public Employment
_Suggested time: 10 minutes_

The purpose of this case study is to make some of the ideas we discussed about stakeholders, goals, and transparency tools more concrete.

### Context-of-use

Algorithmic decision-systems are increasingly being used by government agencies to help unemployed persons. Many governments are concerned with identifying individuals that are at risk of becoming _long-term unemployed_, that is, being unemployed for 12-months or more. The long-term unemployed are particularly vulnerable persons, and tend to earn less once they find new jobs, have poorer health and have children with worse academic performance as compared to those who had continuous employment.

Many countries around the world are using algorithms to help tackle long-term unemployment, including Portugal and the UK. If those at risk of being long-term unemployed can be correclty predicted, appropriate interventions like job search trainings, resume workshops, or reskilling programs can be administred.

<!-- >> **The harsh reality of resoruce constraints:** in an ideal world, public employment agencies would be able to identify individuals who are likely to be long-term unemployed so that they can be given appropriate interventions to get ahead of the problem, like job search trainings, resume workshops, or reskilling programs. This is where algorithmic decision-systems come in to play: governments can use these systems to spot those at risk of becoming long-term unemployed. For instance, a system of _exactly_ this type is used by the national Portuguese vocational agency. -->

### How the system works

Once a person becomes unemployed, their change in employment status is often reported to a government agency, either by their previous employer or when an individual applies for unemployment benefits. For example, in the US, you must go through your state-level Department of Labor to receive benefits.

In this scenario, once a person registers that they are unemployed, they are assigned a case-worker known as a "job counsellor." The job counselor will reach out to the individual (either by phone or by scheduling an in-person meeting) to gather information like their age, marital status, education level, and their work history. This information, along with macroeconomic data related to the individual's employment sector and location of work, are passed into an **algorithmic system** used by the job counselor that generates a risk score between 1 and 5 for how likely it is that the person will become long-term unemployed. If someone is identified as a risk level of 5, they will be offered free job-related interventions by the state like resume workshops or even job trainings.

### Stakeholders and their goals

Using what we learned about stakeholders and their goals, we can create the following table:

<br>


| Stakeholder                                         | Goals                                                                                                                                                                                    |
|-----------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Humans-in-the-loop (job counselors)                 | Learning and support, validity. The job counselor may want to know how the system works overall, and why a particular individual is assigned to a certain risk score.                    |
| Affected persons (unemlpoyed individual)            | Recourse, trust. An individual may believe they are high risk and deserve interventions regardless of the output of the algorithm (or vice-versa)                                        |
| Managers (ex. officials at the Department of Labor) | Learning and support, trust, validity, fairness. The managers may have similiar questions to the job counselor and practitioner, plus concerns about the overall fairness of the system. |
| Compliance officers (ex. auditors)                  | Fairness, privacy. Since the system is working with sensitive data, auditors will want to make sure the system is compliant with applicable fairness and privacy laws.                   |
| Practitioners                                       | Learning and support, validity, trust. Even though the system is already built, practitioners may be interested in monitoring its performance over time.                               |


<br>

Ideally, we would begin applying _participatory design_ at this point, and speak with all the relevant stakeholders to verify that we understand their transparency goals. This is particularly true for job counselors using the system, and the unemployed persons affected by the outcome.

Here are some examples of what we might hear if we talked with stakeholders:

- **Affected persons.** "I want to know if an algorithmic system is being used on me."; "I would like to know what data is being used in an algorithmic system"; "I want to be able to challenge the outcome of the system."

- **Job counselors.** "I need to understand why the algorithmic system assigns a person to a particular risk score. Based on my experience as a job counselor, I may agree (or disagree) with the system's prediction."

- **Managers.** "I want to understand what data is being used by the algorithmic decision system, and what factors it considers important. I want to have a `bird's eye view' of the system. I would also like to know if job counselors are consistently agreeing (or disagreeing) with the risk estimates produced by the algorithm."

### Transparency tools

We can begin by considering the goals of managers and compliance officers, who are concerend a high-altitude view of the algorithmic system. This is a perfect applciation for **transparency labels**, which present snapshots on the data being used by the algorithm, how it rates the importance of that data (**the attribute influence**), and even metrics related to how the system performs for different protected groups. This could be accompanied by text describing what measures are taken to ensrue the privacy of individuals. <!--Below is a mock-up of transparency labels:-->

Next, for learning and support for job counselors and for recourse for individuals, some type of **local transparency** method must be implemnted, because local transparency is specific to each unemployed person. A good choice for this is showing the **attribute influence** for each risk estimate made the system. <!--Also, it may be necessary to contextualize the informaiton shown to users. For example, if an unemployed person has a risk score of 3, what does this _accutally_ mean? What is the chance that a person with a risk score of 3 will become long-term unemployed relative to those with higher or lower scores? Two strong technical choices for attribute influence in this scenario would be SHAP explanations or counterfacutal explanations.-->

Lastly, the technical team and managers within your organization may want a customized dashboard that displays technically-revelant performance metrics about the algorithm. For example, managers may want to understand how often job counselors agree or disagree with the system, as well as track the overall accuracy of the system in predicting long-term unemployed persons. These types of metrics would be helpful in surfacing degredation of the model over time.