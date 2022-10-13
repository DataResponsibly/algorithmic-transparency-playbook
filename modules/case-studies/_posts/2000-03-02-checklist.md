---
title: Public Employment (Using the Transparency Checklist)
---

## Using the Algorithmic Transparency Checklist

We have already completed Step 1 by identifying the algorithmic decision system being used. We can now complete Step 2a-b, and create a list of stakeholders and their potential goals:

| Stakeholder                                         | Goals                                                                                                                                                                                    |
|-----------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Humans-in-the-loop (job counselors)                 | Learning and support, validity. The job counselor may want to know how the system works overall, and why a particular individual is assigned to a certain risk score.                    |
| Affected persons (unemlpoyed individual)            | Recourse, trust. An individual may believe they are high risk and deserve interventions regardless of the output of the algorithm (or vice-versa)                                        |
| Managers (ex. officials at the Department of Labor) | Learning and support, trust, validity, fairness. The managers may have similiar questions to the job counselor and practitioner, plus concerns about the overall fairness of the system. |
| Compliance officers (ex. auditors)                  | Fairness, privacy. Since the system is working with sensitive data, auditors will want to make sure the system is compliant with applicable fairness and privacy laws.                   |
| Practitioners                                       | Learning and support, validity, trust. Even though the system is already built, practitioners may be interested in monitoring its performance over time to                               |

Ideally, we would begin applying _participatory design_ at this point, and speak with all the relevant stakeholders to verify that we understand their transparency goals. This is particularly true for job counselors using the system, and the unemployed persons affected by the outcome.

Here are some examples of what we might hear if we talked with stakeholders:

- **Affected persons.** "I want to know if an algorithmic system is being used on me."; "I would like to know what data is being used in an algorithmic system"; "I want to be able to challenge the outcome of the system."

- **Job counselors.** "I need to understand why the algorithmic system assigns a person to a particular risk score. Based on my experience as a job counselor, I may agree (or disagree) with the system's prediction."

- **Managers.** "I want to understand what data is being used by the algorithmic decision system, and what factors it considers important. I want to have a `bird's eye view' of the system. I would also like to know if job counselors are consistently agreeing (or disagreeing) with the risk estimates produced by the algorithm."

Next we move to Step 2C and Step 2D, where we design transparency features for our algorithmic system and then speak with the technical team about implementing them. Ideally, we would continue the participatory design process and gather feedback on our transparency features from the respective stakeholders.

We can begin by considering the goals of managers and compliance officers, who are concerend a high-altitude view of the algorithmic system. This is a perfect applciation for transparency labels, which presents snapshots on the data being used by the algorithm, how it rates the importance of that data (the attribute influence), and even metrics related to how the system performs for different protected groups. This could be accompanied by text describing what measures are taken to ensrue the privacy of individuals. Below is a mock-up of transparency labels:

Two other uses of tansparency labels include informing affected individuals on the existence of the algorithm, and for training job counselors about the system.

Next, for learning and support for job counselors and for recourse for individuals, some type of local transparency method must be made visible. A good choice for this is showing the attribute influence for each risk estimate made the system. Also, it may be necessary to contextualize the informaiton shown to users. For example, if an unemployed person has a risk score of 3, what does this _accutally_ mean? What is the chance that a person with a risk score of 3 will become long-term unemployed relative to those with higher or lower scores? Two strong technical choices for attribute influence in this scenario would be SHAP explanations or counterfacutal explanations.

Lastly, the technical team and managers within your organization may want a customized dashboard that displays technically-revelant performance metrics about the algorithm. For example, managers may want to understand how often job counselors agree or disagree with the system, as well as track the overall accuracy of the system in predicting long-term unemployed persons. These types of metrics would be helpful in surfacing degredation of the model over time.

Before moving to Step 3, it is also a could idea to review the **Design Considerations** section of this course to make sure you have avoided any transparency pitfalls. For example, one dashboard containing all the information above may very likely be counter productive to transparency by overwhelming stakeholders with too much information that is relevant to their specific goal.

With the design work out of the way, it is time to move to Step 3A and Step 3B where the technical team implements the transparency solutions (for example, they may have to build several dashboards as described above) and tests them with the end users.

At this point, we are finished implementing transparency into the system! All we need to do now is move on to Step 4A and make sure a process is in place to continually monitor the system and the transparency features into the future.