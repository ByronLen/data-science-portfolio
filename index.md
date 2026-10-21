---
layout: default
title: "Data Science Portfolio"
---

# Byron

<!-- Confirm the student identity and personal focus before publication. -->
Data science student interested in reproducible analysis and clear communication.

[GitHub](https://github.com/ByronLen) | [Project repository](https://github.com/ByronLen/data-science-project) | [Live site — pending deployment](https://ByronLen.github.io/data-science-portfolio/)

## About

<!-- Neutral default supplied by the brief; confirm or replace with your own background. -->
I am a data science student interested in reproducible analysis and clear communication.

## Skills

<!-- These are tools and methods demonstrated in this project, not a claim of professional proficiency. -->
- **Programming:** Python.
- **Data analysis:** pandas, NumPy, data cleaning, exploratory data analysis, model evaluation, scikit-learn.
- **Visualization:** Matplotlib, Seaborn.
- **Tools:** Git/GitHub; GitHub Pages/Jekyll (this site; deployment pending).

## Penguin Morphometrics: Can Four Measurements Identify a Species?

Analysis complete · 3 visualizations · Peer review: Planned

### Purpose

Can bill length, bill depth, flipper length, and body mass distinguish Adelie, Chinstrap, and Gentoo penguins? Comparing these measurements makes it possible to examine variation among species and individuals, then contrast descriptive differences with held-out prediction. This reproducible example shows why strong classification still needs careful limits.

### Data

Palmer Penguins contains 344 observations collected by Kristen Gorman and Palmer Station LTER on three Antarctic islands during 2007–2009; the data are CC0 and an offline copy is included in the [project repository](https://github.com/ByronLen/data-science-project).

### Methods

- Validate the schema, convert four measurement columns to numeric, and remove two incomplete rows, leaving 342 complete-case observations; no mean imputation.
- Summarize distributions by species and calculate overall and within-species Pearson correlations; use descriptive eta-squared to compare measurement separation on those 342 observations.
- Use only bill length, bill depth, flipper length, and body mass in a StandardScaler + LogisticRegression pipeline with a stratified 75/25 split (256 training, 86 test; random_state=42).
- Run five-fold stratified cross-validation on the training set only; fit preprocessing within each fold and report test accuracy, macro F1, per-class metrics, and confusion counts without test-based tuning.

### Findings

- Gentoo mean body mass is 5076.016 g versus 3700.662 g (Adelie) and 3733.088 g (Chinstrap); its mean bill depth is 14.982 mm versus 18.346 and 18.421 mm, respectively.
- Adelie and Chinstrap mean bill lengths differ (38.791 versus 48.834 mm), while both have median body mass 3700.000 g. Flipper length has the strongest descriptive separation (eta-squared 0.778); distributions still overlap.
- Test accuracy and macro F1 are both 1.000 on 86 observations, with zero errors and therefore no dominant confusion pair. Training-only cross-validation accuracy is 0.980 ± 0.012.
- Flipper length versus mass has overall r=0.871 versus 0.468 (Adelie), 0.642 (Chinstrap), and 0.703 (Gentoo). Bill versus flipper length has overall r=0.656 versus 0.326 (Adelie), 0.472 (Chinstrap), and 0.661 (Gentoo): pooled correlation is not always greater than every within-species correlation.

### Limitations

- Only three species, three islands, and 2007–2009 are represented. There are 342 complete-case observations and only 68 Chinstrap records; results do not generalize to all penguins or later years.
- These observational data cannot explain causes or isolate environmental, sex, or age effects. High accuracy demonstrates distinguishability rather than biological importance.
- One holdout split can vary; training-only cross-validation only partly addresses this, and there is no external validation set.

[Project repository](https://github.com/ByronLen/data-science-project) · [Project README](https://github.com/ByronLen/data-science-project/blob/main/README.md) · [Dataset page](https://allisonhorst.github.io/palmerpenguins/) · [Dataset DOI](https://doi.org/10.5281/zenodo.3960218)

## Figures

<p align="center">
  <img src="assets/img/01_measurements_by_species.png"
       alt="Box plots and individual observations compare bill length, bill depth, flipper length, and body mass across Adelie, Chinstrap, and Gentoo penguins, with complete-case sample counts."
       width="100%">
</p>
<p><em>Figure 1. Gentoo has greater body mass and shallower bills on average, while Adelie and Chinstrap overlap in mass and bill depth.</em></p>

<p align="center">
  <img src="assets/img/02_bill_vs_flipper.png"
       alt="Bill length versus flipper length for three penguin species, with a named legend and separate linear fits; Gentoo generally has longer flippers and Adelie overlaps with Chinstrap."
       width="100%">
</p>
<p><em>Figure 2. Species-specific fits reveal positive within-species associations and overlap; pooled association also reflects species differences and does not establish causation.</em></p>

<p align="center">
  <img src="assets/img/03_confusion_matrix.png"
       alt="Confusion matrix with true species on rows and predicted species on columns: 38 Adelie, 17 Chinstrap, and 31 Gentoo predictions are correct, with zero off-diagonal errors."
       width="100%">
</p>
<p><em>Figure 3. All 86 held-out observations are classified correctly in this fixed split; perfect accuracy here does not establish performance on external populations.</em></p>
