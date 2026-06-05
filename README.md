# Titanic-Dataset-Analysis-using-Pandas
A structured exploratory data analysis (EDA) of the Titanic dataset using Python and Pandas. The notebook covers data exploration, filtering, aggregation, missing value handling, and key survival insights -organized across seven analytical parts.

---

## Dataset

**File:** `titanic.csv`

The Titanic dataset contains passenger information from the 1912 RMS Titanic disaster. Key columns include:

| Column | Description |
|---|---|
| `pclass` | Passenger class (1 = First, 2 = Second, 3 = Third) |
| `age` | Age of the passenger |
| `gender` | Gender of the passenger |
| `fare` | Ticket fare paid |
| `survived` | Survival status (1 = Survived, 0 = Did not survive) |
| `embarked` | Port of embarkation (S = Southampton, C = Cherbourg, Q = Queenstown) |

---

## Notebook Structure

### Part A - Dataset Exploration
- Load dataset into a Pandas DataFrame
- Inspect first/last 5 rows, dataset shape
- View column names, data types, and summary statistics

### Part B - Filtering Data
- Filter by age, gender, survival status, passenger class, and fare
- Use both boolean indexing and `query()` method
- Filter passengers by embarkation port

### Part C - Unique Values and Counts
- Find unique passenger classes and embarkation ports
- Count passengers by class, gender, and survival status using `value_counts()`

### Part D - Sorting
- Top 10 passengers by highest fare paid
- Top 10 youngest passengers
- Multi-column sort by passenger class and age

### Part E - Missing Values
- Count missing values per column
- Count missing ages specifically
- Handle missing values:
  - Replace missing age with mean age
  - Drop all rows with any missing values

### Part F - Grouping
- Average age and fare per passenger class
- Survival rate by gender
- Average age by gender
- Passenger count per embarkation port

### Part G - Mini Analysis (Key Findings)
| Question | Finding |
|---|---|
| Highest survival rate by class | First class - **62%** |
| Did females survive more than males? | Yes - female survival rate: **74%** |
| Most popular embarkation port | **Southampton (S)** |
| Maximum fare paid | **512** |
| Average passenger age | **~29 years** |

---

## Requirements

- Python 3.x
- pandas

Install dependencies:

```bash
pip install pandas
```

---

## Usage

1. Clone or download this repository.
2. Place `titanic.csv` in the same directory as the notebook.
3. Open the notebook:

```bash
jupyter notebook Titanic_Dataset_Analysis.ipynb
```

4. Run all cells sequentially (Cell → Run All).

---

## Key Concepts Covered

- `df.head()`, `df.tail()`, `df.shape`, `df.dtypes`, `df.describe()`
- Boolean indexing and `df.query()`
- `df.sort_values()`, `df.value_counts()`, `df.unique()`
- `df.isnull().sum()`, `df.fillna()`, `df.dropna()`
- `df.groupby()` with aggregation functions (`mean`, `count`)
