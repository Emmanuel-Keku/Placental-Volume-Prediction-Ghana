# Placental Volume and Utero-Placental Hemodynamics as Early Biomarkers of Adverse Perinatal Outcome in Ghana

### 📚 Course: Stats Models - Final Project | Spring 2025
### 🏫 Tarleton State University
### 👨‍🎓 Authors: Emmanuel Keku & Jonathan Dadzie
### 👨‍🏫 Supervisor: Dr. Jesse Crawford

---

## 📌 Abstract
Placental insufficiency is a major contributor to adverse 
perinatal outcomes — including fetal growth restriction, 
preeclampsia, preterm birth, and stillbirth — conditions 
that disproportionately affect low-and-middle-income 
countries like Ghana.

This study, the **PREDICT-Ghana Study**, developed and 
evaluated regression-based predictive models for 
**second-trimester placental volume** using accessible 
maternal and sonographic variables, providing a low-cost 
alternative to expensive 3D ultrasound technology.

---

## 🎯 Objectives
- Develop accurate predictive models for mid-trimester 
  placental volume
- Outperform traditional clinical judgment alone
- Provide a low-cost alternative to 3D ultrasound
- Support early risk stratification in resource-limited 
  settings in Ghana
- Guide aspirin prophylaxis and antenatal surveillance

---

## 📊 Dataset: PREDICT-Ghana Cohort
- **Type:** Prospectively simulated dataset calibrated to 
  real-world Ghanaian antenatal populations
- **Records:** 1,010 pregnant women
- **Setting:** Mid-trimester ultrasound examination, Ghana
- **Missing Values:** None
- **Target Variable:** Placental Volume (mL)

### Study Variables
| Category | Variables |
|----------|-----------|
| **Primary Outcome** | Placental Volume (mL) |
| **Ultrasound** | Gestational Age, UtA-PI, UtA-RI, Bilateral Notching Score, Placental Thickness |
| **Hemodynamics** | Umbilical Vein Flow (scaled), Spiral Artery Remodeling Angle |
| **Maternal** | Age, Height, Weight, Pre-pregnancy BMI |
| **Laboratory** | Hemoglobin (g/dL), PAPP-A (scaled MoM ×10) |

---

## 🛠️ Tools & Technologies
- **Language:** R
- **Environment:** Google Colab
- **Methods:**
  - Ordinary Least Squares (OLS) Regression
  - Polynomial Regression
  - 10-Fold Cross Validation
- **Diagnostics:**
  - Shapiro-Wilk Test (Normality)
  - Brown-Forsythe Test (Homoscedasticity)
  - Q-Q Plots
  - Residuals vs Fitted Plots

---

## 📋 Methodology

### 1. Data Description
- Descriptive statistics computed for all variables
  (mean, SD, median, quartiles, min, max)
- Complete dataset with no missing values

### 2. Model Building
Three regression models were developed and compared:

| Model | Description |
|-------|-------------|
| **Full Model** | All predictor variables included |
| **Reduced Model** | Only statistically significant predictors (p<0.05) |
| **Polynomial Model** | Includes quadratic term for Spiral Artery Angle I(SpiralArteryAngle²) |

> The **quadratic term** for Spiral Artery Remodeling 
> Angle was included to capture its known **non-linear 
> relationship** with placental volume.

### 3. Model Validation
- **10-Fold Cross Validation** in base R
- Estimated out-of-sample predictive performance (RMSE)
- Compared stability of linear vs polynomial models

### 4. Model Diagnostics
- ✅ Residual normality: Shapiro-Wilk test + Q-Q plots
- ✅ Homoscedasticity: Brown-Forsythe test + 
  Residuals vs Fitted plots
- ✅ All statistical tests two-sided (α = 0.05)

---

## 🏆 Key Findings

### Most Important Predictors of Placental Volume
| Predictor | Clinical Relevance |
|-----------|-------------------|
| **Gestational Age** | Primary driver of placental growth |
| **UtA-PI & UtA-RI** | Markers of placental vascular resistance |
| **Bilateral Notching** | Indicator of defective trophoblast invasion |
| **Spiral Artery Angle** | Non-linear U-shaped relationship with volume |
| **PAPP-A (<0.4 MoM)** | Associated with placental-related complications |
| **Maternal Hemoglobin** | Low levels linked to reduced placental volume |
| **Pre-pregnancy BMI** | Higher BMI linked to larger but dysfunctional placenta |

### Clinical Implications
- 🏥 Models provide accurate, **affordable alternative** 
  to 3D ultrasound for resource-limited settings in Ghana
- 🔍 Enable **early risk stratification** at 18–22 week 
  anomaly scans
- 💊 Guide **aspirin prophylaxis** decisions for 
  high-risk pregnancies
- 👶 Potential to **reduce adverse perinatal outcomes** 
  in sub-Saharan Africa

---

## 💡 Conclusions
- Regression-based models using simple 2D ultrasound 
  measurements and basic anthropometry can reliably 
  predict placental volume
- The polynomial model with quadratic Spiral Artery Angle 
  term outperforms the standard linear model
- 10-fold cross-validation confirmed model generalisability
- These models can be integrated into routine antenatal 
  care in district-level facilities across Ghana
- Findings align with established literature on placental 
  insufficiency in low-resource settings

---

## 🔮 Future Work
- Prospective validation on real clinical cohort data
- External validation in other sub-Saharan African settings
- Integration with electronic health record (EHR) systems
- Development of a clinical decision support tool

---

## 📁 Project Files
| File | Description |
|------|-------------|
| `STATS_MODELS_PROJECT_Emmanuel-Keku.ipynb` | Full R Notebook |

---

## 🔗 Related Projects
- [DS1: Postnatal Depression Prediction](https://github.com/Emmanuel-Keku/Postnatal-Depression-Prediction)
- [Capstone: Hybrid Bayesian-Ensemble Framework](https://github.com/Emmanuel-Keku/Perinatal-Depression-Hybrid-Framework)

---

## 📚 Key References
1. Collins et al. (2019). Placental volume and adverse 
   outcomes. *Ultrasound in Obstetrics & Gynecology*
2. Cnossen et al. (2008). Uterine artery Doppler for 
   preeclampsia prediction. *BJOG*
3. Adu-Bonsaffoh et al. (2023). Antenatal care in Ghana.
4. Melchiorre et al. (2020). Spiral artery remodeling 
   and perinatal outcomes.
5. WHO (2023). Global perinatal health report.

---

## 📫 Contact
### Emmanuel Keku
- 📧 **Email:** ekekuinchrist247@gmail.com
- 🔬 **ORCID:** https://orcid.org/0000-0001-5864-4843
- 🐙 **GitHub:** https://github.com/Emmanuel-Keku

