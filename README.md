# TumorClassificationXAI

**This project tackles the Histopathologic Cancer Detection challenge, aiming to identify metastatic cancer in histopathology images. The dataset consists of 96x96 pixel images, with labels based on the presence of tumor tissue in the center 32x32 pixel region. The project compares two CNN architectures: a baseline model and one with batch normalization.**

---

## 🔎 Highlights & Demo

- **Live Demo:**  
  [![Open in Streamlit](https://static.streamlit.io/badges/streamlit_badge_black_white.svg)](https://tumor-classification-xai.streamlit.app/)  
  _Try tumor prediction and XAI heatmaps interactively!_

- **Visual Results Gallery:**

  | Original | Center Focus Region | Prediction | Attention/Heatmap |
  |:--------:|:------------------:|:----------:|:-----------------:|
  | ![](results/classes.png) | <img src="results/Figure_1.png" width="96"/> | **Tumor** |![](src/results/shap.png) |

---

## 🏆 TL;DR Results Table

| Metric               | Baseline CNN | BatchNorm CNN | Best Value | Visual Example        |
|----------------------|:------------:|:-------------:|:----------:|:---------------------:|
| Validation Accuracy  | 0.85         | 0.91          | 0.91       | ![](results/classes.png) |
| AUC                  | 0.93         | 0.97          | 0.97       | ![](results/Figure_1.png) |

---

## 🚀 Why This Matters

Accurate, explainable tumor detection in histopathology supports **faster**, more **reliable** cancer diagnostics, directly impacting patient outcomes and clinical decision-making. XAI visualizations help build *trust* in medical AI—making results transparent for pathologists and clinicians.

---

## 🖇️ Project Structure

- `data/` – Training & test data, labels
- `src/` – All core code for preprocessing, models, evaluation, and explainability
- `config/` – Config yaml for hyperparameters
- `results/` – Output figures, result images, and class distribution plots
- `requirements.txt` – Dependencies list
- `README.md` – Project documentation
- `app.py` – Streamlit webapp for live demo

---

## ⚙️ Setup & Quickstart

**Install dependencies:**  
```bash
pip install -r requirements.txt
```


**Download Data:**  
- Use [Kaggle Histopathologic Cancer Detection](https://www.kaggle.com/c/histopathologic-cancer-detection/data) (place in `/data`)

**Train & Validate:**  
```bash
python src/main.py
```

**Run Web Demo:**  
```bash
streamlit run app.py
```
---

## 🔑 Demo Output & Visualizations

| ROC Curve / Class Dist | Example Input Patch | XAI Heatmap |
|:----------------------:|:------------------:|:------------------:|:-----------:|
| ![](results/Figure_1.png) | ![](results/classes.png) | ![](results/shap_heatmap.png) |

---

## 📈 Results & Metrics

- **Baseline CNN:** Accuracy ~0.85, AUC ~0.93
- **BatchNorm CNN:** Accuracy ~0.91, AUC ~0.97

---

## 💬 Future Work

- Add data augmentation focused on the 32x32 central region for robustness.
- Develop explicit explainable-AI overlays (Grad-CAM/attention).
- Test for out-of-distribution generalization and rare tumor types.

---

## 🧑‍💼 Contributors

- [Av1352 (Anju Vilashni)](https://github.com/Av1352)
- [yukta1103](https://github.com/yukta1103)
- [sidd9981](https://github.com/sidd9981)
