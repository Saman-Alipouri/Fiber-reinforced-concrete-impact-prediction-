
# Fibercrete Impact Resistance Prediction

This project uses machine learning to predict the **impact resistance** of fiber-reinforced concrete containing **crumb rubber particles**. The predictions focus on impact energy at the **first crack (FCU)** and **ultimate failure (URU)** based on laboratory testing data.

---

##  Dataset Description

The dataset includes:
- Experimental results from concrete mixes with and without polypropylene fibers and crumb rubber.
- Tests conducted at two curing temperatures: -10°C and 25°C.
- Each sample measured:
- FC: Blows to first crack
- UR: Blows to ultimate failure
- PINPB: Percent increase in number of post-crack blows
- FCU: Energy absorbed until first crack (kN.mm)
- URU: Energy absorbed until failure (kN.mm)

###  Sample Features

| Feature | Description |
|--------------|--------------------------------------------|
| FC | Number of blows to first crack |
| UR | Number of blows to ultimate failure |
| PINPB (%) | % increase in blows after first crack |
| CuringTemp | Curing temperature in Celsius |
| **FCU** | Impact energy to first crack (target) |
| **URU** | Impact energy to failure (target) |

---

##  Machine Learning Model

A **MultiOutputRegressor with XGBoost** was trained to predict:
- FCU (First Crack Energy)
- URU (Ultimate Failure Energy)

### Evaluation Metrics:

- R² Score
- MAE (Mean Absolute Error)
- RMSE (Root Mean Squared Error)

### Feature Importance was also computed for each target variable.

---

##  Project Files

```
fibercrete-impact-prediction/
├── impact_resistance.csv # Cleaned dataset
├── modeling.ipynb # Jupyter Notebook (Colab-compatible)
├── impact_model.pkl # Trained ML model
└── README.md # Project description
```

---

##  Notes

- This project is based on a Master's thesis in Civil Engineering – Construction Management.
- All experimental data were obtained through real lab testing.
- The goal is to help better design rubberized concrete with improved impact performance.

---

##  License

This project is open for academic and research use.
