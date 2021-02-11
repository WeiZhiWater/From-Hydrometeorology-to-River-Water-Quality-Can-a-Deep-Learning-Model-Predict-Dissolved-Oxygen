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


<p align="center">
  <img src="/figures/DO map.png" alt="DO map" width="800">
</p>

<p align="center">
  <img src="/figures/figure 2.png" alt="temporal DO dynamics" width="800">
</p>

<p align="center">
  <img src="/figures/CQ_figure.png" alt="C-Q figure" width="700">
</p>

<p align="center">
  <img src="/figures/CT_figure.png" alt="C-T figure" width="700">
</p>

<p align="center">
  <img src="/figures/figure 5.png" alt="correlations" width="800">
</p>
