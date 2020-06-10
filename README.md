# Animated-and-Story-Telling-plot-For-COVID-19-Data-set-Using-Python

#### Import libraries 


import numpy as np # linear algebra

import pandas as pd # data processing

import matplotlib.pyplot as plt

import bar_chart_race as bcr

import seaborn as sns 

import os


#### Load data

os.chdir("D:\Data Sets")

data_1 = pd.read_csv("corona_dat.csv")

data_1.head() # to print first rows

#### Choose the 

cols =['date','Italy','China','Australia','Brazil','India','United Kingdom','Pakistan','Spain','Canada','New Zealand']

data_deaths = data_1[cols]

data_deaths.set_index("date", inplace = True)  ## Set date col as index 

dada_Ada=data_deaths.cumsum(axis = 0) ## take cumulative sum by dates

#### Plot Race bar plot with out put mp4 file

bcr.bar_chart_race(df=dada_Ada, filename='covid19_horiz.mp4', figsize = (3.5,3),title='COVID-19 Cases by Country')


###### Thanks ....... !




