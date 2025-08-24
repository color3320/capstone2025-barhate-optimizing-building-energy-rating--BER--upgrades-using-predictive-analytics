# Optimizing Building Energy Rating (BER) Upgrades using Predictive Analytics

This thesis builds a practical pipeline to **predict BER, CO₂ emissions, and envelope U-values** from **partial homeowner inputs**, combining typed preprocessing with **imputation** (Median, Bayesian MICE, MissForest, Denoising Autoencoder) and **LightGBM** for multi-output regression. In tests, **DEAP-inspired features** improved accuracy; **MissForest** generally provided the strongest imputations; and **multi-output LightGBM** matched or slightly beat chained regressors while being simpler to deploy. The approach supports fast, credible estimates to guide retrofit decisions under real-world missingness.

> Since all work was done locally, I just uploaded the **best version of the code**.

---

## Figure
<p align="center">
  <img src="https://drive.google.com/uc?export=view&id=1zB4zh0RqXk-fdiXvca9Lr7GNP0Wrw_Cq" alt="Thesis figure or workflow" />
</p>

---

## Highlights
- **Targets:** BER, CO₂, U-values (walls/roof/floor/windows/doors).  
- **Imputation:** Median, **MICE (Bayesian Ridge)**, **MissForest (Extra Trees)**, **DAE**.  
- **Models:** **LightGBM** (multi-output) vs. **RegressorChain**.  
- **Key findings:** Feature engineering helps; **MissForest** imputation is most consistent; multi-output LightGBM is accurate and simple to serve.

