# Technical Challenge Documentation Anyone AI

## Introduction
Congratulations! 👏 You have reached the Technical Challenge. This process evaluates your programming abilities. Below is the documentation for the Jupyter Notebook titled **Customers and Orders**, which includes instructions and solutions for two coding exercises:

1. **Exercise 1: Processing Customers Data**
2. **Exercise 2: Processing Orders Data**

The exercises use two datasets:

- `customers.csv`: Contains a list of customers.
- `orders.csv`: Contains orders data linked to the customers.

These datasets are automatically downloaded and saved in the `sample_data` directory at the start of the notebook session. 

---

## Contents of the Notebook

### 1. Importing Required Libraries
The notebook begins by importing necessary libraries for data processing and analysis:

```python
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
```

### 2. Loading the Datasets
The datasets are loaded into Pandas DataFrames for analysis. The code snippet below shows the loading process:

```python
# Load customers dataset
customers = pd.read_csv('sample_data/customers.csv')

# Load orders dataset
orders = pd.read_csv('sample_data/orders.csv')
```

### 3. Exercise 1: Processing Customers Data
This section includes questions and tasks for analyzing the `customers.csv` dataset. Tasks may include:

- Calculating basic statistics about the customer base.
- Identifying unique customers.
- Filtering and grouping data to extract insights.

#### Example Code:
```python
# Example: Calculate the total number of customers
num_customers = customers['customer_id'].nunique()
print(f'Total customers: {num_customers}')
```

### 4. Exercise 2: Processing Orders Data
This section deals with the `orders.csv` dataset and focuses on:

- Understanding relationships between customers and their orders.
- Analyzing order trends and product details.
- Visualizing data using charts and graphs.

#### Example Code:
```python
# Example: Calculate the total value of orders per customer
orders['total_value'] = orders['quantity'] * orders['price']
customer_order_value = orders.groupby('customer_id')['total_value'].sum()
print(customer_order_value)
```

### 5. Data Visualization
Several sections of the notebook include visualization tasks, using libraries like Matplotlib to generate insights:

```python
# Example: Bar chart of orders per customer
orders_per_customer = orders['customer_id'].value_counts()
orders_per_customer.plot(kind='bar')
plt.title('Orders per Customer')
plt.xlabel('Customer ID')
plt.ylabel('Number of Orders')
plt.show()
```

### 6. Exporting Processed Data
After completing the tasks, processed datasets or results can be exported for further use:

```python
# Save processed data to CSV
processed_orders.to_csv('sample_data/processed_orders.csv', index=False)
```

---

## Tips for Completing the Challenge

- Review Python basics, including data manipulation with Pandas and visualization with Matplotlib.
- Use online resources or documentation if needed.
- Take your time; there are no time constraints.

---

## Submission Instructions
Once the exercises are complete:

1. Save the notebook as `customers_and_orders.ipynb`.
2. Submit the notebook through the provided course platform for evaluation.