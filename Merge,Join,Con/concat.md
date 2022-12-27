## Concat 

df 

``` python
result = pd.concat([df1, df2, df3])
```
![image](https://user-images.githubusercontent.com/71545915/209612401-94d210cc-c3bb-4adf-be3a-ce147c8a9499.png)

### pandas.concat 
``` python
pd.concat(
    objs,
    axis=0,
    join="outer",
    ignore_index=False,
    keys=None,
    levels=None,
    names=None,
    verify_integrity=False,
    copy=True,
)
```

|Parameter | 입력   | 설명   |
|----|-----|-----|
|`objs`| a sequence or mapping Series or Dataframe object <br>  | B0  |
|  `axis` | `=0`: index 행방향 아래로 <br> `=1`: columns 열방향 옆으로 |결합방향, default 0 |
|  `join` | A2  | B2  |


``` python
result = pd.concat(frames, keys=["x", "y", "z"])
```
![image](https://user-images.githubusercontent.com/71545915/209612533-07e4b17f-299e-45fd-9917-299811045f90.png)

