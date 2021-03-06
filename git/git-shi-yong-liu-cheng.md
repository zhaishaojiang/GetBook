## 1. 创建仓库

### 1.1 克隆已有的仓库

```
git clone '仓库地址'   // 会创建与仓库同名的文件夹
git clone '仓库地址' '文件名'    // 会将远程仓库克隆岛指定文件夹下
```

### 1.2 在现有目录中初始化仓库

```
git init
```

## 2.  更新提交到仓库

### git add

git add 命令可将文件添加到缓存

```
git add index.html   // 将指定文件添加到缓存区
git add -A   // 全部添加到缓存区
git add .    // 同上
```

### git status

查看项目当前状态

### git diff

查看执行 git status 的结果的详细信息。

git diff 命令显示已写入缓存与已修改但尚未写入缓存的改动的区别。

* 尚未缓存的改动：git diff
* 查看已缓存的改动：git diff --cached
* 查看已缓存与未缓存的所有改动：git diff HEAD
* 显示摘要而非整个 diff：git diff --stat

git status 显示你上次提交更新后的更改或者写入缓存的改动，而 git diff 一行一行地显示这些改动具体信息。

### .gitignore

处理一些无需添加到 git 管理中的文件。\(如一些日志文件，或者编译过程中创建的临时文件等\)。

`.gitignore` 文件的格式规范如下：

* 所有空行或者\( `#` \)开头的行都会被 git 忽略。
* 可以使用标准的 `glob` 模式匹配。
* 匹配模式可以以\( `/` \)开头防止递归。
* 匹配模式可以以\( `/` \)结尾指定目录。
* 要忽略指定模式以外的文件或者目录，可以在模式前加\( `!` \)取反。

所谓的 `glob` 模式是指 shell 所使用的的简化了的正则表达式。星号\(`*`\)匹配另个或多个任意字符； `[abc]` 匹配任何一个列在方括号中的字符\(这个例子要么匹配一个字符 `a` ，要么匹配一个字符 `b` ，要么匹配一个字符 `c` \)；问号\(`?`\)只匹配一个任意字符；如果在方括号中使用短划线\(`-`\)分隔两个字符，表示所有在这两个字符范围内的都可以匹配\(比如 `[0-9]` 表示匹配所有 `0` 到 `9` 的数字\)。使用两个型号\(`*`\)表示匹配任意中间目录，比如 `a/**/z` 可以匹配 `a/z` ， `a/b/z` 或者 `a/b/c/z` 等。

### git commit

使用 git add 命令将想要快照的内容写入缓存区，而执行 `git commit` 将缓存区内容添加到仓库中。

git 为你的每一个提交记录都记录你的名字和邮箱地址，配置用户名和邮箱地址方法如下：

```
git config --global user.name 'username'
git config --global user.email test@xxx.com
```

接下来提交所有改动，使用 `git commit -m '改动说明日志'` 

### git remote

添加一个新的远程 git 仓库：`git remote add <shortname> <url>` 

查看远程仓库列表：`git remote` 

查看远程仓库地址：`git remote -v`

### git pull

`git pull origin master` 拉去远程仓库数据\( origin 为远程仓库的缩略名，master 为该仓库的指定分支\)

### git push

`git push origin master` 把本地仓库中所有添加和修改的内容添加到远程仓库\( origin 为远程仓库缩略名，master 为该仓库指定分支\)



