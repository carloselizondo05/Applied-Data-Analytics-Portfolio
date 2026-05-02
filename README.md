# CIND123 — Data Analytics: Basic Methods
**Toronto Metropolitan University** · Winter 2026

> Covers foundational statistical and analytical methods for data science, including probability distributions, regression modeling, correlation analysis, and simulation techniques applied to real-world datasets.

---

## 🛠 Skills & Tools
**Languages:** Python  
**Libraries:** Pandas, NumPy, SciPy, Scikit-learn, Statsmodels, Matplotlib, Seaborn  
**Techniques:** Survival Analysis, Probability Modeling (Binomial/Poisson), Linear Regression, Monte Carlo Simulation

---

## 📚 Assignments

### Assignment 1: Survival Analysis & Probability Modeling
![Individual](https://img.shields.io/badge/type-Individual-1565c0)

**Overview:** Applied core data analytics techniques across two distinct problem domains — passenger survival analysis and clinical probability modeling — using the Titanic dataset and two independent probability scenarios.

Conducted structured exploratory analysis on the Titanic passenger dataset: extracted and filtered subsets, imputed 263 missing age values using median substitution, computed survival rates by passenger class (Class 1: 61.9%, Class 2: 43.0%, Class 3: 25.5%), and visualized fare distribution by sex using boxplots and mean aggregation. Applied conditional filtering logic to identify specific passenger profiles meeting multi-variable criteria. In the probability section, modeled medication dosage error rates using the Binomial distribution to estimate the likelihood of five or more incorrectly prepared doses in a daily batch of 100, and applied the Poisson distribution to model complaint volume at a call center given a known hourly arrival rate.

**Tech stack:** Python (Pandas, NumPy, Matplotlib, Seaborn, SciPy), Jupyter Notebook

**Key result:** Class 1 passengers were 2.4x more likely to survive than Class 3; binomial and Poisson models produced closed-form probability estimates validated against intuitive interpretations of the underlying processes.

---

### Assignment 2: Regression, Correlation & Monte Carlo Simulation
![Individual](https://img.shields.io/badge/type-Individual-1565c0)

**Overview:** Applied inferential statistics and predictive modeling across three areas: normal distribution analysis, linear regression on academic and crime data, and Monte Carlo simulation for probability estimation.

Modeled smartphone battery life under a normal distribution, computing tail probabilities, interval probabilities, and the 5th percentile threshold using SciPy. Built a least-squares linear regression model on student grade data, visualized the regression line, and generated predictions for new midterm scores. On a North Carolina county-level crime dataset, compared two regression models predicting conviction probability using log-transformed vs. raw police per capita as predictors — finding the raw model explained 20.8% of variance vs. 14.2% for the log version — and computed Pearson correlation coefficients to assess relationships between conviction, arrest, prison sentence, and tax variables. Concluded with a Monte Carlo simulation of 100,000 trials to estimate the probability of rolling more than five even numbers in 20 die rolls, validating the result against the theoretical Binomial value with a difference of 0.0001.

**Tech stack:** Python (Pandas, NumPy, SciPy, Scikit-learn, Statsmodels, Matplotlib, Seaborn), Jupyter Notebook

**Key result:** Monte Carlo estimate converged to within 0.01% of the theoretical Binomial probability across 100,000 trials; police per capita was identified as a statistically significant positive predictor of conviction probability (p < 0.001) while metropolitan area was a significant negative predictor across both models.

---

## ⚠️ Limitations & Future Work

- The crime dataset regression models explain at most ~21% of variance in conviction probability, indicating significant unmodeled factors (socioeconomic conditions, judicial resources, etc.).
- Monte Carlo precision improves with trial count — the 50-run mean approach further reduces variance and could be extended to adaptive stopping criteria.
- Future work could explore multiple regression with interaction terms on the crime data to improve predictive power beyond the two-predictor models used here.

---

## 🤝 Contributing & License

Suggestions and feedback welcome — open an issue or pull request.

Licensed under the [MIT License](LICENSE).
