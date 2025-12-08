# Bias Audit: Logistic Regression on Adult Dataset

## 📊 Project Overview
This project audits bias in a Logistic Regression model trained on the UCI Adult dataset.  
The target is **income ≥ 50K**, with **sex (Male vs Female)** as the sensitive attribute, and **education level** as the feature of interest.

## 🎯 Goals
- Train a baseline model and measure accuracy.
- Audit fairness metrics across Male vs Female.
- Explore intersectional fairness (sex × education).
- Apply bias mitigation (demographic parity).
- Compare fairness metrics before vs after mitigation.

## ⚙️ Methods
- **Model**: Logistic Regression (scikit-learn).
- **Fairness metrics**: Selection rate, true positive rate, demographic parity difference (Fairlearn).
- **Mitigation**: ExponentiatedGradient with DemographicParity constraint.

## 📈 Results
- **Baseline accuracy**: ~0.844
- **Bias findings**:
  - Male group had higher selection rate for income ≥ 50K.
  - Women with the same education level as men were predicted less often as high income.
- **Mitigation results**:
  - Demographic parity difference reduced after applying fairness constraints.
  - Selection rates across groups became more balanced.

## 🖼️ Visualizations
- Fairness metrics by sex.
- Fairness metrics by sex × education.
- Selection rate comparison before vs after mitigation.

## ✅ Conclusion
The audit shows that the baseline model exhibits gender bias, especially within education levels.  
Applying fairness constraints improves parity, though at some cost to accuracy.  
This demonstrates the importance of auditing and mitigating bias in predictive models.

   ```
