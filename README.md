# 02-compiling-advanced-r-yyangjie
---
title: "Problems and Solutions about Compiling Advanced R "
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

3.>Quitting from lines 96-103 (Functionals.Rmd) 
Error in loadNamespace(name) : 不存在叫'emo'这个名字的程辑包
Calls: local ... loadNamespace -> withRestarts -> withOneRestart -> doWithOneRestart
停止执行

解决方法 ：
在R studio terminal 或者Git bash 上输入
$git config --global http.ssBackend "openssl"
$git config --http.sslCAInfo D:/adv-r-master
>install.packages("devtools")
>library(devtools)
>devtools::install_github("hadley/sloop")
>devtools::install_github("hadley/emo")


4.>
Quitting from lines 209-221 (Big-picture.Rmd) 
错误: The dbplyr package is required to communicate with database backends.

解决方法：Install.packages("dbplyr")

5.>
Quitting from lines 233-234 (Perf-measure.Rmd) 
错误: `ggbeeswarm` must be installed to use `type = "beeswarm"` option.

解决方法：Install.packages("ggbeeswarm")

6.>
Quitting from lines 77-84 (Rcpp.Rmd) 
Error in sourceCpp(code = code, env = env, rebuild = rebuild, cacheDir = cacheDir,  : 
  Error 1 occurred building shared library.
Calls: local ... withVisible -> eval -> eval -> cppFunction -> sourceCpp

解决方法：Install.packages("Rcpp")

7.缺少包就安装包，缺少字体就下载字体。

8.>
报错及解决参考：
http://brettklamer.com/diversions/statistical/compile-hadleys-advanced-r-programming-to-a-pdf/
https://github.com/statcomputing/compiling-advanced-r-Kun73/blob/master/README.md
https://yihui.org/tinytex/#for-r-users)(The
