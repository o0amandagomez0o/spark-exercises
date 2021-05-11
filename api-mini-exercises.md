# Spark API Mini Exercises

Copy the code below to create a pandas dataframe with 20 rows and 3 columns:

```python
import pandas as pd
import numpy as np

np.random.seed(13)

pandas_dataframe = pd.DataFrame({
    "n": np.random.randn(20),
    "group": np.random.choice(list("xyz"), 20),
    "abool": np.random.choice([True, False], 20),
})
```

1. Spark Dataframe Basics

    1. Use the starter code above to create a pandas dataframe.
    1. Convert the pandas dataframe to a spark dataframe. From this point
       forward, do all of your work with the spark dataframe, not the pandas
       dataframe.
    1. Show the first 3 rows of the dataframe.
    1. Show the first 7 rows of the dataframe.
    1. View a summary of the data using `.describe`.
    1. Use `.select` to create a new dataframe with just the `n` and `abool`
       columns. View the first 5 rows of this dataframe.
    1. Use `.select` to create a new dataframe with just the `group` and `abool`
       columns. View the first 5 rows of this dataframe.
    1. Use `.select` to create a new dataframe with the `group` column and the
       `abool` column renamed to `a_boolean_value`. Show the first 3 rows of
       this dataframe.
    1. Use `.select` to create a new dataframe with the `group` column and the
       `n` column renamed to `a_numeric_value`. Show the first 6 rows of this
       dataframe.

1. Column Manipulation

    1. Use the starter code above to re-create a spark dataframe. Store the
       spark dataframe in a varaible named `df`

    1. Use `.select` to add 4 to the `n` column. Show the results.

    1. Subtract 5 from the `n` column and view the results.

    1. Multiply the `n` column by 2. View the results along with the original
       numbers.

    1. Add a new column named `n2` that is the `n` value multiplied by -1. Show
       the first 4 rows of your dataframe. You should see the original `n` value
       as well as `n2`.

    1. Add a new column named `n3` that is the n value squared. Show the first 5
       rows of your dataframe. You should see both `n`, `n2`, and `n3`.

    1. What happens when you run the code below?

        ```python
        df.group + df.abool
        ```

    1. What happens when you run the code below? What is the difference between
       this and the previous code sample?

        ```python
        df.select(df.group + df.abool)
        ```

    1. Try adding various other columns together. What are the results of
       combining the different data types?

