# **Data Cleaning in Python**  

This repository contains a **Python script** that demonstrates essential **data cleaning operations** using **Pandas**. The script processes an **Excel dataset** by handling duplicates, missing values, formatting inconsistencies, and filtering out unnecessary records, ensuring the data is structured and ready for analysis.  

---

## **Overview**  

This script performs a series of **data cleaning steps** to improve data quality and usability.  

### **Key Steps:**  

#### **1. Read Data**  
- Loads data from an **Excel file** into a Pandas DataFrame:  
  ```python
  df = pd.read_excel(r"C:\Users\Ashritha\Downloads\Customer Call List.xlsx")
  ```  

#### **2. Remove Duplicates**  
- Identifies and removes **duplicate rows** to avoid redundancy.  

#### **3. Drop Unnecessary Columns**  
- Eliminates the **Not_Useful_Column**, as it is irrelevant for analysis.  

#### **4. Handle Missing Values**  
- Replaces **NaN values** with a placeholder `'-'`.  
- Standardizes inconsistent missing value representations (`'N/a'`, `'NaN'`) by converting them to `'-'`.  

#### **5. Clean & Format Data**  
- **Last_Name:** Removes unwanted characters (e.g., numbers and punctuation).  
- **Phone_Number:** Standardizes phone number format by replacing `"/"` and `"|"` with `"-"`.  

#### **6. Split Address Data**  
- Separates **full address** into three distinct columns:  
  - `Street_Address`  
  - `State`  
  - `Zip_Code`  

#### **7. Standardize Binary Columns**  
- Converts values in **Do_Not_Contact** and **Paying Customer** columns to:  
  - `'Y'` for **Yes**  
  - `'N'` for **No**  

#### **8. Filter Records**  
- **Removes records** where:  
  - `Do_Not_Contact` is `'Y'`.  
  - `Phone_Number` is missing (`'-'`).  

#### **9. Reset DataFrame Index**  
- Resets the index after filtering to maintain consistency.  

---

## **How to Run the Script**  

### **1. Install Pandas**  
Ensure Pandas is installed in your Python environment:  
```bash
pip install pandas
```  

### **2. Adjust File Path**  
Modify the script if needed to match the location of your dataset:  
```python
df = pd.read_excel(r"C:\Users\Ashritha\Downloads\Customer Call List.xlsx")
```  

### **3. Execute the Script**  
Run the script in your preferred Python environment:  
- **Jupyter Notebook**  
- **IDE (PyCharm, VS Code, etc.)**  
- **Command Line (Python script execution)**  

---

## **Conclusion**  

This script provides a **practical approach to data cleaning** using Pandas. It ensures the dataset is structured and analysis-ready by **handling missing values, formatting inconsistencies, and filtering records**.  
