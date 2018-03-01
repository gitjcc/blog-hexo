categories: git&github
title: Git-Cheat-Sheet
---

* content
{:toc}

% Git-Cheat-Sheet
% JCC
% Jan 13, 2017

<!--more-->

# 代码仓库

## 工作流程

![](http://c163img.nos-eastchina1.126.net/bg2015120901.png)

- 远程仓库
- 本地仓库
- 暂存区
- 工作区

## 远程仓库

```
$ git remote -v
  origin  https://github.com/xbcx/xstarp.git (fetch)
  origin  https://github.com/xbcx/xstarp.git (push)
```

## 本地仓库

```
$ git branch -vva
* jcc                     a8f6410 [origin/jcc] Merge pull request #23
  remotes/origin/dev      a8f6410 Merge pull request #23 from xbcx/mmm
  remotes/origin/master   ae4ffdb Merge pull request #27 from xbcx/hotfix
```

## 暂存区

```
$ git commit -m 'demo'
  [jcc cf11507] 'demo'
  1 file changed, 53 insertions(+)
```

## 工作区

```
$ git add .
```


# 常用命令

## 命令清单

- git clone
- git fetch
- git merge
- git pull
- git add
- git commit
- git push
- git remote

## 命令详解

[Git远程操作详解](http://www.ruanyifeng.com/blog/2014/06/git_remote)

## 命令详解

- 合并
- git merge branch-other
- 有冲突的时候感觉不好用


- 添加
- git add file/dir
- git add .

## 命令详解

- 删除
- git rm file/dir

- 提交
- git commit -m 'message'
- git commit -am 'message2'


# 工作流程

## 基本流程

- 新建代码库
- 新建本地分支
- 增加/修改/删除文件
- 提交到暂存区
- 提交到本地仓库
- 本地仓库与远程同步

## 新建代码库

- git init [project-name]
- git clone [url]
- webstorm/phpstorm checkout from vision contrl


## 新建本地分支

- git branch [branch-name]
- git checkout [branch-name]

## 增加/修改/删除文件


- 在工作区修改
- 提交修改到暂存区
- git add .


- 撤销修改
- git checkout [file]
- git reset [file]/[commit]/HEAD^(HEAD^^/HEAD~3)


## 提交暂存区内容到本地仓库

- git commit -m '00'
- git commit -am '00'

## 本地仓库与远程同步

- git push
- git pull
- git fetch [remote]
- git merge [branch]


# 分支管理策略

## git flow

- 长期分支：master + dev
- 临时分支：feature + hotfix

## github flow

- 长期分支：master
- 临时分支：其他

## gitlib flow

- 长期分支：master + pre-production + production
- 临时分支：其他


# 参考

## 参考链接

- [Git 使用规范流程](http://www.ruanyifeng.com/blog/2015/08/git-use-process.html)

- [Git远程操作详解](http://www.ruanyifeng.com/blog/2014/06/git_remote)

- [常用 Git 命令清单](http://www.ruanyifeng.com/blog/2015/12/git-cheat-sheet.html)

- [Git教程-廖雪峰](http://www.liaoxuefeng.com/wiki/0013739516305929606dd18361248578c67b8067c8c017b000/00137621280731812dec22ecc9b44f4b2ca1c680f181a5b000)

- [Git-Book](https://git-scm.com/book/zh/v2)

