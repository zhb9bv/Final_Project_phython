# Final Project - Particle Physics Event Classification
By Emma Cucca
## Dataset Description
This data set contains simulated particle collision events with features describing kinematic 
Each event is labeled as signal or background.

- Missing values are encoded as -999
- Each row = one collision event
- Columns = kinematic features (mass, momentum, angle, etc.)
- Label = “s” (signal) or “b” (background)


## Contents
- Rows: 250,001
- Columns: 33 (including EventId, Weight, and Target)
- Target: Target ∈ {s, b}
- Weight: continuous; use as sample_weight in training and evaluation

## Main Question
I investigated the following question: Which kinematic features show thew strongest difference between the signal and background events?

## Summary of findings
Signal and background distributions differ most strongly in variables like **DER_deltaeta_jet_jet** and **DER_mass_MMC**.
I used Cohen's d effect size to compute the seperation strength between signal and background (distance between peaks). I also computed a scatter plot for PRI_tau_pt and PRI_lep_pt which showed no corelation. I confirmed this by fitting a linear regression model and the metric indicated Tau pT does not strongly predict lepton pT using a linear model. I wrote this code early on when analyzing my dataset. Overall, the dataset shows measurable separation between signal and background. This analysis confirms that these kinematic features are strong candidates for building an effective binary classifier.
