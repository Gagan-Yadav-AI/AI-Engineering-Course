# Day 26 | Machine Learning Associate

### **1. Setup & Import**

```python
import pandas as pd
import numpy as np
import seaborn as sns
import matplotlib.pyplot as plt
from sklearn.model_selection import train_test_split
from sklearn.linear_model import LinearRegression
from sklearn.metrics import mean_squared_error, r2_score

```

* **What it does:** This section brings in all the external toolkits your script needs to function.
* `pandas` and `numpy` handle the data tables and math.
* `seaborn` and `matplotlib` handle drawing graphs.
* `sklearn` provides the actual machine learning algorithms and scoring tools.


* **Expected Output:** *None.* This runs silently in the background.

---

### **2. Data Ingestion**

```python
    print("Loading data...")
    try:
        df = pd.read_csv('Advertising.csv')
    except FileNotFoundError:
        print("Error: 'Advertising.csv' not found. Please ensure it is in the same directory.")
        return

```

* **What it does:** It attempts to read the `Advertising.csv` file into a pandas DataFrame (a virtual table named `df`). The `try/except` block acts as a safety net. If you forgot to put the CSV file in the same folder as the script, it will print an error message and stop instead of crashing the whole program.
* **Expected Output:**
> Loading data...



---

### **3. Data Preprocessing & Cleaning**

```python
    if 'Unnamed: 0' in df.columns:
        df = df.drop('Unnamed: 0', axis=1)

    print("\nChecking for missing values:")
    print(df.isnull().sum())

```

* **What it does:** Often, CSV files have a useless index column (like row numbers) labeled `Unnamed: 0`. This code checks if that column exists and deletes it (`drop`) because it doesn't help predict sales. Then, it counts how many blank/missing values exist in each column.
* **Expected Output:**
> Checking for missing values:
> TV           0
> Radio        0
> Newspaper    0
> Sales        0
> dtype: int64



---

### **4. Exploratory Data Analysis (EDA)**

```python
    print("\nGenerating Correlation Matrix plot...")
    plt.figure(figsize=(6, 4))
    sns.heatmap(df.corr(), annot=True, cmap='coolwarm', fmt=".2f")
    plt.title("Correlation Matrix: Advertising vs Sales")
    plt.tight_layout()
    plt.show() # This will pop up a window with the graph

```

* **What it does:** It calculates the mathematical correlation between every column (e.g., how much does Sales go up when TV spending goes up?). It then uses Seaborn to draw a colored heatmap of these numbers.
* **Expected Output:** 1. A printed line in the terminal: > Generating Correlation Matrix plot...
2. **A separate graphical window will pop up** showing a grid with red (strong positive correlation) and blue (weak/negative correlation) squares. *Note: The script will pause here. You must close the graph window for the rest of the code to run.*

---

### **5. Feature Engineering**

```python
    X = df[['TV', 'Radio', 'Newspaper']]
    y = df['Sales']

```

* **What it does:** It separates your data into two distinct variables. `X` becomes a table holding only your inputs (the advertising budgets). `y` becomes a single column holding your target output (the sales numbers you want to predict).
* **Expected Output:** *None.* This is an internal data manipulation step.

---

### **6. Data Splitting**

```python
    X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.2, random_state=42)

```

* **What it does:** It shuffles your data and splits it into a "Training Set" (80% of the rows) and a "Testing Set" (20% of the rows). The `random_state=42` ensures that every time you run this script, it shuffles the data the exact same way, making your results reproducible.
* **Expected Output:** *None.* ---

### **7. Model Selection & Training**

```python
    print("\nTraining Linear Regression model...")
    lr_model = LinearRegression()
    lr_model.fit(X_train, y_train)

```

* **What it does:** It creates a blank Linear Regression model object. Then, `.fit()` feeds the model the 80% training data. The model studies how the `X_train` budgets relate to the `y_train` sales and figures out the best mathematical formula to connect them.
* **Expected Output:** > Training Linear Regression model...

---

### **8. Model Evaluation**

```python
    y_pred = lr_model.predict(X_test)

    rmse = np.sqrt(mean_squared_error(y_test, y_pred))
    r2 = r2_score(y_test, y_pred)

    print(f"\n--- Model Evaluation Metrics ---")
    print(f"Root Mean Squared Error (RMSE): {rmse:.2f}")
    print(f"R-squared (R2) Score: {r2:.4f} (Explains ~{r2*100:.1f}% of variance)")

```

* **What it does:** First, it forces the trained model to guess the sales (`y_pred`) for the 20% test set using only the test budgets. Then, it compares those guesses to the actual known sales (`y_test`).
* **RMSE** measures how far off the guesses are on average.
* **R-squared** measures the percentage of accuracy (a score of 1.0 is perfect).


* **Expected Output:** *(Numbers may vary slightly depending on your exact CSV file)*
> --- Model Evaluation Metrics ---
> Root Mean Squared Error (RMSE): 1.78
> R-squared (R2) Score: 0.8994 (Explains ~89.9% of variance)



---

### **9. Optimization & Finalization**

```python
    print("\n--- Learned Coefficients (Impact per unit spent) ---")
    coefficients = dict(zip(X.columns, np.round(lr_model.coef_, 3)))
    for feature, coef in coefficients.items():
        print(f"- {feature}: {coef}")

```

* **What it does:** The model learned a specific "multiplier" (coefficient) for each type of advertising. This code extracts those hidden multipliers, rounds them to 3 decimal places, and prints them out. This tells you exactly how much 1 unit of spending in a specific category increases sales.
* **Expected Output:**
> --- Learned Coefficients (Impact per unit spent) ---
> * TV: 0.045
> * Radio: 0.189
> * Newspaper: 0.003
> 
> 



---

### **10. The Execution Block**

```python
if __name__ == "__main__":
    main()

```

* **What it does:** This is standard Python practice. It simply says: "If this script is being run directly by the user, trigger the `main()` function." It prevents the code from accidentally running if you decide to import this file into another Python project later.
* **Expected Output:** *None.* It just starts the sequence.
