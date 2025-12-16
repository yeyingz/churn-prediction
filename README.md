# 📊 Predicción de Churn en Clientes de Telecomunicaciones

Este proyecto desarrolla un sistema predictivo para anticipar el abandono de clientes (churn) en una empresa de telecomunicaciones. Utiliza Python, scikit-learn, XGBoost y LightGBM, y sigue un pipeline completo de análisis, limpieza, transformación, modelado y validación.

## 📁 Estructura del repositorio

churn-prediction/ 
│ 
├── data/ contract.csv internet.csv personal.csv phone.csv
├── notebooks/ churn_prediction_code.ipynb
├── environment.yml # Entorno Conda reproducible 
├── informe_tecnico.ipynb
├── requirements.txt # Librerías necesarias 
└── README.md # Documentación del proyecto

---
## Key Findings

### 1. La Trampa de la "Falsa Lealtad" (Relación Antigüedad vs. Gasto)
**El Insight:** El análisis reveló que los clientes con mayor `TotalCharges` (alto valor histórico/LTV) no son necesariamente los más seguros. De hecho, existe un punto de inflexión donde los usuarios "antiguos" con cuotas mensuales altas (`MonthlyCharges`) se vuelven **altamente sensibles al precio** y propensos a irse si no se les ofrecen incentivos. 
**Impacto de Negocio:**
- **Acción:** No dar por sentada la fidelidad de los veteranos. Crear un programa VIP específico para clientes con `TotalCharges` alto para "blindar" la base de ingresos más crítica.

### 2. Eficiencia Quirúrgica del Presupuesto de Marketing
**El Insight:** Al utilizar un modelo optimizado por **F1-Score** en lugar de Accuracy simple, hemos logrado minimizar los *Falsos Negativos* (clientes que se van sin que nos demos cuenta). 
**Impacto de Negocio:**
- **Ahorro:** En lugar de lanzar campañas de retención masivas (caras y molestas) a toda la base de datos, el modelo permite dirigir el presupuesto **solo al ~20% de clientes** que realmente están en riesgo. Esto triplica el ROI de las campañas de marketing.

### 3. El "Mes de la Muerte" (Patrones de Abandono Temprano)
**El Insight:** El modelo detectó que el comportamiento financiero en los primeros meses (`MonthlyCharges` en relación con contratos de corto plazo) es el predictor más fuerte de abandono temprano. Si un cliente sobrevive a este "valle de la muerte" inicial, su probabilidad de quedarse se dispara exponencialmente.

**Impacto de Negocio:**
- **Estrategia:** El equipo de *Onboarding* debe intervenir agresivamente durante los primeros 3 meses. Si logramos retenerlos en ese periodo crítico, el **Customer Lifetime Value (CLTV)** se multiplica automáticamente sin esfuerzo adicional.

---

## 🚀 Cómo ejecutar el proyecto

1. Clona el repositorio:
   ```bash
   git clone https://github.com/yeyingz/churn-prediction.git
   cd churn-prediction


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
