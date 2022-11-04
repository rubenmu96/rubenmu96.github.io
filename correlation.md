---
layout: page
mathjax: true
permalink: /correlation/
---

Script for finding the correlation between features. Only values equal or greater than p are printed out. 
```python
def correlation(data, p):
    print('Number of features:', len(data.columns))
    columns1 = columns2 = data.columns
    for coli in columns1:
        columns2 = columns2.drop(coli)
        for colj in columns2:
            corr = data[coli].corr(data[colj])
            if np.abs(corr) >= p:
                print('Correlation between ' + coli + ' and ' + colj + ' is ' + str(np.round(corr,3)))
```
