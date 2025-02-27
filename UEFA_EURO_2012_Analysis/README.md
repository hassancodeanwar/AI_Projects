# Euro 2012 Data Analysis

## Overview
This project analyzes the Euro 2012 dataset using Python and pandas. The dataset contains statistical information about the teams that participated in the UEFA Euro 2012 tournament. The analysis focuses on extracting insights such as goal statistics, discipline records, and other key performance metrics.

## Dataset
The dataset used in this project is `Euro2012_stats.csv`, which includes details such as:
- Team names
- Goals scored
- Shots on target
- Yellow and red cards received
- Passing and shooting accuracy

## Requirements
To run this analysis, you need to install the following Python libraries:

```bash
pip install pandas
```

## Project Steps
1. **Load the dataset**
   ```python
   import pandas as pd
   euro12 = pd.read_csv('Euro2012_stats.csv')
   ```

2. **Display general information about the dataset**
   ```python
   print(euro12.info())
   print(euro12.head())
   ```

3. **Extract specific data**
   - Select only the "Goals" column:
     ```python
     goals = euro12['Goals']
     print(goals)
     ```

   - Find the number of teams that participated in Euro 2012:
     ```python
     num_teams = euro12.shape[0]
     print(f'Number of teams that participated in Euro 2012: {num_teams}')
     ```

   - Select teams with more than 6 goals:
     ```python
     high_scoring_teams = euro12[euro12['Goals'] > 6]
     print(high_scoring_teams[['Team', 'Goals']])
     ```

   - Calculate the average number of yellow cards per team:
     ```python
     avg_yellow_cards = euro12['Yellow Cards'].mean()
     print(f'Average Yellow Cards per team: {avg_yellow_cards:.2f}')
     ```

## Running the Analysis
To execute the analysis, simply run the Python script:
```bash
python euro12_analysis.py
```
Ensure that the `Euro2012_stats.csv` file is in the same directory as the script.

## Conclusion
This project provides insights into Euro 2012 team performances, focusing on goal statistics, discipline records, and overall trends. It serves as an introduction to data analysis using pandas.

## License
This project is for educational purposes and does not contain proprietary data.

---

Feel free to modify the analysis and expand the dataset for further insights!

