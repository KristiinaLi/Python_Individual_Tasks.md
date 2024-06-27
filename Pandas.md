## Pandas
Easy Level
In this level, you will read the data from prices.txt (see additional files),  compute the total price of all items, and count the total number of purchased items.

! If you don't know how to deal with non integer characters, remove them manually from the file !

Medium Level
In this level, we will extend the program to skip rows that contain anything other than a number in the code. (Modify your program in such a way that all rows that contain something else than a number, are skipped.)

```Py
import pandas as pd
prices = pd.read_csv('/content/prices.txt', header=None)
prices_column_names = ['Price']
prices.columns = prices_column_names
prices

prices = prices.drop(prices.index[[1, 4, 7]])

prices['Price'] = prices['Price'].astype(float)
prices.sum()

counts = prices['Price'].value_counts()
print(counts.sum())
```
