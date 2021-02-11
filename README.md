## From Hydrometeorology to River Water Quality: Can a Deep Learning Model Predict Dissolved Oxygen at the Continental Scale?

**Zhi, W.**, Feng, D., Tsai, W. P., Sterle, G., Harpold, A., Shen, C., & Li, L. (2021). From Hydrometeorology to River Water Quality: Can a Deep Learning Model Predict Dissolved Oxygen at the Continental Scale?. *Environmental Science & Technology*. [10.1021/acs.est.0c06783](https://doi.org/10.1021/acs.est.0c06783)

## Abstract
<p align="center">
  <img src="/figures/TOC.png" alt="Study site: Coal Creek Watershed" width="700">
</p>

- Dissolved oxygen (DO) reflects river metabolic pulses and is an essential water quality measure. Our capabilities of forecasting DO however remain elusive. 
- Water quality data, specifically DO data here, often have large gaps and sparse areal and temporal coverage. Earth surface and hydrometeorology data, on the other hand, have become largely available. 
- Here we ask: can a **Long Short-Term Memory (LSTM)** model learn about river DO dynamics from sparse DO and intensive (daily) hydrometeorology data? We used **[CAMELS-chem](https://github.com/WeiZhiWater/CAMELS-Chem-DO-dataset)**, a new data set with DO concentrations from 236 minimally disturbed watersheds across the U.S. 
- The model generally learns the theory of DO solubility and captures its decreasing trend with increasing water temperature. It exhibits the potential of predicting DO in “**chemically ungauged basins**”, defined as basins without any measurements of DO and broadly water quality in general.
- Results suggest that more data collections at DO peaks and troughs and in sparsely monitored areas are essential to overcome the issue of data scarcity, an outstanding challenge in the water quality community.

## Figures
- DO records and model performance map
- Model performance in reproducing in reproducing temporal DO dynamics 
- Model performance in reproducing concentration-discharge (C−Q) relationships
- Model performance in reproducing concentration−temperature (C-T) relationships
- Deep learning model training insights: relationships between model performance and watershed predictors

### DO records and model performance map
Mean DO concentrations (Figure 1b) generally are higher at higher latitude, with the highest (11−12 mg/L) in the Northeast andNorthwest. The lowest mean DO occurs in Florida and is surprisingly low (i.e., 4−5 mg/L) for these minimally disturbed watersheds, close to the hypoxia limit of 3 mg/L. DO variations (Figure 1c) are generally lower in the west compared to the east. For the core evaluation group of 84 sites, the model achieved satisfactory performance (NSE≥0.4) for 74% of the sites, and a mean (median) NSE, RMSE, and Pcorr of 0.51 (0.57), 1.2 (1.1), and 0.78 (0.82) mg/L, respectively.

<p align="center">
  <img src="/figures/DO map.png" alt="DO map" width="800">
</p>

### Model performance in reproducing in reproducing temporal DO dynamics 
A detailed look further confirms that the model captures the seasonal dynamics across diverse conditions (Figure 2), despite large data gaps that have challenged the training process. In general, the model covers the bulk variation of DO concentrations from 5 to 15 mg/L. The model does miss DO peaks and troughs in some cases. Although a few occasional mismatches at extreme concentrations may have a limited impact on NSE values when data are abundant (Figure 2c, g), they could lead to a large penalty in basins with few data points in the testing period (e.g., low performance group, Figure 2k).

<p align="center">
  <img src="/figures/figure 2.png" alt="temporal DO dynamics" width="800">
</p>

### Model performance in reproducing concentration-discharge (C−Q) relationships
Concentration−discharge (C−Q) relationships are often used to understand the response of solute concentrationto changing streamflow and offer clues about catchment structure and biogeochemical processes. Figure 3 shows that the good and fair performance occur when the model captures the full range of DO levels (left and middle columns). Low performance occurs when the model misses the peaks and troughs. The C−Q relationship figure also indicates that DO measurements occur mostly in low to intermediate−high discharge regimes, covering 70−80% on logQ but often miss the concentrations at high Q regimes that could largely shape C−Q patterns.

<p align="center">
  <img src="/figures/CQ_figure.png" alt="C-Q figure" width="700">
</p>

### Model performance in reproducing concentration−temperature (C-T) relationships
Temperature controls DO solubility and biological activitiesin water and often drives DO variations. The figure shows that formost sites, the model (red dots) can learn the DO solubility theory and reproduce at least part of the concentration versus temperature curves (Figure 4). The performance is typically better under low T conditions. At higher T conditions, DO levels often drop to levels lower than the solubility prediction (Figure 4, middle row). This is expected as in-steam biological processes can be active under high T conditions. At some sites (Figure 4, top row), the DO data follow the prediction lines at all Tranges, indicating minimal biological activities. At someother sites (Figure 4, bottom row), DO can be much higher than the solubility line, indicating significant photosynthesis in streams. 

<p align="center">
  <img src="/figures/CT_figure.png" alt="C-T figure" width="700">
</p>

<p align="center">
  <img src="/figures/figure 5.png" alt="correlations" width="800">
</p>
