---
title: "[git] Vscode继承git的使用"
date: 2017-08-30T01:37:56+08:00
lastmod: 2021-10-3
draft: false
tags: ["preview", "中文", "tag-1"]
categories: ["中文"]
author: "superfeiyu"


---

>Vscode继承git的配置。

# VScode安装
1. 下载VSCode官网：https://code.visualstudio.com/，按照自己电脑系统可以下载相应的Window,Linux,macOS,这里要注意的是Stable是
    稳定版，而insider是内部会员预览版本，本质就是和Beta测试版本一个意思，下载完成安装即可！
2. 下载Git官网：https://git-scm.com/， 切记如果对VSCode的配置不是很熟，一定要先安装VScode,然后安装Git,在安装git的下一步中有一
    步很重要，就是Choosing the default editor used by Git选在use Visual  Studio Code as Git's default editor(这一步很重要)，
    然后下一步安装成功!
3. 打开VSCode,然后在扩展中下载两个重要的插件(Chinese(Simplified)Language pack)中文汉化包，和GieLeans-Git supecharged两个插件
    能够很好的帮助你进行开发。

# Git在VSCode中的使用
1. 在VSCode中打开Git终端两种方式：（1） 查看—》终端 （2）终端-》新终端

2.  # 1.将代码上传到GitHub的默认main分支（新）
    1. git --version    #查看版本
    2. git config --global init.defaultBranch main   #git在2.28.0上，重新设置git默认分支为main
    3. git config --global user.name "推送者仓库名字"
    4. git config --global user.email "推送者仓库邮箱地址"
    5. git config --global user.password "推送者仓库密码"
    6. git config --global http.sslVerify "false"  网络不稳定无法推送，解除ssl验证
    7. git config          http.proxy http://127.0.0.1:2334    # 设置当前代理
    8. git config --global http.proxy http://127.0.0.1:2334 #设置全局代理 
    9. git config            --unset http.proxy  # 取消当前代理
    10. git config --global --unset http.proxy    #取消全局代理
    11. git config http.proxy socks5://127.0.0.1:10809    #设置socks5代理

    ssh-keygen -t rsa -C "xxx@xxx.com"
    --------------------------------------------------------------------    
    # 2.在执行提交操作即可
    1. git init       //工作空间创建.git文件夹（默认隐藏了该文件夹）
    2. git add .      //添加到暂存区
    3. git commit -m "你的提交注释注释"
    4. git remote add origin http://xxxxxxxxx.git   //本地仓库和远程github关联
    5. git pull --rebase origin main  //远程有readme.md，拉一下
    6. git push -u origin main        //代码合并
   
