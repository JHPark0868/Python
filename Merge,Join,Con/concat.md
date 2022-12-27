## Concat 

Dataframe , Series 를 결합할 때

`pd.merge()`랑 다른 점은 `.merge()`는 df 간 결합해야할 key 가 존재해야함

## pandas.concat 
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

|Parameter | 기본값   | 의미   |
|----|-----|-----|
|`objs`| a sequence or mapping Series or Dataframe object <br>  | B0  |
|  `axis` | `0`, `1` |결합방향, `=0` 아래로(행방향) , `=1` 옆으로(열방향) default 0 |
|  `join` | A2  | B2  |

df 

``` python
result = pd.concat([df1, df2, df3])
```
![image](https://user-images.githubusercontent.com/71545915/209612401-94d210cc-c3bb-4adf-be3a-ce147c8a9499.png)




``` python
result = pd.concat(frames, keys=["x", "y", "z"])
```
![image](https://user-images.githubusercontent.com/71545915/209612533-07e4b17f-299e-45fd-9917-299811045f90.png)

keys 를 통한 hierarchical index (multi index랑 다른가? ) 부여, .loc을 통한 인덱싱 
``` python
In [7]: result.loc["y"]
Out[7]: 
    A   B   C   D
4  A4  B4  C4  D4
5  A5  B5  C5  D5
6  A6  B6  C6  D6
7  A7  B7  C7  D7
```
