# HEATGUARD

### AI-Assisted Heat Risk Forecasting and Early Warning System

HEATGUARD is a climate-risk analytics project designed to identify and communicate potential heat-health risks across Indian cities.

The project combines **ERA5-Land climate data**, thermal indicators, risk scoring, short-term forecasting, and geographic visualization to produce a practical **5-day heat warning outlook** and an interactive **India heat-risk map**.

> Built as an MVP for **Smart India Hackathon (SIH) 2026**.

---

## 🎯 Problem

Extreme heat is not only about high air temperature. Human exposure can also be affected by humidity, wind, thermal conditions, and local vulnerability.

HEATGUARD aims to convert these climate variables into information that is easier to understand and act upon:

- Where is heat risk concentrated?
- How severe could the risk become?
- What could the next few days look like?
- Which locations may need attention first?

---

## 💡 What HEATGUARD Does

The current MVP focuses on four main capabilities.

### 1. Thermal Dataset Generation

ERA5-Land climate data is processed into hourly and daily thermal datasets that can be used for downstream heat-risk analysis.

### 2. Heat-Risk Assessment

The project combines thermal conditions with vulnerability-related factors to estimate a human-health-related risk score.

### 3. 5-Day Heat Warning

HEATGUARD generates a short-term warning outlook containing:

- Forecast horizon
- Heat-risk probability
- Warning level

### 4. Interactive India Heat-Risk Map

The repository contains a Leaflet/Folium-based map that displays heat-risk information for selected Indian cities.

Each location can provide:

- City
- Peak forecast day
- Heat probability
- Vulnerability score
- Human health risk score
- Warning category

---

## 🧠 Core Concept

HEATGUARD follows this general pipeline:

```text
Climate Data
     ↓
Data Processing
     ↓
Thermal Indicators
     ↓
Risk Analysis
     ↓
Short-Term Forecast
     ↓
Heat Warning
     ↓
Interactive Visualization
```

The goal is to make climate information more useful for heat preparedness, planning, and public awareness.

---

## 🗂️ Repository Structure

| File | Description |
|---|---|
| `HEATGUARD_Step1_ERA5_Land.ipynb` | Notebook for ERA5-Land data processing |
| `HEATGUARD_hourly_thermal_dataset.csv` | Hourly thermal dataset |
| `HEATGUARD_daily_thermal_dataset.csv` | Daily thermal dataset |
| `HEATGUARD_5_day_heat_warning.csv` | 5-day heat-risk warning output |
| `HEATGUARD_India_Heat_Risk_Map.html` | Interactive India heat-risk map |
| `india heatmap.png` | Static heat-risk map visualization |
| `SIH 2026 - HEATGUARD MVP.pdf` | Project/MVP documentation |

---

## 🗺️ Interactive Heat-Risk Map

The repository includes an interactive map:

**[Open HEATGUARD India Heat Risk Map](./HEATGUARD_India_Heat_Risk_Map.html)**

The map is built using **Leaflet** and **OpenStreetMap** tiles through Folium.

The current MVP visualization includes example locations such as:

- Ahmedabad
- Delhi
- Kolkata
- Mumbai
- Srinagar

Clicking a location displays its forecast and risk information.

---

## 📊 Sample 5-Day Warning Output

The current MVP warning dataset contains the following example output:

| Forecast Horizon | Risk Probability | Warning Level |
|---|---:|---|
| +1 day | 79.87% | SEVERE |
| +2 day | 57.41% | HIGH |
| +3 day | 90.05% | EXTREME |
| +4 day | 98.76% | EXTREME |
| +5 day | 98.56% | EXTREME |

These values represent the current project output and are intended as **MVP/demo results**, not operational public warnings.

---

## 🧰 Technology Stack

### Programming & Analysis
- Python
- Jupyter Notebook
- Pandas
- NumPy

### Climate Data
- ERA5-Land

### Visualization
- Folium
- Leaflet.js
- OpenStreetMap
- Matplotlib

