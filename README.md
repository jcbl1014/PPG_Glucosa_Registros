# PPG_Glucosa_Registros
Base de datos que contiene registros de señales PPG de 23 sujetos relacionados con la utilización de estas señales en la estimación de los niveles de  glucosa en sangre. 

# Download Dataset  

You can download all CSV files as a single ZIP file:  

🔗 [Download PPG_Glucosa_Registros.zip](https://github.com/jcbl1014/PPG_Glucosa_Registros/blob/main/PPG_Glucosa_Registros.zip)


# Photoplethysmography (PPG) and Blood Glucose Dataset

This repository provides a dataset of photoplethysmography (PPG) signals and corresponding blood glucose measurements from 23 individuals. The data is intended to support research in non-invasive blood glucose estimation.

## Dataset Description

Each subject's data is available as a CSV file named `Subject_X_complete.csv`, where `X` represents the subject number (e.g., `Subject_1_complete.csv`).

### Data Structure

Each CSV file contains the following columns:

- `t`: Time (seconds)
- `y`: PPG signal amplitude
- `y1`: First derivative of the PPG signal
- `y2`: Second derivative of the PPG signal
- `GENDER`: Subject’s gender (`M` for male, `F` for female)
- `AGE`: Subject’s age in years
- `DIABETIC`: Indicates whether the subject has diabetes (`YES` or `NO`)
- `TYPE OF DIABETES`: Specifies the type (`Type 1`, `Type 2`, or `NOT APPLICABLE`)
- `BLOOD GLUCOSE LEVEL (mg/dL)`: Blood glucose measurement in mg/dL

### Sample Data

```csv
t,y,y1,y2,GENDER,AGE,DIABETIC,TYPE OF DIABETES,BLOOD GLUCOSE LEVEL (mg/dL)
0.0,0.5,0.02,-0.001,M,45,NO,NOT APPLICABLE,85
0.01,0.52,0.021,-0.0011,M,45,NO,NOT APPLICABLE,85
...
```

## Research Applications

This dataset can be used for:

- Developing machine learning models for non-invasive glucose monitoring.
- Studying the relationship between PPG signal characteristics and glucose levels.
- Investigating the impact of demographic factors such as age and gender on PPG signals.

## Getting Started

1. **Clone the repository:**

   ```bash
   git clone https://github.com/jcbl1014/PPG_Glucosa_Registros.git
   ```

2. **Navigate to the dataset directory:**

   ```bash
   cd PPG_Glucosa_Registros
   ```

3. **Access data files:**

   Each subject’s data is stored in an individual CSV file (e.g., `Subject_1_complete.csv`).

## Data Collection Method

PPG signals were recorded using a standard PPG sensor placed on the fingertip. The sampling frequency was set at 100 Hz. Blood glucose levels were measured simultaneously using a calibrated glucometer.

## Download

All CSV files are available in a compressed ZIP archive:

🔗 [Download PPG_Glucosa_Registros.zip](https://github.com/jcbl1014/PPG_Glucosa_Registros/raw/main/PPG_Glucosa_Registros.zip)

## Citation

If this dataset is used in research, please cite:

```
@dataset{jcbl1014_PPG_Glucosa_Registros,
  author       = {Julio Cesar},
  title        = {Photoplethysmography (PPG) and Blood Glucose Dataset},
  year         = 2025,
  url          = {https://github.com/jcbl1014/PPG_Glucosa_Registros}
}
```

## License

This dataset is distributed under the [MIT License](LICENSE).

## Acknowledgments

Special thanks to all study participants for their contributions to this dataset.

