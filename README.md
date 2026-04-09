\# Lithium-ion Battery SOH Estimation using WOA-CNN-LSTM



\## Overview



This project develops a data-driven framework for estimating the State of Health (SOH) of lithium-ion batteries using deep learning and metaheuristic optimization. The approach combines Convolutional Neural Networks (CNN), Long Short-Term Memory (LSTM), and the Whale Optimization Algorithm (WOA) to improve prediction accuracy on battery degradation data.



\## Dataset



The model is evaluated on the NASA Prognostics Center of Excellence lithium-ion battery dataset (B0005, B0006, B0007), which contains charge–discharge cycle data.



Download dataset:

https://ti.arc.nasa.gov/tech/dash/groups/pcoe/prognostic-data-repository/



Place data in:



```

data/raw/

```



\## Methodology



The workflow consists of:



\* Extraction of four health factors (HF1–HF4) from charge/discharge cycles

\* Outlier detection using Local Outlier Factor (LOF)

\* Data cleaning via linear interpolation

\* Correlation analysis (Pearson and Spearman) for feature validation

\* Model development and comparison:



&#x20; \* Plain LSTM (baseline)

&#x20; \* CNN-LSTM

&#x20; \* WOA-optimized CNN-LSTM



The CNN layers extract local features, while LSTM captures temporal dependencies. WOA is used to optimize hyperparameters such as learning rate, hidden size, batch size, and dropout.



\## Results



The WOA-CNN-LSTM model consistently outperforms baseline models across all batteries.



\* Significant reduction in RMSE, MAE, and MAPE

\* Up to \~90% improvement over Plain LSTM

\* Accurate tracking of battery degradation trends



\## Repository Structure



\* `src/` → model implementation

\* `data/` → dataset (or download instructions)

\* `figures/` → report figures

\* `report/` → LaTeX source files

\* `results/` → plots and evaluation outputs



\## How to Run



```

pip install -r requirements.txt

python src/main.py

```



\## Limitations



\* Evaluated on only three batteries

\* Tested on laboratory data only (no real-world validation)



\## Author



Elahe Salimi

Pardis Ahmadzadeh



