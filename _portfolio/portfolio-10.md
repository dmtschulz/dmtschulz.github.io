---
title: "Ensemble Learning from Scratch"
excerpt: "Manual implementation of decision trees, random forests, and boosting. <br/><img src='https://raw.githubusercontent.com/dmtschulz/grow-your-own-forest/main/plots/random_forest_boundary.png' width='250'>"
collection: portfolio
---

### Ensemble Learning

This project demonstrates hand-built implementations of common ensemble methods in machine learning:

- ✅ Random Forest Classifier (majority voting)
- ✅ Random Forest Regressor (average prediction)
- ✅ Boosted Tree Regressor (sequential residual learning)

All models were evaluated on real datasets like Iris, Bodyfat, and Diabetes.  
Focus was placed on understanding **bias-variance tradeoffs**, **model complexity**, and **generalization behavior**.

**Key Highlights:**
- Built from scratch using base `DecisionTree` models
- Benchmarked using R² and accuracy across multiple seeds
- Depth-vs-performance visualizations
- Decision boundary plots for classification

**Tools**: Python, NumPy, Scikit-learn, Matplotlib

Check out the [GitHub repository](https://github.com/dmtschulz/grow-your-own-forest).

Decision boundary with 100 trees:
![Decision Boundary](https://raw.githubusercontent.com/dmtschulz/grow-your-own-forest/main/plots/random_forest_boundary.png)

R² score vs depth:
![Depth vs R²](https://raw.githubusercontent.com/dmtschulz/grow-your-own-forest/main/plots/depth_vs_r2_bodyfat.png)
