# clean-baidutieba
删除自己在百度贴吧的发帖和回复

# requirements

`sudo pip3 install -r requirements.txt -i https://pypi.mirrors.ustc.edu.cn/simple/`

或者

`sudo pip3 install requests beautifulsoup4 lxml -i https://pypi.mirrors.ustc.edu.cn/simple/`

# usage

一共有3次输入

1. 刚开始输入cookies,注意格式: `Cookie: xxx=xxx; ... `直接从chrome里访问以下tieba.baidu.com然后把request headers中view source,把cookie一行复制过来就可以

2. 获取发表的帖子和发表的回复前有两次输入，输入的是json文件名，默认程序执行目录，这个是为了让第二次启动这个程序的时候加载json。第一次打开直接按Enter

3. 第一次爬完后会有2个xxxfail.json,然后每12h后程序加载这两个文件再次尝试删除，这两个文件每次删除遍历结束会重写

# todo

有个错误码不知什么情况，230308，据说是tbs不对。。
