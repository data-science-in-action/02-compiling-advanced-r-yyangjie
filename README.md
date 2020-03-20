# 02-compiling-advanced-r-yyangjie
---
title: "Problems and Solutions"
author: "Jie Yang"
data:2020/3/20
---

1.> 
Error in readRDS(dest) : 读取链结时发生了错误
Error in install.packages : 读取链结时发生了错误

解决方法：重新设置镜像  Tools-global options-packages -change(China)

2.>
错误: 找不到对象'.libP'
停止执行

解决方法：重新设置安装路径
> .libPaths(c("Your path",.libPaths()))
> .libPaths()

3.提示缺什么包就安装什么包,安装Rtools

4.>Quitting from lines 96-103 (Functionals.Rmd) 
Error in loadNamespace(name) : 不存在叫'emo'这个名字的程辑包
Calls: local ... loadNamespace -> withRestarts -> withOneRestart -> doWithOneRestart
停止执行
Error in Rscript_render(f, render_args, render_meta, add1, add2) : 
  Failed to compile Functionals.Rmd
Calls: <Anonymous> -> render_new_session -> Rscript_render
停止执行

解决方法 ：
devtools::install_github("hadley/sloop")
devtools::install_github("hadley/emo")

5.https://yihui.org/tinytex/#for-r-users)(The
>install.packages('tinytex')
>tinytex::install_tinytex()
>tinytex::pdflatex('test.tex')

更新中...
