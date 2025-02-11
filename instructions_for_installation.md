# **Instructions for Running the LendingClub Customer Segmentation Analysis**

This guide provides step-by-step instructions on how to set up and run the **LendingClub Customer Segmentation Analysis** project.

## **Table of Contents**
- [Prerequisites](#prerequisites)
- [Installation](#installation)
- [Dataset Download](#dataset-download)
- [Database Setup](#database-setup)
- [Running the Jupyter Notebook](#running-the-jupyter-notebook)
- [Usage](#usage)
- [Troubleshooting](#troubleshooting)

---

## **Prerequisites**
Before running this project, ensure you have the following installed:
- **Python 3.10 or later**  
- **PostgreSQL Database**
- **Jupyter Notebook**
- **Git** (Optional, for version control)

---

## **Installation**
### **1. Clone the Repository**
If you haven’t already, clone the project repository from GitHub:

```bash
git clone https://github.com/abualfaki/MPV1-analyzing_loan_data
cd MPV1-analyzing_loan_data
```

### **2. Create a Virtual Environment**
It’s recommended to use a virtual environment for package management:

```bash
python -m venv env
source env/bin/activate  # On Windows, use `env\Scripts\activate`
```

### **3. Install Dependencies**
Install the required Python libraries:

```bash
pip install -r requirements.txt
```

Alternatively, you can install them manually:

```bash
pip install pandas numpy matplotlib seaborn scikit-learn fuzzywuzzy psycopg2-binary ipython-sql jupyter
```

---

## **Dataset Download**
Since the dataset is too large to be stored in the repository, download it manually from Kaggle:

1. Visit the following link:  
   [LendingClub Loan Defaulters Dataset](https://www.kaggle.com/code/faressayah/lending-club-loan-defaulters-prediction?select=accepted_2007_to_2018Q4.csv.gz)
2. Download the file `accepted_2007_to_2018Q4.csv.gz`
3. Extract and place the file inside the `data/` directory in the project root.

---

## **Database Setup**
1. **Start PostgreSQL**: Ensure your PostgreSQL server is running.
2. **Create a Database**:
   ```sql
   CREATE DATABASE accepted_loans_db;
   ```
3. **Modify Database Connection Settings**: Update database credentials in the notebook `exploratory_data_analysis.ipynb` located in the EDA folder where needed.
4. **Load Data into PostgreSQL**:
   - Use the code in the "Create SQL database to host accepted loans data" section of the `exploratory_data_analysis.ipynb` to load CSV data into tables in the accepted_loans database

---

## **Running the Jupyter Notebook**
Once the environment is set up, run the Jupyter Notebook:

```bash
jupyter notebook
```

- Navigate to the **Jupyter Notebook UI**.
- Open the `/MPV1/notebooks/data_cleaning/accepted_loans_data_cleaning.ipynb` file to clean the data
- Then open the `/MPV1/notebooks/EDA/exploratory_data_analysis.ipynb` to see insights from Exploratory Data Analysis
- Execute the cells sequentially.

---

## **Usage**
- The notebook analyzes **customer segmentation**, **default rates**, and **geographic distributions**.
- It includes **data cleaning, preprocessing, and visualizations**.
- Modify SQL queries and analysis parameters as needed.

---

## **Troubleshooting**
### **1. Virtual Environment Not Activating**
Ensure the virtual environment is activated:
```bash
source env/bin/activate  # On Windows, use `env\Scripts\activate`
```

### **2. PostgreSQL Connection Issues**
- Verify PostgreSQL service is running.
- Check `host`, `port`, `user`, and `password` in database connection settings.

### **3. Package Import Errors**
Ensure all dependencies are installed:
```bash
pip install -r requirements.txt
```

---

## **Conclusion**
You’re now ready to run the **LendingClub Customer Segmentation Analysis**! 🚀

If you encounter any issues, refer to the **Troubleshooting** section or open an issue in the repository.

