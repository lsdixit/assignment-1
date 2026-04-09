# Homework 1 Task 3

---

Answer the following questions based on exercises from *An Introduction to Statistical Learning with Applications in Python*.

## Chapter 2.4 Exercises

---

### Exercise 1 (ISLP exercise 2)

Explain whether each scenario is a **classification or regression** problem, and indicate whether we are most interested in **inference or prediction**. Finally, provide **n** (size of observation dataset) and **p** (number of predictors).

**(a)**  We collect data on 200 protected marine reserves worldwide. For each reserve we record species richness, reserve size, years since establishment, enforcement budget, and proximity to human settlements. We are interested in understanding which factors affect species richness.

> **Your Answer:**

Regression - quantitative response (species richness)
Inference - understanding which factors affect richness 
n = 200, p = 5

---

**(b)** A conservation agency wants to know whether a proposed habitat corridor will successfully support wildlife movement or fail to do so. They collect data on 30 previously established corridors. For each corridor they have recorded whether wildlife movement was successful or unsuccessful, corridor width, length, surrounding land use type, and eight other variables.

> **Your Answer:**

Classification - binary response (success or fail)
Prediction - predict whether proposed corridor will succeed or fail
n = 30, p = 12

---

**(c)** We are interested in predicting weekly average ground-level ozone concentration in a coastal city. We collect weekly data for all of 2019. For each week we record average ozone concentration, sea surface temperature, wind speed, solar radiation, and atmospheric

> **Your Answer:**

Regression - quantitative response - Weekly average ozone concentration 
Prediction - predict weekly average ozone concentration
n = 52, p = 5

---

### Exercise 2 (ISLP exercise 5)

What are the advantages and disadvantages of a very flexible (versus a less flexible) approach for regression? Under what circumstances might a more flexible approach be preferred to a less flexible approach? When might a less flexible approach be preferred?

> **Your Answer:**

Choosing between a flexible and restrictive approach for regression ultimately comes down to the goal of the model outcomes: interpretability versus model accuracy. A flexible model has the potential to predict the true f better than a restrictive model, but likely requires the use of more parameters and has the downside of being less interpretable and has a higher chance of overfitting the data. A restrictive model, on the other hand, is very easy to interpret directly but likely does not match the true f. We may want to use a flexible model when we care more about the prediction accuracy than understanding the statistical coefficients, and conversely may choose a restrictive model when we want to directly interpret results at the cost of prediction accuracy. In the end, it is perhaps best to run a multitude of flexible and restrictive model to find one that balances interpretability with accuracy and minimizes error the best for the data and questions being asked.

---

### Exercise 3 (ISLP exercise 6)

Describe the differences between a **parametric** and a **non-parametric** statistical learning approach. What are the **advantages** of a parametric approach to regression or classification (as opposed to a non-parametric approach)? What are its **disadvantages**?

> **Your Answer:**

Very similarly to the flexible vs restrictive approach for regression, a parametric statistical learning approach makes an initial assumption about the functional form of the relationship between predictors and outcome variables. Conversely, a non-parametric approach makes no initial assumption about the functional form and instead try to estimate f such that it minimizes distance to each data point while keeping a smooth fit. Parametric approaches have a strong disadvantage of potentially fitting an incorrect model to the data based on an incorrect initial assumption of fit. However, they are much easier to estimate and interpret coefficients and require much less data. Non-parametric approaches likely fit a functional form of the relationship that is more accurate to the true f by making no initial assumptions, however require a very large amount of data and are harder to interpret. 