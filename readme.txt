Git问题解决方法汇总

1.git clone git位置

想使用Git把档案获取到某个已存在的目录下错误 fatal: destination path ‘文件夹名’ git clone already exists and is not an empty directory

解决办法，在文件夹目录下执行以下命令：

git init git remote add origin gitpath git fetch git branch master origin/master git checkout master

接着可以看到Git上的.bashrc出现在本地目录下

2.在学习git的时候，发现不能使用git clone从github.com下载，报了个ssl错误。

Cloning into cancan... error: SSL certificate problem, verify that the CA cert is OK. Details: error:14090086:SSL routines:SSL3_GET_SERVER_CERTIFICATE:certificate verify failed while accessing https://github.com/ryanb/cancan.git/info/refs

fatal: HTTP request failed

在网上找了一下，比较简单的解决办法：

git config --global http.sslVerify false
