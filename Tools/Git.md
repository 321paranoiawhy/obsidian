#Git
# Reference

- [Git Command Exploer](https://gitexplorer.com/)
- [Pro Git](https://git-scm.com/book/en/v2)
- [Git 教程 - 廖雪峰](https://www.liaoxuefeng.com/wiki/896043488029600)
- [常用 Git 命令清单 - 阮一峰](https://www.ruanyifeng.com/blog/2015/12/git-cheat-sheet.html)
- [Git 原理入门](https://www.ruanyifeng.com/blog/2018/10/git-internals.html)

# 克隆远程指定分支到本地

```bash
# 克隆远程 dev 分支到本地
git clone <url> -b dev

# 克隆远程 master / main 分支到本地 (默认分支)
git clone <url>
```

# 查看远程分支

```bash
git remote -v
```

# 同步远程分支列表

```bash
git fetch -p
```

# 删除远程分支

```bash
# 删除远程 remoteBranchName 分支
git push origin --delete remoteBranchName
```

# 查看本地分支

```bash
git branch
```

# 查看本地分支状态

```bash
git status
```

# 删除本地分支

```bash
# 删除本地 local 分支
git branch -delete local # git branch -d local

# 强制删除本地 local 分支
git branch -D local
```

# 切换本地分支

```bash
# 切换至本地 another 分支 (检出)
git checkout another
```

#  本地分支推送到远程指定分支

```bash
# 本地 local 分支推送到远程 origin 分支
git push origin local:origin
```

# 拉取远程指定分支并合并到本地分支

```bash
# 拉取远程 dev 分支并合并到本地分支
git pull origin dev
```

# 本地分支合并至远程分支

```bash
# 切换至本地 local 分支
git checkout local
# 拉取远程 local 分支最新代码
git pull origin local

# 切换至本地 dev 分支
git checkout dev
# 拉取远程 dev 分支最新代码
git pull origin dev
# 将本地 local 分支代码合并至本地 dev 分支
git merge local
# 将本地 dev 分支代码推送至远程 dev 分支
git push origin dev
```