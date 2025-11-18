---
title: "Projects"
---

## Selected Projects

### Multinomial Modeling for Cognitive Impairment Classification  
**HRS-HCAP & Mex-Cog | Michigan ISR**

This project shaped how I think about model specification and diagnostics in real-world classification.  
The outcome had **three categories** with **asymmetric separation** and **overlapping covariate distributions**, which made simple multinomial models misleading.

I iteratively compared:

- Multinomial logistic regression  
- Proportional odds & partial-proportional odds  
- Adjacent-category ordinal models  

What I learned was that **model fit was not the main difficulty**—  
**identification** and **overlap** were.

I used:

- graphical overlap checks  
- multinomial residual patterns  
- class-conditional density comparisons  
- sensitivity to imbalance reweighting  

My takeaway: *classification in aging data is essentially a problem of latent structure & restricted support*, not algorithm choice.  
This changed the way I read MCI papers and influenced how I design future models.

---

### High-Dimensional Behavioral Dynamics (Digital Cages Project)  
**Sparse PCA (NExOS), Clustering, Feature Engineering | Michigan**

This dataset had **millions of observations per mouse**, strong temporal autocorrelation, and extremely noisy high-dimensional features.  
The question was simple: *can we recover interpretable behavioral states?*  
Statistically，这变成了：

- a **dimension reduction** challenge  
- a **signal extraction** challenge  
- a **temporal smoothing** challenge  

I implemented:

- PCA → noisy  
- Sparse PCA (NExOS) → interpretable axes  
- k-means & hierarchical clustering → behavioral motifs  
- rolling-window variance features → circadian structure  

The insight:  
**Sparse PCA produced axes aligned with biologically meaningful patterns** (activity, exploration, resting).  
This made me appreciate sparsity not as a mathematical constraint but as a way to *induce interpretability in messy empirical systems*.

---

### Causal Effect of Oral Health on Hearing (NHANES)  
**TMLE, Doubly Robust Estimation, Overlap Diagnostics**

This project taught me to be suspicious—**deeply suspicious**—of causal conclusions drawn from national surveys.

Instead of running a “quick logit,” I analyzed:

- propensity-score overlap  
- trimming thresholds  
- weight truncation  
- AIPW vs TMLE agreement  
- covariate imbalance under positive/partial overlap  

A key experience was identifying **partial-overlap regimes** where estimates flipped sign or inflated.  
This made me realize that *diagnostics are not the first step—they are the entire step*.

Deliverable: a reproducible, one-click pipeline for effect estimation + a negative results note (which I’m proud of).

---

### Time-Series Effects in Bike-Share Demand  
**Poisson → NB → GAM → Mixed Models | Model Ladder Philosophy**

This project reflects my modeling philosophy:  
**start simple, diagnose, escalate only when forced.**

Beginning with a Poisson GLM, the dispersion and residual patterns made the inadequacy clear.  
The ladder went:

1. Poisson  
2. Quasi-Poisson  
3. Negative Binomial  
4. GAM spline on time  
5. Mixed effects with weekday/month random intercepts  

Instead of reporting “the best model,”  
I analyzed **what changed and why**:  
the GAM smoothed out weekday anomalies; NB reduced dispersion inflation; mixed models captured persistent heterogeneity.

Ultimately, the model “improvement” was not the new RMSE—it was **understanding where the Poisson assumptions break in temporal count data**.

---

### Bayesian Hierarchical Modeling of Work Patterns  
**rstan, hierarchical priors, MCMC diagnostics**

This project fundamentally shifted how I view Bayesian computation.  
Instead of tweaking priors, the real work was:

- diagnosing divergent transitions  
- adapting step size  
- reparameterizing  
- monitoring R-hat, ESS  
- validating with LOO-CV  

My largest gain wasn't technical—it was conceptual:  
**good Bayesian models are built backwards—from diagnostics and computational stability to the likelihood—not the other way around.**
