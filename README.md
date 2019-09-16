## EECS 731 Project 1: Exploratory Analysis by Matthew Taylor

### Overview

The purpose of this project is to gain exposure to, and become familiar with, core data science tools. The pandas Python module will be used to combine two datasets in a way that might provide additional value or insight.

### Approach

For this project, I found two datasets relating to traffic. Specifically, I found a dataset containing a history of [gas prices in New York state](https://catalog.data.gov/dataset/gasoline-retail-prices-weekly-average-by-region-beginning-2007) and a dataset containing information on [car accidents in New York state](https://catalog.data.gov/dataset/motor-vehicle-crashes-case-information-beginning-2009). These two datasets contained partial overlap that I could leverage to combine these datasets.

The gas prices dataset lists the average gas price over a given week. However, the other dataset lists car accidents by day. Therefore, a simple transformation had to be made. Car accidents were grouped by week so the an average gas price could correspond to a single number of accidents. Once this transformation was made, the two datasets were simply combined by week. The resulting dataset could be used to determine a relationship between the price of gas and the number of car accidents.

### How to Run

This project was written in a Jupyter Notebook running Python 3.7.2. This project relies on a small number of modules, which can be installed by running this command:
```
pip3 install -r requirements.txt
```

Once the requirements are installed, each of the cells in the Jupyter Notebook can be executed. However, this is not required as each cell has already been executed and the results are shown.

### Results

This project was a wonderful introduction to the tools that will be used this semester and data science in general. It showed how vaguely related datasets can be combined to derive new insight. To demonstrate how this is possible, I performed simple linear regression on my resulting data frame and found an interesting trend: as the price of gas increases, the number of car accidents tends to decrease.
