# fMRI

## ABIDE-I NYU Resting-State fMRI Functional Connectivity Features

This repository provides precomputed resting-state functional connectivity (FC) features from the **NYU site of the ABIDE-I dataset** for autism spectrum disorder (ASD) classification.

The functional connectivity features were constructed from ROI-wise resting-state fMRI time series based on the **AAL atlas**. For each subject, pairwise Pearson correlation coefficients were calculated between all ROI time series to obtain an FC matrix. The correlation coefficients were then transformed using the Fisher \(z\)-transformation, and the **upper triangular elements of the FC matrix, excluding the diagonal**, were vectorized as the final FC features.

The dataset is provided as:

`ABIDE_NYU_fc_features.csv`

### Data format

- The **first column**, `sample_id`, contains the subject identifier.
- The intermediate columns contain the vectorized functional connectivity features.
- The **last column**, `label`, contains the diagnostic label:
  - `1`: Autism Spectrum Disorder (ASD)
  - `0`: Healthy Control (HC)

If the AAL atlas contains 116 ROIs, the number of pairwise functional connectivity features is:

\[
\frac{116\times115}{2}=6670
\]

