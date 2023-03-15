# extract date components into new columns

## Here, InvoiceDate is a column which contains date and time and from this column we make additional columns of date, day, month, year and quarter from below methods 

### **to_datetime** convert datetime column to datetime format (if not already in datetime format) 

``` df['date'] = pd.to_datetime(df['InvoiceDate']) ```
``` df['date_column'] = df['date'].dt.date ```
``` df['day'] = df['date'].dt.day ```
``` df['month'] = df['date'].dt.month ```
``` df['year'] = df['date'].dt.year ```
``` df['quarter'] = df['date'].dt.quarter ```

# Find null values and handle them 

## find all rows with null values
``` null_rows = df.isnull().any(axis=1) ```

## drop rows with null values
``` df = df[~null_rows] ```

# get data for a particular day
```desired_date = '2010-12-01'```
``` day_data = df.loc[desired_date]```



