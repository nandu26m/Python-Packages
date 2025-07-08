
# 🐼 Pandas Cheat Sheet (2025 Master Version)

## 1. Data Import

```python
import pandas as pd

df = pd.read_csv('file.csv')
df = pd.read_excel('file.xlsx', sheet_name='Sheet1')
df = pd.read_sql(query, connection)
df = pd.read_json('file.json')
df = pd.read_parquet('file.parquet')
df = pd.read_html('page.html')[0]
df = pd.read_clipboard()
```

## 2. Data Export

```python
df.to_csv('output.csv', index=False)
df.to_excel('output.xlsx', sheet_name='Sheet1')
df.to_parquet('output.parquet')
df.to_json('output.json', orient='records')
df.to_sql('table_name', con=connection, if_exists='replace')
```

## 3. Data Selection & Indexing

```python
df['column']
df[['col1', 'col2']]
df.loc[0, 'col']
df.iloc[0:5, 0:2]
df.at[0, 'col']
df.iat[0, 1]
df.query('col > 5')
df[df['col'].isin(['A', 'B'])]
df.set_index('id')
df.reset_index()
df.xs(key=2024, level='year')
```

## 4. Data Cleaning

```python
df['col'].str.lower()
df['col'].str.strip()
df['col'].str.replace(r'\s+', '_', regex=True)
df['col'].str.contains('pattern')
df['col'].str.extract('(\d+)')
df['col'].str.split(',').str[0]
df['col'].str.len()

df['col'].replace({'old': 'new'})
df.dropna()
df.fillna(0)
df.duplicated()
df.drop_duplicates()
```

## 5. Data Transformation

```python
df['new'] = df['col'].apply(lambda x: x * 2)
df['new'] = df['col'].map({'A': 1, 'B': 2})
df.assign(new_col=lambda x: x['col1'] + x['col2'])

df.melt(id_vars=['id'], value_vars=['A', 'B'])
df.pivot_table(values='val', index='idx', columns='cat', aggfunc='sum')
df.merge(df2, on='key', how='left')
df.sort_values(['col1', 'col2'])
df.groupby('col').agg({'col2': ['mean', 'sum']})
df.groupby('col').transform('mean')
df.groupby('col').filter(lambda x: len(x) > 2)
pd.crosstab(df['A'], df['B'])
pd.cut(df['score'], bins=3)
pd.qcut(df['score'], q=4)
```

## 6. Statistics & EDA

```python
df.describe()
df['col'].value_counts()
df['col'].nunique()
df['col'].mode()
df['col'].median()
df['col'].std()
df['col'].corr(df['col2'])
df.cov()
```

## 7. Time Series & Date Handling

```python
df['date'] = pd.to_datetime(df['date'])
df['date'].dt.year
df['date'].dt.month
df['date'].dt.day
df['date'].dt.weekday
df['date'].dt.strftime('%Y-%m-%d')

df.resample('M').mean()
df.rolling(window=7).mean()
df.shift(1)
df.asfreq('D', method='ffill')

pd.date_range('2024-01-01', periods=12, freq='M')
```

## 8. Advanced Pandas

```python
df.pipe(lambda d: d.dropna().sort_values('col'))
df.eval('col1 + col2')
df.copy(deep=True)
df.select_dtypes(include='number')
df.nlargest(5, 'col')
df.sample(n=10)
df.explode('col')
pd.get_dummies(df['category'])
```

## 9. Tips & Best Practices

- Always check `df.info()` and `df.head()` first
- Use `.copy()` when slicing (`df2 = df[condition].copy()`)
- Use `categorical` dtype to save memory
- Avoid `inplace=True`; prefer assignment for clarity
- Use method chaining to keep code clean:

```python
df.pipe(...)
  .assign(...)
  .query(...)
  .sort_values(...)
```
