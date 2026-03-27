# Beyond GDP: Using PCA to Uncover the Hidden Dimensions of World Happiness

A machine learning tutorial exploring **Principal Component Analysis (PCA)** applied to the **World Happiness Report 2026** dataset (2025 rankings, 145 countries).

## Overview

What makes a country happy? The WHR measures six factors across 145 nations. This tutorial uses PCA to compress these six dimensions into two interpretable axes — revealing geographic clustering and showing that a single "Overall Wellbeing" dimension explains 77% of variance in reported happiness scores (r=0.88).


## Getting Started

### Requirements
- Python 3.8+  |  Jupyter Notebook or JupyterLab

### Installation
```bash
git clone https://github.com/guhan-ac/world-happiness-pca.git
cd world-happiness-pca
pip install pandas numpy matplotlib seaborn scikit-learn scipy openpyxl jupyter
```

### Data
Download the official dataset from the World Happiness Report:  
https://worldhappiness.report/data-sharing/  

### Run
```bash
jupyter notebook notebook.ipynb
```
Run all cells top-to-bottom. All 6 figures will be generated and saved automatically.

## Key Results

| Metric | Value |
|---|---|
| Countries | 145 (2025 rankings, WHR 2026) |
| PC1 explained variance | 47.5% — "Overall Wellbeing" |
| PC2 explained variance | 18.8% — "Generosity & Governance" |
| 2-component total | 66.2% of total variance |
| PC1 vs happiness correlation | r = 0.88, R² = 0.77 (p < 0.001) |
| Geographic clustering | Clear regional separation discovered without region labels |

## Figures

| File | Description |
|---|---|
| `fig1_correlation_heatmap.png` | Pearson correlations between the 6 WHR features |
| `fig2_scree_plot.png` | Scree plot + cumulative explained variance |
| `fig3_loadings_heatmap.png` | Feature loadings on PC1 and PC2 |
| `fig4_pca_scatter.png` | Countries in PCA space, coloured by world region |
| `fig5_pc1_vs_happiness.png` | PC1 score vs self-reported happiness (r=0.88) |
| `fig6_top_bottom_pc1.png` | Top/bottom 10 countries on the PC1 axis |

## Accessibility
- All figures use the **Okabe-Ito colour-blind-safe palette** (Wong, 2011)
- All figures include alt-text descriptions in the tutorial docx
- Notebook has detailed markdown explanations alongside every code cell
- All colour choices verified using a deuteranopia simulator

## References

1. Helliwell, J. F. et al. (2026). *World Happiness Report 2026*. University of Oxford: Wellbeing Research Centre. https://worldhappiness.report/
2. Pearson, K. (1901). On lines and planes of closest fit. *Philosophical Magazine*, 2(11), 559–572. https://doi.org/10.1080/14786440109462720
3. Hotelling, H. (1933). Analysis of a complex of statistical variables. *Journal of Educational Psychology*, 24(6), 417–441.
4. Jolliffe, I. T. (2002). *Principal Component Analysis* (2nd ed.). Springer.
5. Jolliffe, I. T., & Cadima, J. (2016). PCA: a review. *Phil. Trans. R. Soc. A*, 374(2065). https://pmc.ncbi.nlm.nih.gov/articles/PMC4792409/
6. scikit-learn (2024). *PCA documentation*. https://scikit-learn.org/stable/modules/decomposition.html#pca

## Licence
**MIT Licence** — see [LICENSE](LICENSE). Free to use, adapt, and redistribute with attribution.
