## Git {docsify-ignore}

- [廖雪峰的Git教程](https://www.liaoxuefeng.com/wiki/896043488029600)
- 使用git后文件可能处于的位置：`工作区` `缓存区` `本地仓库` 
- 提交所有修改到缓存区：`git add .` 或 `git add --all`
- 查看文件区别
	- 查看文件在工作区与缓存区的区别：`git diff [文件名]`
	- 查看文件在缓存区与本地仓库的区别：`git diff --cached [文件名]` 
	- 查看文件在工作区与本地仓库（最近一次提交）的区别：`git diff HEAD [文件名]`
- 查看提交历史：`git log` 或 `git log --pretty=oneline(每个提交输出一行)`，可得到`版本号` 和 `提交备注`
- 版本回退：`git reset --hard [版本号]`，也可使用`HEAD^(上一个版本)` `HEAD^^(上上个版本)` 和`HEAD~100(往上第100个版本)` 来代替`[版本号]` 
- 版本回退后再向前：通过`git reflog` 找出历史命令，进而找出之前的版本号
- 本地与远程库的连接
  1. 远程新建库
  2. 本地新建目录，进入目录，初始化`git init `
  3. 本地与远程关联：`git remote add origin git@github.com:michaell/learngit.git`，翻译过来就是”git远程添加origin（默认库名），地址是git@......“
  4. 关联之后就可将本地内容推送到远程库：`git push -u origin master`， 翻译过来就是”git推送到origin库的master分支（默认分支）“，其中`-u`参数使得本地与远程库origin的master分支绑定，以后可直接使用`git push`

- 本地直接克隆远程库：`git clone git@github.com:michaell/gitskills.git(速度快)`或者`git clone https://github.com/michaell/gitskills.git`
- 强制push，覆盖远程库中的文件：`git push -u origin master -f`
- 无法pull远程库：`git pull origin master --allow-unrelated-histories`
- 直接提交（合并提交到缓存区这一步）：`git commit -am "[message]"`
- 本地库(新用户)与远程库（github）的信任机制
	- 本地库默认相信诸如github之类远程库（只会给出一个小小警告）
	- 远程库并不相信本地库，需要ssh连接，故需要本地用户在用户根目录下创建SSH Key，并将公钥上传到github，实现认证和加密传输
	- 本地用户还需配置用户名和邮箱地址，用于区分不同的提交人
	- SSH Key是针对用户的，不是针对仓库
- 打标签：`git tag -a [tag-name] -m [message]`
- 推送标签：`git push origin [tag-name]`

---

