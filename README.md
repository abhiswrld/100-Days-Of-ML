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
* 📁 `Day_23_to_34_Feature_Engineering/` - Feature Scaling, Categorical Encoding, ColumnTransformers, Pipelines, Mathematical & Power Transformations, and Date/Time variables.

*(I will continue adding folders as I progress through the course!)*

## Tech Stack & Libraries Used

* **Language:** Python
* **Data Extraction:** `requests`, `BeautifulSoup4`
* **Data Manipulation:** `pandas`, `numpy`
* **Data Visualization:** `matplotlib`, `seaborn`
* **Statistics:** `scipy`
* **Machine Learning & Preprocessing:** `scikit-learn` (Pipelines, Transformers, Encoders, Linear & Tree Models)
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
* **Day 28:** Discovered the power of `ColumnTransformer` in scikit-learn. I learned how to streamline feature engineering—instead of manually applying different transformations (like `SimpleImputer` for numericals, `OrdinalEncoder` for ordinal categoricals, and `OneHotEncoder` for nominals) to individual columns and then concatenating multiple NumPy arrays, `ColumnTransformer` handles it all in one clean, efficient step!
* **Day 29:** Mastered Scikit-Learn `Pipeline`s. I learned how to chain multiple preprocessing steps and a machine learning model into a single, cohesive workflow. By building a Titanic survival predictor, I successfully connected imputation, One-Hot Encoding, MinMax scaling, feature selection (`SelectKBest`), and a Decision Tree classifier. Pipelines drastically clean up the code and ensure the exact same transformations are applied to both training and test sets.
* **Day 30:** Explored Mathematical Feature Transformations to handle skewed data and convert it into a normal distribution. Learned how to apply Log Transforms (great for right-skewed data), Reciprocal Transforms, and Square Transforms (for left-skewed data) using scikit-learn's `FunctionTransformer`. I also used KDE and QQ plots to visualize the distributions before and after transformation, and proved that linear models (like Logistic Regression) benefit from normally distributed data, while tree-based models (like Decision Trees) remain largely unaffected.
* **Day 31:** Dived into `PowerTransformer`s in Scikit-Learn to convert arbitrary distributions into normal distributions. I explored the **Box-Cox** and **Yeo-Johnson** methods. I learned that Box-Cox searches for an optimal lambda value to normalize the data but requires strictly positive numbers (which I bypassed by adding a tiny constant `0.00001`), whereas Yeo-Johnson natively handles zero and negative values. I tested both on a Concrete Strength dataset, comparing Linear Regression $R^2$ scores and Cross-Validation results before and after the transformations.
* **Day 32:** Covered Discretization (Binning) using `KBinsDiscretizer` to convert continuous numerical features into categorical bins, which helps handle outliers and improve value spread. I applied KMeans and Quantile strategies via `ColumnTransformer`, evaluated the impact on a Decision Tree's accuracy, and visualized the distribution shifts using Matplotlib.
* **Day 33:** Messed around with Handling Mixed Data to clean columns containing both numerical and categorical information (like the Titanic dataset's Cabin and Ticket features). I learned how to separate these into distinct columns using Pandas techniques like `pd.to_numeric`, `np.where`, regex extraction (`str.extract`), string slicing, and lambda functions.
* **Day 34:** Explored Date and Time Variables. I learned how to convert string columns to datetime objects using `pd.to_datetime`. Using the Pandas `.dt` accessor, I extracted features like the year, month, day, day of the week, week of the year, and time components (hour, minute, second). I also created custom boolean flags (like checking if a day falls on a weekend) and calculated elapsed time using the `datetime` module.
* **Day 35:** Started the "Handling Missing Data" module. Mapped out the differences between Univariate (mean/median/mode) and Multivariate (KNN/Iterative) imputation. Focused today on **Complete Case Analysis (CCA)**—the technique of dropping rows with missing values. I learned the golden rule: only apply CCA if the missing data is Missing Completely at Random (MCAR) and makes up less than 5% of the dataset. I used Matplotlib (histograms and KDE density plots) and Pandas to visually and numerically prove that the data distributions for both numerical and categorical variables remained identical before and after dropping the rows!