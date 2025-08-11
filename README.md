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
