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

## 命名规范
```js
[
    {
      value: 'WIP',
      name: '💪  WIP:      Work in Progress',
    },
    {
      value: 'feat',
      name: '✨  feat:     A new feature',
    },
    {
      value: 'fix',
      name: '🐞  fix:      A bug fix',
    },
    {
      value: 'refactor',
      name: '🛠  refactor:  A code change that neither fixes a bug nor adds a feature',
    },
    {
      value: 'docs',
      name: '📚  docs:     Documentation only changes',
    },
    {
      value: 'test',
      name: '🏁  test:     Add missing tests or correcting existing tests',
    },
    {
      value: 'chore',
      // prettier-ignore
      name: '🗯  chore:     Changes that don\'t modify src or test files. Such as updating build tasks, package manager'
    },
    {
      value: 'style',
      // prettier-ignore
      name: '💅  style:    Code Style, Changes that do not affect the meaning of the code (white-space, formatting, missing semi-colons, etc)'
    },
    {
      value: 'revert',
      name: '⏪  revert:   Revert to a commit',
    },
  ],
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
## 学习资料
* [在线练习Git使用](https://learngitbranching.js.org/?locale=zh_CN)
* [廖雪峰：史上最浅显易懂的Git教程](https://www.liaoxuefeng.com/wiki/896043488029600)

# Git分支
多人协同，离不开分支的支持

不同人在不同的开发分支上进行工作，开发完成后将内容汇入主分支或公共开发分支
## 命名规范
通常开发分支前缀
```json
{
    "prefixes": [
        "feature",
        "fix",
        "hotfix",
        "release"
    ],
}
```
## 创建分支
**创建**
```sh
git branch newBranchName
```
切换
```sh
git checkout otherBranchName
```
创建并切换
```sh
git checkout -b newBranchName
```
## 合并分支
* 此时可能会遇到冲突的问题，冲突会导致无法合并
* 出现冲突的情况有很多种，这里不一一列举，大家后续遇到问题，利用搜索引擎解决
* 造成冲突的原因往往也是由于不规范的开发方案导致的

### merge

### rebase

### Merge PullRequest

# GitHub
* 开源协作社区
* 提供Git仓库托管服务
## [注册](https://github.com/join?ref_cta=Sign+up&ref_loc=header+logged+out&ref_page=%2F&source=header-home)
* 提供邮箱就行

## 创建远程仓库

## 推送本地存储库
```sh
git add remote remoteUrl
```
```sh
git push -u originName branchName
# 等价于
git push --set-upstream originName localBranch:remoteBranch
```

## 拉取远程分支

**创建并更新本地远程分支**
```sh
git fetch
```

```sh
git pull
```

```sh
git pull originName remoteBranch：LocalBranch
```
# 多人协同开发实践
以GitHub为例

## Fork
## PR
>pull request

## Code Review

## Merge PullRequest

# 练习
* 提交PR