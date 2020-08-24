## GNULinux {docsify-ignore}

### Configure
- 修改`hosts`文件
	- hosts文件所在位置：`/etc/hosts`
	- windows中所在位置：`C:\Windows\System32\drivers\etc\hosts`,如果文件名是`host`,则需要改成`hosts`
	- 修改格式：`127.0.0.1	google.com(中间至少隔一个空格)`
	- windows下的辅助命令：`ipconfig /release(执行之后会断网)` `ipconfig /flushdns`,用于刷新DNS缓存
	- 文件中应只包含`IP+域名`，不需要添加端口、协议和主机名等，访问时在域名后添加端口
---

### Bash
- yum完全卸载依赖
    1. 找出安装包时的命令(command-number)：`sudo yum history list [package-name]`; 
    2. 恢复该命令之前的状态：`sudo yum history undo [command-number]`;
- `sudo`提示`command not found`
	1. `sudo`默认执行系统命令，执行其他命令可能导致`command not found`;
	2. 使用`sudo vim /etc/sudoers`打开文件修改`env_reset`参数为`!env_reset`，然后`:wq!`退出;
	3. 使用`vim ~/.bashrc`打开用户配置文件，加上`alias sudo='sudo env PATH=$PATH`，退出，使用`source ~/.bashrc`重新加载;

---
### Vim
- 缩进
  - 解决粘贴外部文本时缩进混乱：粘贴前：`:set paste` ; 粘贴后：`:set nopaste`;

---
 
