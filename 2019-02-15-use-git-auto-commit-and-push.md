# 使用 Git 实现自动 Commit 和 Push

工作和生活中常常会把代码和文本文件保存在 Github 上。每次写完一个新功能或者写完一篇新文章的时候，都需要执行 git commit 和 git push 的命令，将本地代码或文件合并到远程的服务器，方便在家和公司电脑文件的一致性。

经常重复性的输入这两个命令，唯一变化的只是 commit 的日志信息不同，其他的代码都是相同的。写了一个批处理的命令，只要双击该文件，输入 commit 日志信息就能实现自动git commit 和 push 的功能，节省了大量写重复代码的时间。

``` git
set /p commit_log=请输入 commit 日志信息:
git status
git add -A
git commit -m "%commit_log%"
git push origin master
pause
```

