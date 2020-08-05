## Python {docsify-ignore}

- 更换pip源
	- 临时配置：`pip(pip3) install [package-name] -i https://pypi.tuna.tsinghua.edu.cn/simple/`
	- 设为默认配置：`pip(pip3) install -U pip` `pip(3) config set global.index-url https://pypi.tuna.tsinghua.edu.cn/simple/`
- 卸载包依赖
	- 找出包依赖：`pip(3) show [package-name]`
	- 依次卸载包依赖： `pip(3) uninstall [package-name] [package-name] ...`
---
