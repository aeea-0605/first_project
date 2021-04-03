# EDA 2 : WEEKDAY_genres

```python
dfs = pd.concat([mon_df, tue_df, wed_df, thu_df, fri_df, sat_df, sun_df, full_df], axis=1)
dfs.index.name="genres"
dfs.columns.name="weekday"
dfs.fillna(0)

dfss = dfs/dfs["counts"].sum()
dfss = dfss.drop(columns=["counts"])
dfss
```

![EDA%202%20WEEKDAY_genres%204e3f65da412542909bd7659967fa1cbd/Untitled.png](EDA%202%20WEEKDAY_genres%204e3f65da412542909bd7659967fa1cbd/Untitled.png)

```python
plt.figure(figsize=(10,10))
sns.heatmap(dfss, cmap="RdYlGn_r", annot=True, fmt='.3f')
plt.title('특정요일의 장르 분포', fontsize=20)
plt.show()
```

![EDA%202%20WEEKDAY_genres%204e3f65da412542909bd7659967fa1cbd/Untitled%201.png](EDA%202%20WEEKDAY_genres%204e3f65da412542909bd7659967fa1cbd/Untitled%201.png)