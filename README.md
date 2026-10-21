# Economic Writings

This is a collection of research papers I wrote for my economics and statistics classes at Western Colorado University. I'm double majoring in Computer Science and Economics, and these projects are where I got to use data to answer real-world questions.

---

## 1. Mental Health Days and Income (BRFSS Analysis)

**Class:** Math313 – Statistical Modeling & Simulations (Spring 2026)
**Tools:** R, Quarto

### The question
What health habits and money factors are connected to how many bad mental health days people have in a month?

### The data
I used the CDC's Behavioral Risk Factor Surveillance System (BRFSS), a big national health survey with over 400,000 adults. I looked at poor mental health days, income, sleep, exercise, physical health, BMI and sex.

### What I did
- About 70% of people reported zero bad mental health days, so the data had a ton of zeros and was very spread out.
- Because of that, I compared three models: Poisson, negative binomial and zero-inflated negative binomial.
- The zero-inflated negative binomial model fit best based on a dispersion test and AIC.

### What I found
- **Income was the biggest factor.** People in the lowest income group (under $10k) had about **2.15x more** bad mental health days than people in the highest group (over $75k).
- Not exercising was linked to about **30% more** bad days.
- Each extra hour of sleep was linked to about **6% fewer** bad days.
- Women, people with obesity and people with more bad physical health days also reported more bad mental health days.

Since this is survey data from one point in time, these are connections, not proof of cause and effect.

---

## 2. Understanding Homelessness Across U.S. States

**Class:** ECON 316 – Econometrics (Fall 2025)
**Tools:** SPSS

### The question
Which state factors best predict how many people are experiencing homelessness?

### The data
I combined data for all 50 states plus D.C. from HUD, the Census Bureau, the Bureau of Labor Statistics, the Bureau of Economic Analysis and NOAA. I looked at unemployment, population, median rent, disposable income, poverty rate, homelessness funding per person and whether the state has a warm climate.

### What I did
- Ran a multiple linear regression with all seven variables. It explained about **63%** of the differences between states.
- Removed unemployment, income and poverty since they weren't significant and overlapped with each other.
- Checked for multicollinearity, autocorrelation and heteroskedasticity.

### What I found
- **Population** was the strongest predictor. Bigger states have more people experiencing homelessness.
- Higher **rent** was linked to more homelessness.
- More **funding** per person was linked to less homelessness, but the effect was only marginally significant.
- Warmer states had more homelessness, but it wasn't statistically significant.
- I found heteroskedasticity tied to population size. In the future, using homelessness *rates* instead of total counts would help fix that.

---

## What I learned
- How to pick the right model for the type of data I have
- How to check whether a model's assumptions actually hold
- How to explain statistical results in plain language
- How to combine data from several government sources
