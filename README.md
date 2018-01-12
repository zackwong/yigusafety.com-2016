yigusafety.com-2016
=============

毅固防滑英文官网2016年版


域名绑定、301转向及nginx配置
-----

新建配置文件: ``sudo nano /etc/nginx/sites-available/yigusafety.com``

编辑配置文件及保存: 

    server {
        server_name yigusafety.com;
        return 301 http://www.yigusafety.com$request_uri;
    }
    server {
        server_name www.yigusafety.com;
        index index.html;
        root /srv/yigusafety.com-2016/_site;
        error_page 404 /Error.html;
    }

建立链接: ``sudo ln -s /etc/nginx/sites-available/yigusafety.com /etc/nginx/sites-enabled/``

重启nginx: ``sudo service nginx restart``


下载及生成网站
-----

1. 下载网站源码: ``git clone git://github.com/zackwong/yigusafety.com-2016.git``

2. 进入源码根目录: ``cd yigusafety.com-2016``

3. 生成网站: ``jekyll build``


开发者
---------

* Zack Wong &lt;hzzzoo@126.com&gt;

