# Churn_prediction_Telecom_Industry_Data_Science


## Project Overview


This project is an end-to-end data analysis solution designed to extract critical business insights from Telecom data set. We utilize Python for data processing and analysis, Machine Learning algorithms for model building and structured problem-solving techniques to determine the reasons for customer churn . The project is ideal for data analysts looking to develop skills in data manipulation, model building , and data pipeline creation.

---

## Project Steps

### 1. Set Up the Environment
   - **Tools Used**: Python Jupyter Notebook. 
   - **Goal**: Create a structured workspace within VS Code and organize project folders for smooth development and data handling.

### 2. Download Customer Churn Data
   - **Data Source**: Use the Kaggle API to download the Customer Churn datasets from Kaggle.
   - **Dataset Link**: [Customer Churn Dataset](https://www.kaggle.com/datasets/shilongzhuang/telecom-customer-churn-by-maven-analytics)
   - **Storage**: Save the data in the `datasets/` folder for easy reference and access.

### 3. Install Required Libraries and Load Data
   - **Libraries**: Install necessary Python libraries using:
     ```powershell
     pip install pandas numpy matplotlib scikit-learn
     ```
   - **Loading Data**: Read the data into a Pandas DataFrame for initial analysis and transformations.

### 4. Explore the Data
   - **Goal**: Conduct an initial data exploration to understand data distribution, check column names, types, and identify potential issues.
   - **Analysis**: Use functions like `.info()`, `.describe()`, and `.head()` to get a quick overview of the data structure and statistics.

### 5. Data Cleaning
   - **Remove Duplicates**: Identify and remove duplicate entries to avoid skewed results.
   - **Unncessary Columns**: Using the correlation method, remove the columns which are not highly correlated.
   - **Handle Missing Values**: Using KNNImputer method fill the categorical missing values and fill the numerical columns using `.mode()` (most frequent data.)
   - **Fix Data Types**: Ensure all columns have consistent data types (e.g., dates as `datetime`).
   - **Convert Categorical Data**: Convert the categorical data into numerical data using label encoding technique.
   - **Validation**: Check for any remaining inconsistencies and verify the cleaned data.

### 6. Data Visualization
   - **Visualization**: Pie chart was used to check for the Number of customers churned, Stayed and Joined. Heatmap was used to determine the correlation between the columns.
     
### 7. Train Test Split
   - **Splitting of data**: The data is split into independent and dependent data respetively.The further split of training and test dataset occurs to test for the accuracy of the model prediction. The data is split into 80% training dataset and 20% test dataset.

### 7. Model Building
   - **Standardize the data**:  The data is standardized using `StandardScaler` for the algorithms to work efficiently on the same scale.
   - **PCA**:  The efficiency of the model reduces due to more number of dimesnions in dataset. Hence Principal Component Analysis is applied to reduce the dimensionality.
   - **Algorithms**: Various Machine Learning algorithms are used to check for the churn rate in telecom industry.Ensemble Algorithms like Random Forest Classifier, Decision Tree classifier, Support Vector Machine and LightGBM is used. Among which the LightGBM model stood exceptionally good in determining the customer churn for a service provider.
   - **Hyper-parameter tuning**: Many ensemble models contains various parameters, where it is necessary to determine the most optimal parameter that enhances the model performance. Hyper parameter tuning was carried out by GridSearchCV and RandomSearchCV. Along with which bagging technique was used to improve the model's efficiency.
   - **Performance Metrics**: Used various performance metrics like Accuracy, Recall, Precision, F-measure and AUC-ROC, to evaluate the model's performance. The AUC-ROC was used as an measure to determine the churn rate, where it was around 0.90%.
   - **Visualization**:  Various charts were used to plot the performance of the model using matplotlib or seaborn. 
     
### 8. Project Publishing and Documentation
   - **Documentation**: Maintain well-structured documentation of the entire process in Markdown or a Jupyter Notebook.
   - **Project Publishing**: Publish the completed project on GitHub or any other version control platform, including:
     - The `README.md` file (this document).
     - Jupyter Notebooks (if applicable).
     - Data files (if possible) or steps to access them.

---

## Requirements

- **Python 3.8+**
- **Python Libraries**:
  - `pandas`, `numpy`, `matplotlib`, `scikit-learn`,`seaborn`
- **Kaggle API Key** (for data downloading)

## Getting Started

1. Clone the repository:
   ```powershell
   git clone <repo-url>
   ```
2. Install Python libraries:
   ```powershell
   pip install -r requirements.txt
   ```
3. Set up your Kaggle API, download the data, and follow the steps to load and analyze.

---

## Project Structure

```plaintext
|-- data/                     # Raw data and transformed data
|-- notebooks/                # Jupyter notebooks for Python analysis
|-- README.md                 # Project documentation
|-- requirements.txt          # List of required Python libraries
|-- main.py                   # Main script for loading, cleaning, and processing data
```
---

## Results and Insights

This section will include your analysis findings:
- **Profitability**: Determines the customer who are likely to churn in the future and also tells the reason for churning which gives an insights for the service provider to reframe their policies if necessary. Reducing the churn rate by 5% , increases the profit by 60%.
- **Customer Behavior**: Predicting the Customers who are likely to churn the service providers. 

## Future Enhancements

Possible extensions to this project:
- Use deep learning techniques to give more accuracy.
- Additional Feature engineering techniques.
- Automation of the data pipeline for real-time data ingestion and analysis.

---

## License

This project is licensed under the MIT License. 

---

## Acknowledgments
- **Data Source**: Kaggle’s Customer Churn Dataset
---
