## Merge

`pd.concat()`와 다른점 `.merge()`는 `keys`를 통한 결합임


``` python
pd.merge(
    left,
    right,
    how="inner",
    on=None,
    left_on=None,
    right_on=None,
    left_index=False,
    right_index=False,
    sort=True,
    suffixes=("_x", "_y"),
    copy=True,
    indicator=False,
    validate=None,
)
```

``` python
left = pd.DataFrame(
    {
        "key": ["K0", "K1", "K2", "K3"],
        "A": ["A0", "A1", "A2", "A3"],
        "B": ["B0", "B1", "B2", "B3"],
    }
)
right = pd.DataFrame(
    {
        "key": ["K0", "K1", "K2", "K3"],
        "C": ["C0", "C1", "C2", "C3"],
        "D": ["D0", "D1", "D2", "D3"],
    }
)
result = pd.merge(left, right, on="key")
```
default는 inner join

![image](https://user-images.githubusercontent.com/71545915/209614781-4821fcdd-b2b5-484c-ae28-3a38fcec650f.png) 


