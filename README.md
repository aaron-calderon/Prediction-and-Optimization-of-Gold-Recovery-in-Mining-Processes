# Prediction-and-Optimization-of-Gold-Recovery-in-Mining-Processes

**Objective:** Develop a machine learning model that predicts the amount of gold recovered from gold ore, using data from extraction and purification processes. The model will help optimize production and eliminate unprofitable parameters.

**Tasks:**
1. *Prepare the data*
2. *Analyze the data*
3. *Build the model*

**Problem Type:**
*Supervised Regression* — We need to predict two continuous target variables:
- `rougher.output.recovery`: Gold recovery rate after the flotation stage.
- `final.output.recovery`: Gold recovery rate after the full purification process.

**Evaluation Metric:**

*sMAPE (Symmetric Mean Absolute Percentage Error):*

    sMAPE = (1/N) * Σ [ |yᵢ - ŷᵢ| / ((|yᵢ| + |ŷᵢ|) / 2) ] × 100%

The final metric combines both targets:

    sMAPE_final = 25% × sMAPE(rougher) + 75% × sMAPE(final)

This weighted formula places more importance on the final concentrate recovery.
