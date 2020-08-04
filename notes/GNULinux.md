## GNULinux {docsify-ignore}

### Bash
- yum完全卸载依赖
    1. 找出安装包时的命令(command-number)：`sudo yum history list [package-name]`; 
    2. 恢复该命令之前的状态：`sudo yum history undo [command-number]`;

---
### Vim
- 缩进
  - 解决粘贴外部文本时缩进混乱：粘贴前：`:set paste` ; 粘贴后：`:set nopaste`;

---
 
