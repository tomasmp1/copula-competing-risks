# Modeling Competing Risks Using Copulas

This project demonstrates the application of **copulas**, specifically the **Clayton copula**, in modeling **competing risks** within time-to-event data. It simulates dependent failure times representing **loan repayment** and **loan default**, fits marginal distributions, and estimates copula dependence parameters using **maximum likelihood estimation (MLE)** and **bootstrap resampling**.

---

## Key Insights

- **Clayton copula captures lower tail dependence**, modeling scenarios where early failure in one process increases the likelihood of failure in the other.  
- **Exponential marginals provide a strong fit** for both repayment and default times, supported by AIC-based model selection and Q-Q validation.  
- **MLE performs accurately**, recovering true parameter values for both the copula and marginals under controlled synthetic conditions.  
- **Bootstrap inference quantifies uncertainty**, providing sampling distributions for all estimated parameters.

---

## Repository Contents

- `notebooks/`
  - `copula-competing-risks.Rmd` : Full analysis notebook with code, results, and commentary  
  - `copula-competing-risks.html` : Rendered output with figures and discussion  
- `README.md` : This file

---

## Getting Started

1. **Open the notebook** in **RStudio** or any R Markdown-compatible environment.  
2. Ensure all required R packages are installed: `copula`, `fitdistrplus`, `survival`, and `ggplot2`.  
3. Knit the `.Rmd` file to **HTML** to reproduce the complete analysis, figures, and discussion.  

**No additional setup is required.** All code, data handling, and analysis are included in the notebook.

---

## Notebook Overview

| Section | Description |
|----------|-------------|
| Data Generation | Simulates dependent time-to-event data for loan repayment and default using a Clayton copula, with visualisations of dependence and event-time distributions |
| Fit Marginals | Fits candidate distributions to each event type, evaluates AIC for model selection, and visualises Q–Q plots of fitted marginals |
| Estimate Parameters | Performs maximum likelihood estimation of copula and marginal parameters, applies bootstrap resampling for uncertainty assessment, and visualises parameter distributions |
| Discussion | Interprets results, summarises simulation design and key findings, compares MLE, bootstrap, and true values, and concludes with implications for copula-based competing risk modelling |
