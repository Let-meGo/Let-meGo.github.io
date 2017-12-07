# 项目介绍

> 将新电脑的生成的ssh key添加到GitHub账户上
> 在新电脑上克隆username.github.io仓库的xxx分支到本地，此时本地git仓库处于xxx分支
> 切换到username.github.io目录，执行npm install(由于仓库有一个.gitignore文件，里面默认是忽略掉 node_modules文件夹的，也就是说仓库的hexo分支并没有存储该目录[也不需要]，所以需要install下)


## 编写博客

* 依次执行git add .、git commit -m 'back up hexo files'（引号内容可改）、git push指令，保证xxx分支版本最新
* 执行hexo d -g指令（在此之前，有时可能需要执行hexo clean），完成后就会发现，最新改动已经更新到master分支了，两个分支互不干扰！

## 最后

* 目录切换下username.github.io下，此时需要安装一下npm install，
*  最后执行hexo g、hexo s、hexo d等命令即可提交成功
