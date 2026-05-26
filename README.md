# 📊 data-analysis-cheatsheet

> A single-file, interactive HTML cheat sheet covering **5 types of data analysis** across **3 skill levels** — with 49 one-click copy-ready Python code blocks. No install. No dependencies. Just open in a browser.

<br>

![HTML](https://img.shields.io/badge/HTML-Single%20File-orange?style=flat-square&logo=html5)
![Python](https://img.shields.io/badge/Python-3.8%2B-blue?style=flat-square&logo=python)
![pandas](https://img.shields.io/badge/pandas-2.x-150458?style=flat-square&logo=pandas)
![License](https://img.shields.io/badge/License-MIT-green?style=flat-square)
![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen?style=flat-square)

---

## 🖥️ Preview

The cheat sheet ships as a single `eda_cheatsheet.html` file with:

- **Sidebar navigation** to switch between analysis types
- **3-level tab switcher** (Basic → Intermediate → Advanced)
- **Syntax-highlighted code blocks** with one-click copy
- **Dark theme** with colour-coded sections per analysis type
- **Responsive layout** — works on desktop and mobile

---

## 🗂️ Repository Structure

```
data-analysis-cheatsheet/
│
├── eda_cheatsheet.html     # ← The entire cheat sheet (open this)
├── README.md               # This file
└── LICENSE
```

---

## 🚀 Quick Start

```bash
# Clone the repo
git clone https://github.com/your-username/data-analysis-cheatsheet.git

# Open the cheat sheet — no server needed
cd data-analysis-cheatsheet
open eda_cheatsheet.html        # macOS
xdg-open eda_cheatsheet.html   # Linux
start eda_cheatsheet.html       # Windows
```

Or just **[download the raw HTML file](./eda_cheatsheet.html)** and open it locally.

---

## 📚 What's Covered

The cheat sheet is split into **5 analysis modules**. Each module has **Basic**, **Intermediate**, and **Advanced** tiers.

---

### 1. 🔵 Exploratory Data Analysis (EDA)

> *Understand your data before you model it.*

EDA is the first step in any data project. You inspect shape, types, distributions, relationships, and anomalies to build intuition about the dataset.

| Level | Topics Covered |
|-------|---------------|
| **Basic** | Load CSV/Excel/JSON, `.head()` / `.info()` / `.describe()`, missing values, duplicates, histogram, bar chart, boxplot, correlation heatmap |
| **Intermediate** | Full import stack, deep stats profile (skew/kurtosis/normality), all-distributions grid, missingno visualisations, KNN imputation, bivariate scatter + chi-square, IQR & Z-score outlier detection |
| **Advanced** | Memory optimisation (downcast dtypes), PCA scree plot + 2D projection, VIF multicollinearity check, Isolation Forest + UMAP anomaly visualisation, ydata-profiling & Sweetviz automated reports |

**Key Libraries:** `pandas` `numpy` `matplotlib` `seaborn` `missingno` `scipy` `sklearn` `umap-learn` `ydata-profiling` `sweetviz`

---

### 2. 🟣 Inferential Analysis

> *Draw statistically valid conclusions from sample data.*

Inferential statistics lets you go beyond your dataset — testing hypotheses, measuring effect sizes, and estimating population parameters from samples.

| Level | Topics Covered |
|-------|---------------|
| **Basic** | Import block, one-sample t-test, two-sample Welch t-test, paired t-test, Pearson correlation, Spearman correlation |
| **Intermediate** | One-Way ANOVA + Tukey HSD post-hoc, Mann-Whitney U test, Kruskal-Wallis test, t-distribution confidence intervals, bootstrap CI |
| **Advanced** | OLS regression (statsmodels formula API + residual diagnostics), Cohen's d effect size, power analysis (minimum sample size), Bonferroni & Benjamini-Hochberg multiple testing correction |

**Key Libraries:** `scipy.stats` `statsmodels` `numpy`

---

### 3. 🟢 Cluster Analysis

> *Find natural groupings without labelled data.*

Clustering is unsupervised segmentation — grouping similar observations without prior labels. Used for customer segmentation, anomaly detection, topic modelling, and more.

| Level | Topics Covered |
|-------|---------------|
| **Basic** | StandardScaler, K-Means, elbow method (inertia plot), cluster label assignment |
| **Intermediate** | Silhouette score sweep to pick best k, Davies-Bouldin score, DBSCAN (density-based), hierarchical clustering with dendrogram, fcluster, cluster profile heatmap (Z-scored means) |
| **Advanced** | Gaussian Mixture Models (GMM) with BIC model selection, soft membership probabilities, UMAP 2D cluster visualisation |

**Key Libraries:** `sklearn` `scipy.cluster.hierarchy` `umap-learn` `seaborn`

---

### 4. 🟠 Time Series Analysis

> *Understand and forecast patterns over time.*

Time series data has temporal structure — trend, seasonality, cycles, and noise. This module covers everything from loading date-indexed data to production forecasting.

| Level | Topics Covered |
|-------|---------------|
| **Basic** | Parse dates, set DatetimeIndex, resample (D/W/M/Q), rolling mean + std band, exponentially weighted moving average (EWM) |
| **Intermediate** | ADF + KPSS stationarity tests, differencing & log-transform to achieve stationarity, STL decomposition (trend + seasonal + residual), ACF & PACF plots for ARIMA order selection |
| **Advanced** | Auto-ARIMA order selection (`pmdarima`), SARIMA 12-step forecast with confidence interval band, Facebook Prophet forecast with changepoints, yearly + weekly seasonality components |

**Key Libraries:** `pandas` `statsmodels` `pmdarima` `prophet` `matplotlib`

---

### 5. 🩷 Cohort Analysis

> *Track user behaviour across acquisition cohorts over time.*

Cohort analysis groups users by their first event (e.g. sign-up or first purchase month) and tracks how their behaviour changes over subsequent periods. Essential for product, growth, and retention analytics.

| Level | Topics Covered |
|-------|---------------|
| **Basic** | Build cohort table (cohort month + period index), pivot to cohort matrix, retention rate heatmap |
| **Intermediate** | Cumulative per-user LTV curves by cohort, average retention curve across all cohorts |
| **Advanced** | Kaplan-Meier survival curve, log-rank test to compare cohort survival, Cox Proportional Hazards model (hazard ratios per feature, predict median survival) |

**Key Libraries:** `pandas` `seaborn` `lifelines`

---

## 🔧 Python Requirements

```bash
pip install pandas numpy matplotlib seaborn scipy statsmodels scikit-learn
pip install missingno ydata-profiling sweetviz
pip install umap-learn pmdarima prophet lifelines
```

> **Python 3.8+** recommended. All code blocks are written for pandas 2.x.

---

## 🎨 Design & Features

| Feature | Detail |
|---------|--------|
| Theme | Dark (`#07080f` base), colour-coded per analysis type |
| Font | IBM Plex Mono (code) + Fraunces (headings) |
| Navigation | Sticky sidebar with 5 analysis types |
| Level switcher | Basic / Mid / Adv tabs — shows only the relevant tier |
| Copy buttons | Every code block has a one-click copy button |
| Responsive | Hamburger sidebar on mobile viewports |
| No dependencies | Pure HTML + CSS + vanilla JS — zero npm, zero bundler |

---

## 📖 How to Use

1. **Pick an analysis type** from the sidebar (EDA, Inferential, Cluster, Time Series, Cohort)
2. **Select your level** using the tabs at the top of the sidebar (Basic / Mid / Adv)
3. **Read the heading** above each code block — it describes exactly what the code does
4. **Click COPY** to copy any code block to clipboard
5. **Paste into your notebook** or `.py` file and adapt column names

---

## 🗺️ Roadmap

- [ ] Text / NLP Analysis module
- [ ] Geospatial Analysis module  
- [ ] A/B Testing module
- [ ] Dark/Light theme toggle
- [ ] Search bar across all code blocks
- [ ] Jupyter Notebook versions of each section

---

## 🤝 Contributing

Contributions are welcome! If you'd like to add a new analysis type, fix a bug, or improve a code block:

```bash
# 1. Fork the repo
# 2. Create a branch
git checkout -b feature/add-nlp-module

# 3. Make your changes to eda_cheatsheet.html
# 4. Open a pull request
```

Please keep code blocks **self-contained**, **well-commented**, and consistent with the existing style.

---

## 📄 License

This project is licensed under the **MIT License** — see the [LICENSE](./LICENSE) file for details.  
Free to use, modify, and distribute. Attribution appreciated but not required.

---

## ⭐ If This Helped You

Give it a star — it helps others find the repo.

```
git clone https://github.com/your-username/data-analysis-cheatsheet.git
```

---

<div align="center">

Made for data scientists, analysts, and anyone who forgets how to run a Kaplan-Meier at 2am.

**pandas · scipy · sklearn · statsmodels · seaborn · prophet · lifelines**

</div>
