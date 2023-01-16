---
title: "Pandas"
tags:
- python
- how-to
DocumentClass: manual
---

I am unable to leave pandas because I work with catalogs. But I hear good things about [xarray](https://docs.xarray.dev/en/stable/)

# Basic
## Dataframes
- Change column name: `emme14.rename(columns={'LAT':'lat', 'LON':'lon', 'MwCorr': 'Mw'}, inplace=True)`
- Make a datetime column with available columns: `emme14['datetime'] = pd.to_datetime(emme14[['YEAR', 'MONTH', 'DAY', 'HOUR', 'MINUTE', 'SECOND']])`
- Sort by values: `DataFrame.sort_values(by='column name', axis=0, inplace=True)`
- Slice a dataframe to independant variable by adding `.copy()`

# Row iteration
## iterrows
Iterate over DataFrame rows as (index, Series) pairs.
- Return the index and the row as **series**
- Does not preserve dtype
```python
for i, row in df.iterrow():
	print(row)
```

## itertuples
- Iterate over DataFrame rows as `namedtuples`
- Return the iterator, An object to iterate over named tuples for each row in the DataFrame with the first field possibly being the index and following fields being the column values.

