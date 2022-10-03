---
layout: page
---

## A Survey of Transparency Methods

There are a wide range of transparency tools available – some of which have been around well before the resurgence of AI, and some developed in recent years. Here we catalog a number of known methods, provide a short several details relevant to their implementation, and links to relevant documentation (when applicable). Note that the XAI field is in constant flux and new methods for explainability are being developed on a near-yearly basis.

<br>

### Intrinsic explainability mechanisms

Some algorithms have built-in tools for explainability. These include algorithms like [decision trees](https://scikit-learn.org/stable/modules/tree.html), [linear models](https://scikit-learn.org/stable/modules/linear_model.html), and [rules-list](https://christophm.github.io/interpretable-ml-book/rules.html) where artifacts like the tree diagram, the linear formula, and a list of if-then rules, respectively can be easily extracted from the model. Researchers have also developed experimental methods for extracting intrinsic explainablity from black-box. One such example is [Self-Explaining Nueral Networks](https://arxiv.org/abs/1806.07538).

<br>

### Counterfactual explanations

A full discussion of counterfactual explanations can be found [here](https://christophm.github.io/interpretable-ml-book/counterfactual.html), but in summary, counterfactual explanations are local example-based explanations that are used to show how changes in input features impact outputs.

For counterfactual explanations of a single individual, features are perterbutated to see the impact on the outcome. For example, one can modify an individual's income or education level to understand how that would influence an algorithm’s decision to grant or deny them a loan.

<br>

### Post-hoc explainability methods

Post-hoc explainability methods can be very useful for creating explanations of both black-box and interpretable models. These methods generate local explanations about an input into an already trained algorithm or model (hence "post-hoc"). In order of popularity, the most commonly used are SHAP, LIME, and QII. There is also a new method known as SAGE by the creators of SHAP that provides global model explanations.

In industry, SHAP is the most commonly used post-hoc explainability method. This is because it is intuitive and easy to implement due its well-maintained [Python package](https://shap.readthedocs.io/en/latest/index.html). An implementation of SHAP could include showing stakeholders the top 3 factors that influence their output positively, and the 3 factors that influence their output negatively.

While there are many positives to post-hoc explainability methods like SHAP (intuitive, easy to understand), there are several weaknesses that should be noted: (1) there are several examples of instability in post-hoc explanations where similar inputs yield very different explanations, (2) features identified by SHAP as important are not necessarily those which are actionable, important, or meaningful to stakeholders (3) post-hoc explainability methods are vulnerable to adversarial attacks, (4) the built-in visualizations created by SHAP were designed for data scientists and are not always useful or easily understood by other stakeholders.

<br>

### Crosstabs

Crosstabs are a model agnostic method that provide global or group-level explanations about the outputs of a model. Crosstabs are simply summaries of the top 10-25% highest (or lowest) scored outputs of an algorithm.

For example, crosstabs for an algorithm used to predict whether or not an individual will be approved for a loan may show that the 10% most likely to be approved have an average income of $100,000 and a credit score of 750, versus the 10% most likely to be denied which may have an average income of $15,000 and a credit score of 350.

One advantage of crosstabs is that they can be used to provide group level explanations. One such use-case is comparing crosstabs between members of different protected groups to understand the fairness of your algorithm.

<br>

### Simplifying algorithms

One technique that can improve the explainability of complex algorithms is replacing them with simpler models that make similar predictions. In many cases (but not all), simpler models can be used to approximate the outputs made by more complex models. To do this, create a simpler model and compare the outputs of that model using [Jaccard plots of similarity](https://en.wikipedia.org/wiki/Jaccard_index). Indications of high similarity may show that you can drastically reduce the feature space of a model while maintaining high fidelity to the models original output.

There are also methods for directly reducing the complexity of models, like select-regress-round where complex linear models are reduced to short rules-list. Empirical evidence shows that in many cases using select-regress-round does not significantly impact the accuracy of an algorithm.