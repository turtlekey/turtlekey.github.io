## Nginx {docsify-ignore}

- 基本操作
	- 运行服务：`nginx`;
	- 缓和结束服务（等待当前连接完成）：`nginx -s quit`;
	- 直接结束服务：`nginx -s stop`;
	- 重载配置（配置成功则使用新配置，失败则继续使用旧配置，服务不会中断）：`nginx -s reload`.

- nginx的配置包括简单指令和块指令，其中块指令属于嵌套结构，如```{http{server{location}}}```.每一个server块通过```listen（监听端口）```和```server_name（域名/主机名）```参数的配置来区分不同的主机，同一个域名/主机名可以配置不同的端口来提供不同的服务，但同一端口只能用于一种服务。当在浏览器中输入域名（ip地址）及端口时，请求会被定位到匹配的服务上。每个server块中都有若干个location块，用于定位同一服务中的不同资源，URI支持正则表达式，所以也可用于对某一类的URI返回同一个页面。

- `nginx.conf`参考
```text
#全局配置(main)
user [www] [www];      #使用nginx服务的用户和用户组
error_log [/data/wwwlogs/error_nginx.log] [debug|info|notice|warn|error|crit|alert|emerg];  #错误日志的存放目录和级别，级别越高记录信息越少
pid [/var/run/nginx.pid];   #nginx服务的PID号，可用于查看服务信息和结束服务
......
#server配置
server {
       listen [80];  #监听端口
       server_name [_|ip地址|域名];    #当只有一个主机时，可使用[_]
       access_log [/data/wwwlogs/access_nginx.log] [combined]; #访问日志的存放目录和格式，访问日志记录访问者信息，可用于网站分析
       root [/data/wwwroot/default];      #如果匹配的location中没有自己的root指令，则会使用server中的root指令，以定位资源
       index [index.html index.htm index.php];   #用于网站主页的文件，优先级递减
       error_page [404|403|...] [/404.html|/403.html|...];      #自定义错误页面
       location /nginx_status {
              stub_status [on|off];       #是否开启状态页，nginx状态页可以查看相关连接状态
              access_log [on|off];        #是否将连接记录到访问日志
              allow [ip地址];        #允许访问状态页的ip，一般设为本机ip
              deny [all];          #拒绝其他所有ip访问
              }
       }
include [**.conf];   #引入外部配置文件          
```
       
---
