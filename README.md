# Obesity and Diabetes in the US 2011-2016
![Img from file](Images/main.png)
<br>
Diabetes is a disease that occurs when your blood glucose, also called blood sugar, is too high. Blood glucose is your main source of energy and comes from the food you eat. Insulin, a hormone made by the pancreas, helps glucose from food get into your cells to be used for energy

## Research done to Answer the following questions:
* Has Diabetes % Increased in the US 
* Has Obesity % Increaed in the US
* What are the top 10 states with Diabetes/Obesity
* What are the bottom 10 states with Diabetes/Obesity
* Do States with higher Diabetes Rates  also have Higher Obesity Rates

## Process
### Datasets
For Obesity dataset I used 6 difffent csv files from 2011-2016 downloaded from the CDC website\
For Diabetes dataset I used 6 diffrent csv files files from 2011-2016 downloaded from the CDC website

### Data Cleaning
For data cleaning I used Jupyter Notebook
```python
# Dependencies
import pandas as pd
from glob import glob

# use glob() to list all files that match a pattern 
obesity_files = sorted(glob('Resources/*-Obesity.csv'))
obesity_files
```
![Img from file](Images/output1.png)






