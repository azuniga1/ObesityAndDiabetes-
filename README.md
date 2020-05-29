# Obesity and Diabetes in the US 2011-2016
![Img from file](Images/main.png)
<br>
Diabetes is a disease that occurs when your blood glucose, also called blood sugar, is too high. Blood glucose is your main source of energy and comes from the food you eat. Insulin, a hormone made by the pancreas, helps glucose from food get into your cells to be used for energy

## Research done to Answer the following questions:
* Has Diabetes % Increased in the US 
* Has Obesity % Increaed in the US
* What are the top 5 states with Diabetes/Obesity
* What are the bottom 5 states with Diabetes/Obesity
* Do States with higher Diabetes Rates  also have Higher Obesity Rates

## Technology used
* Anaconda 
* Jupyter NoteBook
* Python/Pandas
* Tableau

## Process
### Datasets
For Obesity dataset I used 6 difffent csv files from 2011-2016 downloaded from the CDC website\
For Diabetes dataset I used 6 diffrent csv files files from 2011-2016 downloaded from the CDC website

### 1. Data Cleaning
I used Jupyter Notebook to concate the difffent csv files into one csv file and data cleaning
```python
# Dependencies
import pandas as pd
from glob import glob

# use glob() to list all files that match a pattern 
obesity_files = sorted(glob('Resources/*-Obesity.csv'))
obesity_files
```
![Img from file](Images/output1.png)

```python
# Concat all files  by using pd.concat() and asssign() methods
obesity_2011_to_2016 = pd.concat((pd.read_csv(file).assign(filename = file)
          for file in obesity_files), ignore_index = True)
obesity_2011_to_2016.head()
```
![Img from file](Images/output2.png)


### 2. Visualization
I used Tableau to visualize my findings

Map of Diabetes & Obesity in 2016

![Img from file](Images/DiabetesMap.png)

![Img from file](Images/ObesityMap.png)

[Tableau DashBoard](https://public.tableau.com/views/USADiabetesObesity2011-2016/Dashboard1?:display_count=y&publish=yes&:origin=viz_share_link)


### 3. Conclusion
* Has Diabetes % Increased in the US 
    <br>From 2011-2016 Diabetes has increase from 8.4% to 8.5% 
    <br>
* Has Obesity % Increaed in the US
    <br>From 2011-2016 Obesity has increased from 27.4% to 29.6%
    <br>
* What are the top 5 states with Diabetes/Obesity
    <br>
    In 2016 the top 5 states<br>
    Diabetes:<br>
    1. Alabama 13.2%<br>
    2. West Virginia 12.7%<br>
    3. Mississippi 12.14%<br>
    4. Arkansas 12.1%<br>
    5. Kentucky 11.8%<br>
    <br>
    Obesity:<br>
    1. West Virginia 37.7%<br>
    2. Mississippi 37.3%<br>
    3. Arkansas 35.7%<br>
    4. Alabama 35.7%<br>
    5. Lousisian 34.8%<br>
    <br>
* What are the bottom 5 states with Diabetes/Obesity
* Do States with higher Diabetes Rates  also have Higher Obesity Rates




