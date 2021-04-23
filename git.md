##### .gitconfig 文件中配置

```
[user]
	name = 张威
	email = 294341493@qq.com
[alias]
	ac = commit -am
	ad = add .
	br = branch
	brd = branch -d
	brD = branch -D
	ch = checkout
	chb = checkout -b
	chd = checkout dev
	chl = checkout develop
	chm = checkout master
	chr = checkout --
	cl = clone
	co = commit -m
	com = commit -m
	di = diff
	lo = log --color --graph --pretty=format:'%Cred%h%Creset -%C(yellow)%d%Creset %s %Cgreen(%cr) %C(bold blue)<%an>%Creset' --abbrev-commit
	me = merge
	med = merge dev
	mel = merge develop
	pl = pull
	ps = push origin
	psb = push --set-upstream origin
	psd = push origin -d
	psm = push -u origin master
	re = remote -v
	rer = remote rm origin
	rea = remote add origin
	ss = stash
	ssl = stash list
	ssp = stash pop
	st = status
```

##### 检查是否已经存在 SSH Key

> 通常 SSH Key 会默认生成在/Users/username/.ssh 目录下，查看此目录下是否存在.ssh 文件夹及相关目录

##### 生成 Key

1. 在控制台输入: ssh-keygen -t rsa
2. 一路回车，完成后，私钥放在~/.ssh/id_rsa 文件，公钥放在~/.ssh/id_rsa.pub 文件
3. 复制公钥，关联到 Github/Gitlab 即可

##### Gitlab 问题

- Gitlab 报错:
  Unable to negotiate with xxx.xx.xxx.x port 22: no matching host key type found. Their offer: ssh-dss
- 解决方法:
  在~/.ssh 目录下创建 config 文件 touch config && vi config
  Host git.xxxxxxx.com
  HostKeyAlgorithms ssh-dss
