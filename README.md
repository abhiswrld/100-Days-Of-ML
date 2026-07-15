# 100 Days of Machine Learning Journey

This repository contains my code, notes, and projects as I work my way through the [CampusX 100 Days of Machine Learning](https://www.youtube.com/playlist?list=PLKnIA16_Rmvbr7zKYQuBfsVkjoLcJgxHH) course.

I am using this repository to track my daily progress, store my datasets, and act as a personal dictionary for machine learning code.

## Repository Structure

The folders are organized based on the course curriculum. Here is my progress so far (Days 1-22):

* 📁 `Day_01_to_14_ML_Basics/` - Intro to ML, Types of ML, MLDLC, Tensors, Environment Setup, and an End-to-End Toy Project.
* 📁 `Day_15_Working_with_CSV/` - Data ingestion with Pandas.
* 📁 `Day_16_Working_with_JSON_SQL/` - Extracting data from JSON files and SQL databases.
* 📁 `Day_17_Fetching_Data_API/` - Hitting APIs to gather external data.
* 📁 `Day_18_Web_Scraping/` - Using BeautifulSoup and requests (Scraping Quotes to Scrape).
* 📁 `Day_19_to_22_EDA/` - Exploratory Data Analysis (Univariate, Bivariate, Multivariate) and Pandas Profiling.

*(I will continue adding folders as I progress through the course!)*

## Tech Stack & Libraries Used

* **Language:** Python
* **Data Extraction:** `requests`, `BeautifulSoup4`
* **Data Manipulation:** `pandas`, `numpy`
* **Environment:** VS Code (with Jupyter Extension)

## Progress Log

* **Days 1-14:** Covered the theoretical foundations of ML, set up local environments, and built an end-to-end toy project.
* **Days 15-17:** Learned how to bring in data from diverse sources including CSVs, JSON, SQL databases, and web APIs.
* **Day 18:** Successfully scraped quotes, authors, and tags from a sandbox website and structured them into a Pandas DataFrame!
* **Days 19-22:** Mastered Exploratory Data Analysis (EDA) to understand datasets and used Pandas Profiling for automated reporting.
* **Day 23:** Started the Feature Engineering module, focusing on different types and techniques for preparing raw data for ML models.
* **Day 24:** Learned about the first topic of Feature Scaling, more importantly Standardization. Understood why it is necessary to standardize data since it helps with model performance in the long run.
* **Day 25:** Normalization is very helpful, especially when we know the min and max value in the dataset (then we can use MinMaxScaling). For outliers use RobustScaling, and for space data we use MaxAbsScaling.
* **Day 26:** Ordinal Encoding is used for categorical data that is presented in some order (such as rankings), one important thing is to know that label encoding is used for only target variables.
* **Day 27:** One Hot Encoding is used for categorical data that is presented in no given order (such as car brands). I learnt how to use OHE to transform categorical data that is nominal into numerical data that can be read by the ML algorithms.