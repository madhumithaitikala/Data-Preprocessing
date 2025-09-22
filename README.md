# Data-Preprocessing
Data Cleaning and Preprocessing  handled missing values, removed duplicates, standardized formats, and prepared Netflix dataset for analysis.
INTERVIEW-QUESTIONS:
1. What are missing values and how do you handle them?**

Missing values occur when data entries are absent for some variables in a dataset.
Handling them:
Remove rows/columns: Use `dropna()` if missing data is small.
Imputation: Fill with mean, median, mode, or use advanced methods like KNN or regression.
Flagging: Create a separate indicator for missing values.

----------------------------------------------------------------------------
2. How do you treat duplicate records?**
Duplicates are rows that appear more than once.
Treatment:
 Identify duplicates using `duplicated()` in Pandas.
 Remove duplicates using `drop_duplicates()`.
 Sometimes, investigate if duplicates are valid before removing.
-----------------------------------------------------------------------------
3. Difference between dropna() and fillna() in Pandas?
dropna() : Removes missing values
When missing data is small and deletion won’t affect analysis 
fillna() Replaces missing values with a specified value
When you want to impute missing data rather than delete it    
4. What is outlier treatment and why is it important?
Outliers are extreme values that differ significantly from other observations.
Importance:
They can skew analysis, affect model performance, and lead to misleading insights.
Treatment:
 Remove outliers if they are errors.
 Cap or floor extreme values (Winsorization).

Transform data (log, square root) to reduce impact.

----------------------------------------------------------------------------------
5. Explain the process of standardizing data.
Standardization rescales data to have a mean = 0 and standard deviation = 1
Formula:

$$
Z = \frac{X - \mu}{\sigma}
$$
 $X$ = original value, $\mu$ = mean, $\sigma$ = standard deviation
 Purpose:
 Ensures features contribute equally to distance-based algorithms like KNN, SVM.


 ---------------------------------------------------------------------------------------
6. How do you handle inconsistent data formats (e.g., date/time)?
 Identify inconsistencies (e.g., `DD/MM/YYYY` vs `MM-DD-YYYY`).
Convert to a uniform format using Pandas:
df['date'] = pd.to_datetime(df['date'], format='%Y-%m-%d')

------------------------------------------------------------------------------------

7. What are common data cleaning challenges?

* Missing values and null entries.
* Duplicate rows or records.
* Outliers and anomalies.
* Inconsistent formats (dates, strings, units).
* Typographical or spelling errors.
* Noise in data or irrelevant columns.

--------------------------------------------------------------------------------

8. How can you check data quality?

Completeness: Check for missing values (`isnull().sum()`).
Uniqueness:Look for duplicates.
Consistency: Ensure formats and units are uniform.
Accuracy: Compare with source or expected ranges.
Validity: Check if values are within acceptable limits or categories.
Timeliness: Ensure data is current and relevant.


