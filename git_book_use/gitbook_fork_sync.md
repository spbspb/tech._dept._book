# github使用指南——在你pull request之前
#### <p align="right"> 作者：BG2DGR</p>

## 合作写书
假定这篇文章的前置文章，李雨桐同学的《如何用git写文章》已经完善了，大家都可以按照他的步骤写一篇新的文章了，且推送到自己的GitHub上面，但是gitbook是托管到三老师的GitHub上面([ArtisticZhao](https://github.com/ArtisticZhao))。想要你写的这篇文章发布，就需要向三老师的Github发起pull request。  
那么这样就会出现这样一个问题（李雨桐和陈功同学都遇到了这个问题）：在他们文章推送之前，三老师又更新了一篇文章，但是你本地的编写的环境是你fork的三老师之前的GitHub，也就是说，三老师在更新自己的GitHub，又加入了文章之后（也可能是其他同学提交了文章），你的repo并没有跟着一同更新，这是你的pull request就好产生冲突（“conflict”）。如何解决呢？

## 保证你fork的仓库最新（syncing your fork）
GitHub实际上对应着git “远程仓库”的概念。（似乎隐约记得三老师曾经提过，新建一个repo要从GitHub新建然后，然后clone到本地进行开发）。而这个过程就是为了避免手动新建仓库（repo）的时候`git init`，需要自己添加位于GitHub的远程仓库。
新的命令，显示远程仓库
```
git renote -v
```
如下图  
![](/git_book_use/gitbook_fork_sync/00.png)  
我新建一个文件夹a，并使用`git init`初始化一个gith环境，最后使用`git remote -v`查看了git的远程库，结果返回是空，当然，因为从头到尾就没涉及到远程库的问题（笑😀）  
**强调： 在图中有美元符“$”开头的是输入的命令，没有的为回显**
