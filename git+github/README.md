# Git
## 简介
>Git是目前世界上最先进的分布式版本控制系统（没有之一）。

通俗：管理项目代码，记录每一处的变动

**简单演示Git的作用**
* 演示diff
* 历史变动
* 追踪改动人员

### 推荐的Vs Code插件
* Git History
* Git Graph
* GitLens

注：先演示命令行，再演示GUI插件效果

## 初始化本地仓库
```sh
git init
```

修改一些文件看看

```sh
git status
```
## 工作区&暂存区&版本库
* 本地修改->工作区
* 提交本地修改->暂存区
* 提交暂存区的内容->版本库

工作区默认和暂存区的内容进行比较

## 添加到暂存区&跟踪文件
暂存区：
```sh
git add filename

git add *
```


## 查看变动
```sh
git diff filename
```

## 提交暂存区内容
```sh
git commit -m "msg"
```
## 查看提交日志
```sh
git log
```
```sh
git reflog
```

## 撤销修改

会退到最近的一次 `commit` 或者 `add`
```sh
git checkout -- filename
```

## 版本回退
```sh
git reset HEAD^

# 变动内容回到暂存区
git reset --hard HEAD^
```

通过`git reflog`查询回退前的commitId

```sh
git reset --hard commitId
```

## 分支
```sh

```

### 创建分支
```sh

```
## 学习资料
* [在线练习Git使用](https://learngitbranching.js.org/?locale=zh_CN)
* [廖雪峰：史上最浅显易懂的Git教程](https://www.liaoxuefeng.com/wiki/896043488029600)

# GitHub

# 多人协调实践

# 作业
* 提交PR