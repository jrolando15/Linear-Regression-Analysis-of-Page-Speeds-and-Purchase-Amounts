# Linear-Regression-Analysis-of-Page-Speeds-and-Purchase-Amounts

#Project Description
This project demonstrates the use of linear regression to analyze the relationship between website page speeds and purchase amounts. It includes generating synthetic data, performing linear regression analysis, and visualizing the results.

## Table of contents
- [Installation](#installation)
- [Usage](#usage)
- [Project Structure](#project-structure)
- [Examples](#examples)
  - [Generating Synthetic Data](#generating-synthetic-data)
  - [Performing Linear Regression](#performing-linear-regression)
  - [Plotting Results](#plotting-results)
- [License](#license)

## installation
To run this project, you need to have Python installed along with the following libraries:
- `numpy`
- `matplotlib`
- `scipy`

You can install these libraries using pip:
```bash
pip install numpy matplotlib scipy
```

## Usage
To run the project, simply execute the Python script. The script will generate synthetic data, perform linear regression analysis, and plot the results.

## Project structure
```bash
linear-regression-page-speeds/
├── notebooks/
│   └── linear_regression_page_speeds.ipynb         # Jupyter notebook with the code
│   ├── data_generation                             # Data generation  
│   ├── linear_regression                           # Linear regression analysis 
│   ├── plotting                                    # Plotting utility 
├── README.md                                       # Project README file
└── requirements.txt                                # List of dependencies
```

## Examples
- Generating Syntethic Data
```python
import numpy as np
from pylab import *

pageSpeeds = np.random.normal(3.0, 1.0, 1000)
purchaseAmount = 100 - (pageSpeeds + np.random.normal(0, 0.1, 1000)) * 3

scatter(pageSpeeds, purchaseAmount)
show()
```

# Performing linear Regression
```python
from scipy import stats

slope, intercept, r_value, p_value, std_err = stats.linregress(pageSpeeds, purchaseAmount)
r_squared = r_value ** 2
print(f"R-squared: {r_squared}")
```

# Plotting Results
```python
import matplotlib.pyplot as plt

def predict(x):
    return slope * x + intercept

fitLine = predict(pageSpeeds)

plt.scatter(pageSpeeds, purchaseAmount)
plt.plot(pageSpeeds, fitLine, c='r')
plt.show()
```

## License
This README file provides a comprehensive overview of the project, including installation instructions, usage, project structure, and examples of the different steps involved in the project. The project structure follows best practices for organizing Python projects, making it easy to navigate and maintain.
