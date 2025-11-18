---
title: "Methods"
---

## My Approach to Statistical Modeling

My methods background is broad, but how I *use* methods matters more to me than the list of techniques.  
Below I summarize not what I know, but **how I think about problems**.

---

### **1. Diagnostics First**
I design models from diagnostics backward.  
Overlap, residuals, leverage, calibration, and identifiability determine model choice—not the other way around.

This came from working with cognitive impairment classification, where *model failure taught me the structure of the data*.

---

### **2. Semiparametric Thinking**
I gravitate toward methods that keep interpretability while allowing flexibility:

- GAMs  
- shape-constrained estimation  
- sparse PCA  
- partial-proportional odds models  

I like methods that refuse to pretend the world fits into simple parametric boxes.

---

### **3. High-Dimensional Structures**
Working with Digital Cages data made me appreciate sparsity and clustering—not as machine learning tricks, but as **scientific tools for structure recovery**.

I use:

- PCA / Sparse PCA (NExOS)  
- hierarchical clustering  
- feature extraction for time-series signals  

---

### **4. Causal Inference as a Discipline of Skepticism**
NHANES taught me that causal inference is 90% diagnostics, 10% estimation.

My workflow always includes:

- overlap checks  
- truncation regimes  
- AIPW vs TMLE triangulation  
- sensitivity to positivity violations  

---

### **5. Bayesian Modeling with Engineering Discipline**
I see Bayesian inference as modeling + computation:

- prior specification  
- model reparameterization  
- MCMC stability (R-hat, ESS, divergences)  
- LOO-CV & posterior predictive checks  

The hierarchical work hour project solidified this computational mindset.

---

### **6. Measurement Modeling & Latent Structure**
My applied work in cognitive aging requires:

- CFA  
- invariance testing  
- domain scoring  
- WLSMV modeling

This shaped how I think about latent variables and empirical identifiability.

---

### **7. Reproducibility as a Method**
Most of my projects involve full pipelines:
- fixed seeds  
- environment control  
- knitted R Markdown / Quarto  
- multi-step data engineering scripts  

I aim for statistical analyses that can be reproduced **exactly**, not approximately.

---
