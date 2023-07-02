<a name="readme-top"></a>
<div align = "center">
  <h1 align="center">Fifa Player Performance Analysis</h3>
  <p align="center">
    Analysis of performance of FIFA players across multiple years, from FIFA 17 through FIFA 22.
    <br />
</div>

<!-- TABLE OF CONTENTS -->
<details>
  <summary>Table of Contents</summary>
  <ol>
    <li>
      Project Objective
      <ul>
        <li><a href="#built-with">Technologies Used</a></li>
      </ul>
      <ul>
        <li><a href="#built-with">methods Used</a></li>
      </ul>
    </li>
    <li><a href="#About dataset">About the dataset</a></li>
    <li><a href="#Missing values">Treatment of missing values</a></li>
    <li><a href="#Encoding categorical variables">Encoding of Categorical Variables</a></li>
    <li><a href="#Feature Selection">Feature Selection</a></li>
    <li><a href="#Model Used">Model</a></li>
    <li><a href="#Evaluation Metric">Evaluation Metric</a></li>
  </ol>
</details>

<!-- Project Objective -->
<a name="Project Objective"></a>
## Project Objective

The goal of this competition is to leverage data analysis, machine learning, and statistical modeling techniques to gain valuable insights into player performance, trends, and potential.

<p align="right">(<a href="#readme-top">back to top</a>)</p>

### Technologies Used

* Numpy
* Pandas
* Matplotlib
* Scikitlearn

<p align="right">(<a href="#readme-top">back to top</a>)</p>

### Methods Used

* Exploratory Data Analysis
* Data Preprocessing
* Machine Learning

<p align="right">(<a href="#readme-top">back to top</a>)</p>

<!-- ABOUT THE Dataset-->
## About The Dataset

The dataset contains detailed player information for FIFA editions from FIFA 17 to FIFA 22, including player attributes, ratings, positions, clubs, contract details, physical attributes, and various performance metrics. It offers a rich collection of features for in-depth analysis and exploration.
Note: This dataset is sourced from the FIFA video game series and represents virtual player attributes and statistics rather than real-world performance data.

[Dataset Link](https://www.kaggle.com/competitions/mltiverse-join-comp/data)

<p align="right">(<a href="#readme-top">back to top</a>)</p>

<!-- Missing values-->
## Treatment of missing values

For treatment of missing values I have plotted graphs that shows the relationship between missing values and values present with target variable.

Inference from the graph:
1. for some of the features the mean of target variable (Value) is 0 for missing values which may be due to the lack of information that we get from missing values so we dropped those rows and made a observation that if those features contains null values in test set then Value must be zero.
  
2. for the left out features i have done univariate imputation.

<p align="right">(<a href="#readme-top">back to top</a>)</p>


## Feature Selection

Feature selection is done through lasso regression.

<p align="right">(<a href="#readme-top">back to top</a>)</p>


## Model
<a name="Model"></a>
After trying out serveral different models I found out Random Forest Regressor to be the best model providing me the least Rmse score which is my evaluation metric and no other model like XGBoostRegressor or ANN was even close to it.

<p align="right">(<a href="#readme-top">back to top</a>)</p>

## Evaluation Metric

<table>
  <tr>
    <th>Model</th>
    <th>RMSE score(Val)</th>
    <th>RMSE score(Test)</th>
  </tr>
  <tr>
    <td>Random Forest Regressor</td>
    <td>401547.06</td>
    <td>2748736.90</td>
  </tr>
</table>

<p align="right">(<a href="#readme-top">back to top</a>)</p>
