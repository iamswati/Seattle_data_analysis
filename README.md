# PREDICT THE POWER CONSUMPTION OF BUILDINGS [View on Website](https://iamswati.github.io/Seattle_data_analysis/)

**Values Skills:** Data pre-processing, descriptive statistics, Python

**Skills:** Regression methods, Prediction methods.

## TASK

You work for the city of Seattle. To achieve its goal of a carbon-neutral city in 2050, your team is taking a close interest in emissions from non-residential buildings. For this, careful records were made by your agents in 2015 and 2016.However, these surveys are expensive to obtain, and from those already done, you want to try to predict the emissions of buildings whoseemissionshave not yet been measured.Two measures interest you: CO2 emissions and total energy consumption. You also want to evaluate the interest in the emission prediction of the ENERGYSTAR Score(which is complicated to calculate)with the approach currently used by your team.

```
# In Python, 3 environment comes with many helpful analytics libraries installed

import numpy as np        # linear algebra
import os                 # accessing directory structure
import pandas as pd       # data processing, CSV file I/O (e.g. pd.read_csv)

# Pandas uses the plot() method to create diagrams.
# Pythons uses Pyplot, a submodule of the Matplotlib library to visualize the diagram on the screen.
# Matplotlib is a low level graph plotting library in python that serves as a visualization utility
import matplotlib.pyplot as plt

# Seaborn is a Python data visualization library based on matplotlib. It provides a high-level interface for drawing attractive and informative statistical graphics.
import seaborn as sns
%matplotlib inline
```

# Readind 2015-building-energy-benchmarking.csv file

```
df_2015=pd.read_csv(r"C:\Users\swati\Desktop\Project 2\2015-building-energy-benchmarking.csv")
df_2015
```

## Drop un-necessary columns

```
df_2015.drop(['PropertyName', 'TaxParcelIdentificationNumber', 'CouncilDistrictCode', 'Neighborhood', 'DataYear', 'ListOfAllPropertyUseTypes', 'LargestPropertyUseType','LargestPropertyUseTypeGFA', 'SecondLargestPropertyUseType', 'SecondLargestPropertyUseTypeGFA', 'ThirdLargestPropertyUseType', 'ThirdLargestPropertyUseTypeGFA', 'YearsENERGYSTARCertified', 'Comment', 'Outlier', '2010 Census Tracts', 'City Council Districts', 'DefaultData', 'ComplianceStatus', 'Seattle Police Department Micro Community Policing Plan Areas', 'SPD Beats', 'Zip Codes'], axis=1, inplace=True)

# The head() method returns the headers and a specified number of rows, starting from the top.
df_2015.head()
```

## Correlation

![HeatMap 2015](https://user-images.githubusercontent.com/67102886/132089453-f809206d-7880-45e6-8277-13013920c216.png)

## Histogram

![Histogram](https://user-images.githubusercontent.com/67102886/132089600-daa86fef-47ca-44b2-8f47-35f232b07555.png)

![output](https://user-images.githubusercontent.com/67102886/132089530-95e86bd9-8e0e-4c01-8e9d-4dc91e44f9a6.png)

![output](https://user-images.githubusercontent.com/67102886/132089552-bf399b33-fe4b-46b6-953a-620300111391.png)

![output](https://user-images.githubusercontent.com/67102886/132089564-34e62773-8e98-4cc9-a615-2a7a3f23a2b8.png)

![output](https://user-images.githubusercontent.com/67102886/132089631-9966c085-dede-4c8a-be1e-c385080d3b0f.png)


# Reading 2016-building-energy-benchmarking.csv file

## Drop un-necessary columns

```
df_2016.drop(['OSEBuildingID', 'DataYear', 'BuildingType', 'PrimaryPropertyType', 'PropertyName', 'Address', 'City', 'State', 'ZipCode', 'TaxParcelIdentificationNumber', 'ListOfAllPropertyUseTypes', 'LargestPropertyUseType', 'LargestPropertyUseTypeGFA', 'ENERGYSTARScore', 'Neighborhood', 'CouncilDistrictCode', 'SecondLargestPropertyUseType', 'SecondLargestPropertyUseTypeGFA', 'ThirdLargestPropertyUseType', 'ThirdLargestPropertyUseTypeGFA', 'YearsENERGYSTARCertified', 'Comments', 'Outlier', 'DefaultData', 'ComplianceStatus'], axis=1, inplace=True)

# The head() method returns the headers and a specified number of rows, starting from the top.
df_2016.head()
```

## Correlation

![HeatMap 2016](https://user-images.githubusercontent.com/67102886/132089654-1f961a90-b864-4fbe-afc3-29dd439c915b.png)

## Histogram

![Histogram](https://user-images.githubusercontent.com/67102886/132089693-b780010e-bcd0-404b-acb2-15b64b2cd512.png)

![output](https://user-images.githubusercontent.com/67102886/132089711-d249dc91-3147-4bea-b45e-9c7a875f0a19.png)

![output](https://user-images.githubusercontent.com/67102886/132089718-5a563785-104e-409d-9619-34340861d115.png)

![output](https://user-images.githubusercontent.com/67102886/132089720-faea2156-b0cd-4f29-8ee7-21f6f3b2e359.png)

