# Applied Data Analytics Portfolio

---

## CIND123 — Data Analytics: Basic Methods
**Toronto Metropolitan University** · Winter 2026

> Covers foundational statistical and analytical methods for data science, including probability distributions, regression modeling, correlation analysis, and simulation techniques applied to real-world datasets.

---

## 🛠 Skills & Tools
**Languages:** Python  
**Libraries:** Pandas, NumPy, SciPy, Scikit-learn, Statsmodels, Matplotlib, Seaborn  
**Techniques:** Survival Analysis, Probability Modeling (Binomial/Poisson), Linear Regression, Monte Carlo Simulation

---

## 📂 Featured Projects

### [Assignment 1: Survival Analysis & Probability Modeling](./CIND123/CIND123%20A1/Assignment_1.ipynb)
![Individual](https://img.shields.io/badge/type-Individual-1565c0)

**Overview:** Applied core data analytics techniques across two distinct problem domains — passenger survival analysis and clinical probability modeling — using the Titanic dataset and two independent probability scenarios.

Conducted structured exploratory analysis on the Titanic passenger dataset: extracted and filtered subsets, imputed 263 missing age values using median substitution, computed survival rates by passenger class (Class 1: 61.9%, Class 2: 43.0%, Class 3: 25.5%), and visualized fare distribution by sex using boxplots and mean aggregation. Applied conditional filtering logic to identify specific passenger profiles meeting multi-variable criteria. In the probability section, modeled medication dosage error rates using the Binomial distribution to estimate the likelihood of five or more incorrectly prepared doses in a daily batch of 100, and applied the Poisson distribution to model complaint volume at a call center given a known hourly arrival rate.

<p align="center">
  <img src="CIND123/CIND123%20A1/survival_by_class.png" width="400">
  <br>
  <i>Figure 1: Survival rates across passenger classes, highlighting the significant advantage held by First Class passengers.</i>
</p>

<p align="center">
  <img src="CIND123/CIND123%20A1/Distribution_of_Fare_by_Sex.png" width="400">
  <br>
  <i>Figure 2: Distribution of fares paid by gender, revealing outliers and median cost differences.</i>
</p>

**Tech stack:** Python (Pandas, NumPy, Matplotlib, Seaborn, SciPy), Jupyter Notebook

**Key result:** Class 1 passengers were 2.4x more likely to survive than Class 3; binomial and Poisson models produced closed-form probability estimates validated against intuitive interpretations of the underlying processes.
* **Data Cleaning:** Successfully imputed 263 missing age values using median substitution for more accurate modeling.
---

### [Assignment 2: Regression, Correlation & Monte Carlo Simulation](./Assignment_2.ipynb)
![Individual](https://img.shields.io/badge/type-Individual-1565c0)

**Overview:** Applied inferential statistics and predictive modeling across three areas: normal distribution analysis, linear regression on academic and crime data, and Monte Carlo simulation for probability estimation.

Modeled smartphone battery life under a normal distribution, computing tail probabilities, interval probabilities, and the 5th percentile threshold using SciPy. Built a least-squares linear regression model on student grade data, visualized the regression line, and generated predictions for new midterm scores. On a North Carolina county-level crime dataset, compared two regression models predicting conviction probability using log-transformed vs. raw police per capita as predictors — finding the raw model explained 20.8% of variance vs. 14.2% for the log version — and computed Pearson correlation coefficients to assess relationships between conviction, arrest, prison sentence, and tax variables. Concluded with a Monte Carlo simulation of 100,000 trials to estimate the probability of rolling more than five even numbers in 20 die rolls, validating the result against the theoretical Binomial value with a difference of 0.0001.

<p align="center">
  <img src="CIND123/CIND123%20A2/grades_regression.png" width="400">
  <img src="CIND123/CIND123%20A2/crime_correlation_heatmap.png" width="400">
  <br>
  <i>Figure 3 & 4: (Left) Linear regression model for grade prediction; (Right) Correlation matrix of county-level crime variables.</i>
</p>

<p align="center">
  <img src="CIND123/CIND123%20A2/battery_distribution.png" width="400">
  <img src="CIND123/CIND123%20A2/monte_carlo_distribution.png" width="400">
  <br>
  <i>Figure 5 & 6: (Left) Normal distribution curve for battery life; (Right) Monte Carlo simulation results vs. theoretical Binomial PMF.</i>
</p>

**Tech stack:** Python (Pandas, NumPy, SciPy, Scikit-learn, Statsmodels, Matplotlib, Seaborn), Jupyter Notebook

**Key Result:** Successfully validated a Monte Carlo simulation against theoretical models and identified $polpc$ and $smsa$ as primary drivers of conviction probability.

* **Predictive Modeling:** Developed a least-squares regression model for grade prediction ($y = 9.58 + 0.66x$) and a crime model (polpc + smsa) explaining **20.8%** of the variance in conviction probability.
* **Simulation Accuracy:** Monte Carlo estimate ($n=100,000$) converged to within **0.01%** of the theoretical Binomial probability.
* **Statistical Significance:** Identified police per capita as a significant positive predictor ($p < 0.001$), while metropolitan area ($smsa$) was a significant negative predictor across both models.
---

## ⚠️ Limitations & Future Work

- The crime dataset regression models explain at most ~21% of variance in conviction probability, indicating significant unmodeled factors (socioeconomic conditions, judicial resources, etc.).
- Monte Carlo precision improves with trial count — the 50-run mean approach further reduces variance and could be extended to adaptive stopping criteria.
- Future work could explore multiple regression with interaction terms on the crime data to improve predictive power beyond the two-predictor models used here.

---

## 🤝 Contributing & License

Suggestions and feedback welcome — open an issue or pull request.

Licensed under the [MIT License](LICENSE).