### Data Storage
- CSV

### Development
- Git
- GitHub
- Jupyter Notebook

---

## 🚀 Getting Started

### Prerequisites

Make sure you have:

- Python 3.9 or newer
- Jupyter Notebook or JupyterLab
- Git

### Clone the Repository

```bash
git clone https://github.com/puspalgoswami/HEATGUARD.git
cd HEATGUARD
```

### Create a Virtual Environment

#### Windows

```bash
python -m venv venv
venv\Scripts\activate
```

#### Linux / macOS

```bash
python3 -m venv venv
source venv/bin/activate
```

### Install Dependencies

Install the Python packages required for the notebook and visualization workflow:

```bash
pip install pandas numpy jupyter folium matplotlib
```

Start Jupyter:

```bash
jupyter notebook
```

Then open:

```text
HEATGUARD_Step1_ERA5_Land.ipynb
```

---

## 📈 Working With the Existing Dataset

The repository already contains processed datasets, so you can explore the available outputs without rebuilding the entire pipeline.

### Read the Daily Dataset

```python
import pandas as pd

df = pd.read_csv("HEATGUARD_daily_thermal_dataset.csv")

print(df.head())
print(df.shape)
```

### Read the 5-Day Warning

```python
import pandas as pd

warnings = pd.read_csv("HEATGUARD_5_day_heat_warning.csv")

print(warnings)
```

### Open the Interactive Map

Open the following file directly in a web browser:

```text
HEATGUARD_India_Heat_Risk_Map.html
```

---

## 🔬 Data Pipeline

### Step 1: Climate Data

ERA5-Land is used as the underlying climate-data source.

### Step 2: Thermal Data Processing

Relevant climate variables are processed into hourly and daily thermal datasets.

### Step 3: Risk Analysis

The processed thermal information is used to derive heat-risk and health-related metrics.

### Step 4: Forecasting

The project produces a short-term forecast extending up to five days.

### Step 5: Visualization

The results are presented through:

- CSV datasets
- A static India heatmap
- An interactive Leaflet map
- Heat warning outputs

---

## 🌡️ Risk Levels

The current MVP uses warning categories such as:

| Level | Meaning |
|---|---|
| LOW | Lower estimated heat-health risk |
| HIGH | Elevated heat-health risk |
| SEVERE | Significant heat-health concern |
| EXTREME | Very high estimated heat-health risk |

These categories are designed to make numerical outputs easier to interpret.

---

## 🌍 Why HEATGUARD?

A useful heat-warning system should do more than report temperature.

HEATGUARD focuses on a more practical question:

> **How risky could the heat become, where could it happen, and how soon could it happen?**

By combining climate information, thermal analysis, risk scoring, forecasting, and geographic visualization, HEATGUARD aims to provide a clearer picture of emerging heat risks.

---

## 🏗️ Future Scope

The current repository represents an MVP. Future development can include:

- Real-time weather and climate data ingestion
- Automated daily forecasting
- Higher-resolution geographic coverage
- More Indian cities and districts
- Integration of **WBGT, Heat Index, and UTCI**
- Improved machine-learning forecasting models
- More detailed vulnerability modeling
- Automated SMS, email, or mobile alerts
- Public-facing dashboard
- Mobile application
- Cloud deployment and API integration
- Validation using historical heatwave and health-impact data

---

## ⚠️ Disclaimer

HEATGUARD is a **research and prototype project**.

The outputs in this repository are intended for experimentation, demonstration, and further development. They should not be treated as a substitute for official weather forecasts, government heat-health warnings, or professional medical advice.

---

## 🏆 Project

**HEATGUARD — AI-Assisted Heat Risk Forecasting and Early Warning System**

**Smart India Hackathon 2026**

Repository:

https://github.com/puspalgoswami/HEATGUARD

---

## 👨‍💻 Author

**Puspal Goswami**

GitHub:

https://github.com/puspalgoswami

---

## 📄 License

No open-source license has been specified for this repository yet.
