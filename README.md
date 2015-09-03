# scriptkid
猪猪侠分布式扫描系统一键部署脚本

说实话，刚看到猪猪侠发布thorns的时候眼前一亮，还是很期待的，但是测试后，效果不太理想 
主要因为全端口模式扫描速度太差，可能主要是nmap的问题. 

测试了一下，扫tcp的1-65535端口，255个ip，6个服务器分发任务,没有一次能成功扫完的。有时候因为时间太长，导致celery抛一些很奇怪的错误。 

共享下这套系统的安装脚本，centos5 centos6通用，主要是 

1.判断操作系统版本,python版本 
2.如果是centos5,centos6,python2.7以下 升级python到2.7.x以上 
3.下载nmap，自动安装 
4.下载各种依赖软件 
5.下载扫描器其他软件，并运行。 


代码见https://raw.githubusercontent.com/uncia/scriptkid/master/thronsinstall.sh
