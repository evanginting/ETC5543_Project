# Predicting Critical Elements in Coal Mine Waste: A Machine Learning Approach for a Low-Emission Future

## Objective
As global demand for critical minerals rises, this study investigates the economic potential of ex-
tracting critical elements from coal mine waste in Australia. Using data from the largest element mapping project by ACARP, combined with recent private sector research, this research employs exploratory data analysis (EDA) and machine learning to achieve two key objectives: (1) leveraging low-cost element analysis (ME-4ACD81) to predict concentrations of valuable elements such as REEs (Rare Earth Element), HREEs (Heavy Rare Earth Element), and LREEs (Light Rare Earth Element) through numerical regression, and (2) identifying enriched elements and project areas with significant economic potential for future extraction. The study found that elements from lower cost lab test can predict the REEs, HREEs, and LREEs with reasonably good performance. This was achieved even with the challenge of low correlation coefficient between the independent and dependent variables. This study also found that Fort Cooper possess a significant amount of critical elements, making it economically feasible to pursue extraction efforts with confidence that the investment in Fort Cooper will yield substantial returns and contribute meaningfully to meeting the global demand for critical minerals.

## Structure
The ETC554_Project repository is the record for data analysis process and the integration of final report:

1. "data" folder: The collections of the raw data of element concentration from ACARP projects and private researches.

2. 01_Data_Preparation.Rmd: It is a rmd file for wrangling process for raw data in data folder and merge all different projects to single RDS object.

3. results folder: The collections of RDS output= yielded from the wrangling process in data preparation.

4. 02_Exploratory_Data_Analysis.Rmd: The exploratory data analysis(EDA) working file to summarize their main patterns and elemental correlation via visualization techniques, which is used to identify enrichment elements and project areas with siginificant potential and build up the foundation for preditive analysis stage.

5. 02_Exploratory_Data_Analysis.html: The html report rendered from 02_Exploratory_Data_Analysis.Rmd.

6. 03_Predictive_Analysis.Rmd:  Under machine learning method, the predictive analysis work file to use element list in low-cost element analysis (ME-4ACD81) to predict concentrations of valuable elements such as REEs
(Rare Earth Element), HREEs (Heavy Rare Earth Element), and LREEs (Light Rare Earth Element).

7. Presentation folder:

8. "Final_report"" folder: The integration process for the final academic report in Monash report format.

## Usage
To replicate the analysis:

1. Download or clone the repository.
2. Navigate to the data folder and place your raw data files.
3. Open 01_Data_Preparation.Rmd to preprocess the data and generate the necessary RDS files.
4. Run 02_Exploratory_Data_Analysis.Rmd for data exploration and visualization.
5. Execute 03_Predictive_Analysis.Rmd for machine learning-based predictive modeling.

## Session information
This repository is built and managed by Posit Cloud with R version 4.4.1. The prerequsite of the package include:

**Data Preparation stage:**

- Tidyverse 2.0.0,
- data.Table 1.15.4,
- openxlsx 4.2.5.2,

**EDA stage:**

- knitr 1.4.8,
- corrplot 0.94,
- kableExtra 1.4.0,
- gridExtra 2.3,
- moments 0.14.1,
- MASS 7.3-60.2

**Predictive Analysis stage:**

- tidymodels 1.2.0,
- randomForest 4.7-1.2,
- randomForestSRC: 3.3.1,
- xgboost 1.7.8.1,
- vip 0.4.1,
- rpart 4.1.23,
- MLmetrics 1.1.3,
- doParallel 1.0.17

**Final report:**
The report template is created from Monash package, to install this:

```
# install.packages("remotes")
remotes::install_github("numbats/monash")
library(monash)
```


## License
This project is licensed under the MIT License - see the LICENSE file for details.

## Acknowledgement
This repository is managed by Evan Ginting (evanginting - egin0003@student.monash.edu) & Yuhao Long (Alberlong44 - ylon0012@studeb.monash.edu), with the collaboration with Matrix Geoscience team, Kane Maxwell(kane.maxwell@matrixgeoscience.com) and Limin Xu (limin.xu@matrixgeoscience.com).
