# Assignment

## Brief

Write the Python codes for the following questions.

## Instructions

Paste the answer as Python in the answer code section below each question.

### Question 1

Question: Select all numeric columns except float from the DataFrame `dft`.

Answer:

```
import numpy as np
import pandas as pd

ft = pd.DataFrame(
    {
        "A": np.random.rand(3), 
        "B": 1, 
        "C": "foo", 
        "D": pd.Timestamp("20010102"), 
        "E": pd.Series([1.0] * 3).astype("float32"), 
        "F": False, 
        "G": pd.Series([1] * 3, dtype="int8")})

dft

# Select numeric columns excluding float types
numeric_non_float = dft.select_dtypes(include=['int', 'int64', 'int32', 'int16'],exclude =['float'])
numeric_non_float

```

### Question 2

Question: How do you return the last 3 rows of a DataFrame `df`?

Answer:

```

data = {"state": ["Ohio", "Ohio", "Ohio", "Nevada", "Nevada", "Nevada"],
        "year": [2000, 2001, 2002, 2001, 2002, 2003],
        "pop": [1.5, 1.7, 3.6, 2.4, 2.9, 3.2]}

frame = pd.DataFrame(data)
frame.tail(3)

```

### Question 3

Question: Return the minimum and maximum of a Series `x` as a new Series with the index `["min", "max"]`.

Answer:

```
sdata = {"Ohio": 35000, "Texas": 71000, "Oregon": 16000, "Utah": 5000}
x = pd.Series(sdata)
x
result = pd.Series([x.min(), x.max()], index=["min", "max"])
result


```

### Question 4

Question: Multiply `df1` and `df2` (two DataFrames) with a `fill_value` of 1.

Answer:

```
df1 = pd.DataFrame(np.arange(20.).reshape((4, 5)), columns=list("abcde"))
df2 = pd.DataFrame(np.arange(30.).reshape((5, 6)), columns=list("abcdef"))
df1.multiply(df2, fill_value=1)

```

### Question 5

Question: How do you create a DataFrame from a nested dictionary of dictionaries?

```python
nested_dict = {'A': {'a': 1, 'b': 2}, 'B': {'a': 3, 'b': 4}}




```

Answer:

```
frame4 = pd.DataFrame(nested_dict)

frame4

```

## Submission

- Submit the URL of the GitHub Repository that contains your work to NTU black board.
- Should you reference the work of your classmate(s) or online resources, give them credit by adding either the name of your classmate or URL.
