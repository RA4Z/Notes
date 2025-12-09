Power Query is a powerful data connection and data preparation technology that allows users to **discover, connect, combine and refine data** from various sources. It is and integral component of [[Excel]] and [[Power BI]]

### ETL for the Desktop
Power Query performs the "heavy lifting" of the **ETL process**
- **E (Extract):** It connects to data from hundreds of different sources
- **T (Transform):** It allows you to clean, reshape, merge, filter, pivot, unpivot and otherwise manipulate the data
- **L (Load):** It loads the cleaned data into your destination

### Useful Commands
- Get the date of the current Date-time
```Python
Date.From(DateTime.LocalNow())
```

- Add days to a date and get the date
```Python
Date.From(Date.AddDays(DateTime.LocalNow(), 15))
```
