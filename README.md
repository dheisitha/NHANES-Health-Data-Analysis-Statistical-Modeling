# NHANES 2021–2023 Exploratory Data Analysis

## Overview

This project presents an exploratory data analysis (EDA) of selected datasets from the **National Health and Nutrition Examination Survey (NHANES) 2021–2023** cycle. The analysis investigates relationships between demographic characteristics, body measurements, cardiovascular health indicators, cholesterol levels, and smoking behaviour.

Five NHANES datasets were merged into a single analytical dataset, followed by data cleaning, transformation, and feature engineering. Interactive visualizations were then developed using **Bokeh** to explore patterns and associations within the population.

The project demonstrates data wrangling, statistical exploration, and interactive data visualization techniques using Python in a Jupyter Notebook environment.

---

## Objectives

- Merge multiple NHANES datasets into a unified dataset
- Clean and preprocess health survey data
- Create derived health variables such as:
  - BMI Category
  - Hypertension Status
  - Cholesterol Classification
- Explore relationships between lifestyle factors and cardiometabolic health
- Develop interactive visualizations using Bokeh
- Consider ethical aspects of working with de-identified health data

---

## Datasets

The project uses the following NHANES 2021–2023 datasets provided in **SAS Transport (.xpt)** format:

- `DEMO` – Demographic Information
- `BMX` – Body Measurements
- `BPXO` – Blood Pressure
- `TCHOL` – Total Cholesterol
- `SMQ` – Smoking Questionnaire

These datasets are merged using the participant identifier before analysis.

---

## Technologies Used

- Python 3
- Jupyter Notebook
- NumPy
- Pandas
- Bokeh

---

## Python Libraries

```python
import numpy as np
import pandas as pd

from bokeh.plotting import figure, show
from bokeh.models import (
    ColumnDataSource,
    Slider,
    Select,
    HoverTool,
    CDSView,
    CustomJS,
    RangeSlider,
    DataTable,
    TableColumn,
    TextInput,
    Tabs,
    TabPanel,
    FactorRange
)

from bokeh.layouts import row, column
from bokeh.io import output_notebook, curdoc
from bokeh.transform import factor_cmap, jitter
```

---

## Project Structure

```
.
├── NHANES_Analysis.ipynb
├── DEMO.xpt
├── BMX.xpt
├── BPXO.xpt
├── TCHOL.xpt
├── SMQ.xpt
└── README.md
```

---

## Features

- Data import from SAS Transport (.xpt) files
- Data cleaning and preprocessing
- Dataset merging
- Missing value handling
- Feature engineering
- Interactive Bokeh visualizations
- Reader-controlled charts and tables
- Exploratory statistical analysis

---

## How to Run

1. Clone or download this project.
2. Ensure all `.xpt` dataset files are located in the project directory.
3. Install the required Python packages.

```bash
pip install numpy pandas bokeh jupyter
```

4. Launch Jupyter Notebook.

```bash
jupyter notebook
```

5. Open the notebook and run all cells.

---

## Analysis Topics

The notebook explores relationships including:

- Age and BMI
- BMI categories across demographic groups
- Blood pressure distributions
- Cholesterol classifications
- Smoking behaviour and cardiovascular indicators
- Demographic trends in health outcomes

Interactive controls allow users to filter and explore the data dynamically.

---

## Ethical Considerations

Although NHANES data is publicly available and de-identified, this project acknowledges the ethical responsibility involved in handling human health data. The analysis is intended solely for educational and analytical purposes while respecting participant privacy and avoiding misleading interpretations.

---

## Author

Developed as a data analysis project using Python, Jupyter Notebook, and the NHANES 2021–2023 datasets.