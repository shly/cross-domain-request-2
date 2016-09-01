# cross-domain-request-2-JSONP
## 跨域请求解决方案二 JSONP

##解决方案原理
jsonp，即json+padding
利用&lt;script>标签没有跨域限制的“漏洞”，来达到与第三方通讯的目的。
当需要通讯时，动态创建script标签，src指向要请求的数据的地址，并指定一个回调函数来接收，如

    script.src = 'http://localhost:4000/data.json?callback=handleResponse';

响应的数据格式为

    handleResponse({"name","value"});

## DDEMO说明
http://localhost:3000下的app.html请求http://localhost:4000下的data.json

##DEMO使用方式
1 分别在a文件夹下和b文件夹下执行 npm install
2 分别启动服务器 npm start 
3 a服务器端口号是3000，b服务器端口号为4000 
4 访问localhost:3000/app.html
