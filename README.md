PPG and Blood Glucose Dataset 2025
This repository contains a dataset of PPG signals and blood glucose levels collected from multiple participants. The data can be used for research in biomedical signal processing and non-invasive glucose estimation.
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
The .MAT files containing the raw PPG signals were converted to .CSV using the following MATLAB script:
% Get a list of .MAT files in the current folder
files = dir('*.mat');

% Process each .MAT file
for i = 1:length(files)
    % Load the .MAT file
    matData = load(files(i).name);
    
  % Get a list of .MAT files in the current folder
files = dir('*.mat');

% Process each .MAT file
for i = 1:length(files)
    % Load the .MAT file
    matData = load(files(i).name);
    
    % Extract the vectors
    t = matData.t;   % Time vector
    y = matData.y;   % PPG forehead
    y1 = matData.y1; % PPG ear
    y2 = matData.y2; % PPG finger

    % Create a table with the data
    dataTable = table(t, y, y1, y2);

    % Generate the .CSV filename
    csvFileName = strrep(files(i).name, '.mat', '.csv');
    
    % Save the table as a CSV file
    writetable(dataTable, csvFileName);
    
    fprintf('Converted file: %s\n', csvFileName);
end

disp('Conversion completed. All .MAT files have been converted to .CSV.');

% Test the conversion with an example subject file
data = readtable('Subject_17_complete.csv');  
head(data) % Display the first rows of the file





## Research Applications

This dataset can be used for:

- Developing machine learning models for non-invasive glucose monitoring.
- Studying the relationship between PPG signal characteristics and glucose levels.
- Investigating the impact of demographic factors such as age and gender on PPG signals.


   Each subject’s data is stored in an individual CSV file (e.g., `Subject_1_complete.csv`).


## Download

All CSV files are available in a compressed ZIP archive:

🔗 [Download PPG_Glucosa_Registros.zip](https://github.com/jcbl1014/PPG_Glucosa_Registros/raw/main/PPG_Glucosa_Registros.zip)

