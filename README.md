# 🔋 Lithium-ion Battery SOH Estimation using WOA-CNN-LSTM

---

## **📌 Overview**

This project presents a **data-driven framework** for estimating the **State of Health (SOH)** of lithium-ion batteries using a hybrid deep learning architecture. The proposed approach integrates:

* **Convolutional Neural Networks (CNN)** for feature extraction
* **Long Short-Term Memory (LSTM)** for temporal modeling
* **Whale Optimization Algorithm (WOA)** for hyperparameter optimization

The objective is to achieve **high-accuracy SOH prediction** while maintaining computational efficiency for real-world **Battery Management Systems (BMS)**.

---

## **📂 Dataset**

The model is evaluated on the **NASA Prognostics Center of Excellence (PCoE)** lithium-ion battery dataset:

* Batteries: **B0005, B0006, B0007**
* Data type: Charge–discharge cycle measurements

🔗 **Official Source:**
https://phm-datasets.s3.amazonaws.com/NASA/5.+Battery+Data+Set.zip

---

## **⚙️ Methodology**

### **1. Feature Engineering**

* Extraction of **four health factors (HF1–HF4)** from raw signals
* Captures key degradation characteristics

### **2. Data Preprocessing**

* **Outlier detection:** Local Outlier Factor (LOF)
* **Data cleaning:** Linear interpolation
* **Validation:** Pearson & Spearman correlation analysis

### **3. Model Architectures**

* **Baseline:** Plain LSTM
* **Hybrid:** CNN-LSTM
* **Optimized:** WOA-CNN-LSTM

### **4. Optimization**

WOA is used to tune:

* Learning rate
* Hidden layer size
* Batch size
* Dropout rate

---

## **📊 Results**

The **WOA-CNN-LSTM** model consistently outperforms baseline models:

* Significant reduction in **RMSE, MAE, and MAPE**
* Up to **~90% improvement** over standard LSTM
* Accurate tracking of long-term degradation trends

---

## **📁 Repository Structure**

```
src/        → Model implementation  
data/       → Dataset   
figures/    → Report figures  
report/     → Report PDF file  
results/    → Output plots and evaluation results  
```

---

## **⚠️ Limitations**

* Limited to **three batteries**
* Evaluated on **laboratory-controlled data only**

