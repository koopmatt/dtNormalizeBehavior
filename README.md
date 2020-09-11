# dtNormalizeBehavior
behavior of pandas 1.1.1 dt.normalize() on pre-epoch dates

**dt.normalize() on pre-epoch increments DAY by ONE.**


```
import pandas as pd
print(pd.__version__)
df = pd.DataFrame({'year': [1969, 2016],'month': [1, 1],'day': [1, 1],'hour': [9, 9]})
df=pd.to_datetime(df)
df
df.dt.normalize()
```

```
df

Out[7]:
0   1969-01-01 09:00:00
1   2016-01-01 09:00:00
dtype: datetime64[ns]

df.dt.normalize()

Out[8]: 
0   1969-01-02
1   2016-01-01
dtype: datetime64[ns]
```
