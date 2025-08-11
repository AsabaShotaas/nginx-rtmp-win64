# nginx-rtmp-win64

* Nginx: 1.29.1  
* Nginx-Http-Flv-Module: 1.2.12  
* openssl-3.4.2
* pcre2-10.45
* zlib-1.3.1

# configure arguments
auto/configure \
    --with-cc=cl \
    --with-debug \
    --prefix= \
    --conf-path=conf/nginx.conf \
    --pid-path=logs/nginx.pid \
    --http-log-path=logs/access.log \
    --error-log-path=logs/error.log \
    --sbin-path=nginx.exe \
    --http-client-body-temp-path=temp/client_body_temp \
    --http-proxy-temp-path=temp/proxy_temp \
    --http-fastcgi-temp-path=temp/fastcgi_temp \
    --http-scgi-temp-path=temp/scgi_temp \
    --http-uwsgi-temp-path=temp/uwsgi_temp \
    --with-cc-opt=-DFD_SETSIZE=1024 \
    --with-pcre=objs/lib/pcre2-10.45 \
    --with-zlib=objs/lib/zlib-1.3.1 \
    --with-openssl=objs/lib/openssl-3.4.2 \
    --with-openssl-opt=no-asm \
    --with-http_ssl_module \
    --with-http_sub_module \
    --add-module=objs/lib/nginx-http-flv-module-1.2.12
    
# usage instructions
1.确保根目录有temp目录存在。  
2.双击nginx.exe启动服务。  
3.双击stop.bat停止服务。  

1.Ensure that the temp directory exists in the root directory.  
2.Double-click nginx.exe to start the service.  
3.Double-click stop.bat to stop the service.  

# concise explanation​
conf/nginx.conf 为nginx配置文件。    
RTMP监听 1935 端口。  
HTTP监听 80 端口。  
不支持exec。

conf/nginx.conf is the Nginx configuration file.  
RTMP listens on port 1935.  
HTTP listens on port 80.  
It does not support exec.  

# credits
[Nginx](https://nginx.org/)   
[nginx-rtmp-module](https://github.com/arut/nginx-rtmp-module)  
[nginx-http-flv-module](https://github.com/winshining/nginx-http-flv-module/)
