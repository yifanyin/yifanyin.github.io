---
title: "Pandas"
tags:
- python
- how-to
---

I am unable to leave pandas because I work with catalogs. But I hear good things about [xarray](https://docs.xarray.dev/en/stable/)

# Basic
## Dataframes
- Change column name: `emme14.rename(columns={'LAT':'lat', 'LON':'lon', 'MwCorr': 'Mw'}, inplace=True)`
- Make a datetime column with available columns: `emme14['datetime'] = pd.to_datetime(emme14[['YEAR', 'MONTH', 'DAY', 'HOUR', 'MINUTE', 'SECOND']])`
- Sort by values: `DataFrame.sort_values(by='column name', axis=0, inplace=True)`

# Row iteration
## iterrow
Iterate over DataFrame rows as (index, Series) pairs.
```python
for i, row in df.iterrow():
	...
```

## itertuple
Iterate over DataFrame rows as namedtuples