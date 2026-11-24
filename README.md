# Bias, Variance and an Unbiased Cross-Validation Score

## Objective

I aimed to understand the bias-variance tradeoff and compare different cross-validation methods for estimating prediction error.

## Methodology

- I performed cross-validation on polynomial models of degrees 1 to 12 using 80 simulated data points.
- I selected the polynomial degree with the lowest cross-validation error.
- I evaluated the selected model on 20,000 new simulated data points.
- I used nested cross-validation to estimate prediction error separately from model selection.
- I decomposed the expected prediction error into squared bias, variance, and noise through simulation.
- I wrote my own k-fold cross-validation function for scikit-learn models and compared its results with the lab results.

## Key Findings

I selected degree 5, which had a cross-validation error of 0.1853. However, its true error estimated using new data was higher at 0.2330. Nested cross-validation estimated an error of 0.1910, which was closer to the true error.

The bias-variance decomposition showed that the noise alone was 0.2025. My own cross-validation function produced an error of 0.1921 for degree 5 using 10 folds.

Overall, I found that selecting a model based on the lowest cross-validation error can lead to an overly optimistic estimate of its prediction performance.
