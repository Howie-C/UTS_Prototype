# UTS_Prototype
UTS - Research Project Prototype
This is the prototype application developped for UTS 32933 Research Project course.

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

## Research Dataset
MIMIC-IV is a relational database containing real hospital stays for patients admitted to a tertiary academic medical center in Boston, MA, USA.  
For more details or downloading, please refer to: [MIMIC-IV](https://mimic-iv.mit.edu/docs/)

## How to test the prototype?

### Test by using the GUI (Recommanded)
Run the file GUI.py to initiate the Graphical User Interface window.  
Functions can be select, different algorithms are clear and easy to select as options in GUI.

### Test prediction modelling only (A quick way but cannot view the complete prototype)
Run the file predict_modelling.py.  
In row 457, modify the coressponding variables explained in row 455.  
```python
if __name__ == '__main__':

	#modelling(sample_size, tt_ratio, balancing, top_N, model_approach)    # row 455

	modelling(1000, 0.3, 1, 1, 2)    # row 457
```
For example, in the above, sample size = 1000, train-test ratio = 0.3, data balancing is True, Top_N is 500, Model algorithm is Random Forest.  
Balancing Code:  
0 - Imbalanced Data  
1 - Balanced Data  
Top_N Code:  
0 - no Top_N applied  
1 - Top 500 icd  
2 - Top 300 icd  
Model Code:  
0 - Decision Tree  
1 - SVM  
2 - Random Forest  

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

