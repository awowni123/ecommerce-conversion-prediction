# E-Commerce Conversion Prediction & Behavioral Analysis

Customer behavior analysis and purchase conversion prediction using **Python, Pandas, Scikit-learn, Matplotlib, and Seaborn**.

## Dataset

- 12,330 original shopping sessions
- 12,205 unique sessions after removing duplicates
- 17 predictor variables
- Target: `Revenue` (purchase / no purchase)
- Conversion rate: **15.63%**

## Key Insights

- New visitors converted at **24.93%** vs **14.09%** for returning visitors.
- Converting sessions viewed a median of **29 product pages** vs **16** for non-converters.
- Converters spent about **2.1× more time** on product-related pages.
- Non-converters had about **4.5× higher bounce rates** and **2.3× higher exit rates**.
- November had the highest conversion rate at **25.49%**.

## Model

Built an interpretable **Logistic Regression** model with:

- One-hot encoding
- StandardScaler
- Stratified train-test split
- Class-weight comparison
- Precision, Recall, F1-score, ROC-AUC
- Threshold analysis
- Feature coefficient interpretation

### Standard Logistic Regression
- Accuracy: **88.78%**
- Precision: **75.71%**
- Recall: **41.62%**
- F1-score: **53.72%**
- ROC-AUC: **89.97%**

### Balanced Logistic Regression
- Precision: **50.92%**
- Recall: **79.58%**
- F1-score: **62.10%**
- ROC-AUC: **90.96%**

A **0.30 prediction threshold** gave a better precision-recall balance:
- Precision: **67.88%**
- Recall: **58.64%**
- F1-score: **62.92%**

## Feature Insights

- `PageValues` was the strongest positive predictor.
- Higher `ExitRates` were strongly associated with lower conversion.
- Removing `PageValues` reduced ROC-AUC from about **0.91 to 0.76**, showing its strong predictive importance.

## Business Takeaways

- Target high-intent sessions with low-cost personalized interventions.
- Investigate highly engaged users who still do not purchase.
- Reduce exit behavior around key product and checkout pages.
- Use seasonal conversion patterns to guide campaign timing.

## Project Structure

```text
data/
images/
notebooks/
README.md
