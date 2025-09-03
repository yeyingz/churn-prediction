# 📊 Predicción de Churn en Clientes de Telecomunicaciones

Este proyecto desarrolla un sistema predictivo para anticipar el abandono de clientes (churn) en una empresa de telecomunicaciones. Utiliza Python, scikit-learn, XGBoost y LightGBM, y sigue un pipeline completo de análisis, limpieza, transformación, modelado y validación.

---

## 📁 Estructura del repositorio

churn-prediction/ 
│ 
├── data/ # Datasets utilizados 
├── notebooks/ # Jupyter notebooks del análisis y modelado 
├── src/ # Scripts reutilizables 
├── models/ # Modelos entrenados (si aplica) 
├── environment.yml # Entorno Conda reproducible 
├── requirements.txt # Librerías necesarias 
└── README.md # Documentación del proyecto

---

## 🚀 Cómo ejecutar el proyecto

1. Clona el repositorio:
   ```bash
   git clone https://github.com/yeyingz/churn-prediction.git
   cd churn-prediction

Crea el entorno virtual:

bash
conda env create -f environment.yml
conda activate churn-env
Abre los notebooks en VS Code o Jupyter:

bash
jupyter notebook
📊 Métricas del modelo final (XGBoost)
Accuracy: 0.9993

F1-score: 1.0000

AUC-ROC: 1.0000

Validación cruzada (5-fold):

Promedio F1-score: 1.0000

Desviación estándar: 0.0000

🧠 Variables más influyentes
TenureMonths

TotalCharges

MonthlyCharges

📌 Requisitos
Python 3.10

pandas, scikit-learn, xgboost, lightgbm, matplotlib, seaborn

Instalación alternativa:

bash
pip install -r requirements.txt
👤 Autor
Aurelio Jaén, Andalucía, España Proyecto desarrollado en septiembre de 2025

📄 Licencia
Este proyecto se distribuye bajo licencia MIT. Puedes usarlo, modificarlo y compartirlo libremente.

---

## ✅ 2. `.gitignore` recomendado

Este archivo evita subir archivos innecesarios o sensibles al repositorio.

```gitignore
# Jupyter notebooks checkpoints
.ipynb_checkpoints/

# Entornos virtuales
env/
venv/
__pycache__/
*.pyc

# Archivos de sistema
.DS_Store
Thumbs.db

# Modelos entrenados
*.pkl
*.joblib

# Archivos de configuración local
.env
*.log

# Datos grandes o sensibles
data/*.csv
data/*.xlsx