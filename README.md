# UTS_Prototype
UTS - Research Project Prototype
This is the prototype application developped for UTS 32933 Research Project course.

## Files Overview:
Please use Python 3 to excecute the programs.

### GUI.py
This is the main file that a user can initiate the Graphical User Interface window, user can interact and perform all the functions by running this file.

### data_processing.py
This file is imported and used in GUI.py.  
This program manipulate the datasets using Python Pandas, implement ETL (extract, transform and load) on the original datasets.

### predict_modelling.py
This file is imported and used in GUI.py.  
This is the core modelling program which performs the predictions. Scikit-learn is mainly used as the modelling tool here.

### top_N.py
This file is NOT imported and used in GUI.py  
This program goes through all the data and filters out the top 'N' number of diagnoses icds. Saved the filtered data as CSV file in 'data' folder.  
top_300.csv and top_500.csv is already created for testing.

### others
4 ploting files are stored under folder 'plot'.  
Both 4 files are imported and used in GUI.py

## Imported External Libraries
All the modelues imported and the coresponding format is listed as below.
```python
import tkinter as tk
from tkinter import PhotoImage
from tkinter import ttk
from PIL import ImageTk, Image
from prettytable import PrettyTable
import time
import pandas as pd
import numpy
import sklearn.model_selection as cross_validation
import sklearn.tree as tree
import sklearn.metrics as metrics
import matplotlib.pyplot as plt
import seaborn as sns
from sklearn import svm, datasets, metrics, model_selection
from sklearn.metrics import accuracy_score
from sklearn.ensemble import RandomForestClassifier
from sklearn.datasets import make_classification
```

## Installation
For Windows:  
Use the package manager [pip](https://pip.pypa.io/en/stable/) to install the external libriaires listed above.

```bash
pip install tk
pip install Pillow
pip install prettytable
pip install times
pip install pandas
pip install numpy
pip install -U scikit-learn
pip install matplotlib
pip install seaborn
```

## Contribution
Supervisor:  
Xueping Peng  
Students:  
Yihao Chen  
GUI develop, modelling design, modelling implementation, data ETL, data visualization, part of reporting.  
Jinghan Wang  
Modelling design, modelling implementation, program testing and result analysis, most of reporting.  
Junzhou Zhang  
Modelling design, part of reporting.


