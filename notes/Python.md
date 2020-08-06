## Python {docsify-ignore}

- 更换pip源
	- 临时配置：`pip(pip3) install [package-name] -i https://pypi.tuna.tsinghua.edu.cn/simple/`
	- 设为默认配置：`pip(pip3) install -U pip` `pip(3) config set global.index-url https://pypi.tuna.tsinghua.edu.cn/simple/`
- 卸载包依赖
	- 找出包依赖：`pip(3) show [package-name]`
	- 依次卸载包依赖： `pip(3) uninstall [package-name] [package-name] ...`

- 寻找质数（跳出循环）,如果内层循环正常结束，则运行`else`语句，如果中途`break`，则跳过`else`语句
```python
#查找指定范围内的质数

import math

def primeNumber(n,m):
    primeList = []
    def prime(n,m):
        for number in range(n,(m+1)):
            for divisor in range(2,int(math.sqrt(number))+1):
                if number%divisor != 0:
                    continue
                else:
                    break
            else:
                primeList.append(number)
        #print(primeList)
        return primeList
    if n > m:
        print("Be sure n<m")
    if n > 2:
        prime(n,m)
    else:
        primeList = [2]
        prime(3,m)
```
---
