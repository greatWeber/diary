# git基本操作

## clone GitHub上面的项目

1. 先在github创建一个项目，记得把`Initialize this repository with a README`给勾上
2. 在本地目录中运行`git clone [项目url]`
3. 设置git的邮箱和名称. `git config --global user.name "name"`;`git config --global user.email  "youremail"`
4. 第一次提交时，会弹出登录github的窗口

## git 常用命令

### git add 
> git add 命令可将该文件添加到缓存

```js
git add . //添加所有修改的文件
```

### git status
> git status 命令用于查看项目的当前状态。

```js
git status -s // -s 参数，以获得简短的结果输出。如果没加该参数会详细输出内容
```

### git commit
> 使用 git add 命令将想要快照的内容写入缓存区， 而执行 git commit 将缓存区内容添加到仓库中。

```js
git commit -m "注释" //使用 -m 选项以在命令行中提供提交注释
git commit -am "注释" //跳过git add命令，直接提交
```


### git push
> git push 是将本地库中的最新信息发送给远程库

### git pull
> git pull 是从远程获取最新版本到本地，并自动merge

### git diff
> git diff 来查看执行 git status 的结果的详细信息。

```js
git push origin master //把本地master分支的最新修改推送至远程库，现在，你就拥有了真正的分布式版本库！
```

1. 尚未缓存的改动：git diff
2. 查看已缓存的改动： git diff --cached
3. 查看已缓存的与未缓存的所有改动：git diff HEAD
4. 显示摘要而非整个 diff：git diff --stat


### git rm
> git rm 删除文件

```js
git rm -f <file> //如果删除之前修改过并且已经放到暂存区域的话，则必须要用强制删除选项 f

git rm --cached <file> //如果把文件从暂存区域移除，但仍然希望保留在当前工作目录中，换句话说，仅是从跟踪清单中删除，使用 --cached 选项即可

git rm –r * //递归删除，即如果后面跟的是一个目录做为参数，则会递归删除整个目录中的所有子目录和文件

```

## 参考
1. [廖雪峰git教程](https://www.liaoxuefeng.com/wiki/0013739516305929606dd18361248578c67b8067c8c017b000)

2. [菜鸟教程](http://www.runoob.com/git/git-tutorial.html)