# windows下编译安装nginx-vod-module
> 在windows下编译nginx-vod-module,做点播使用
## 操作系统(system)
- windows7
## 工具(tools)
- gitgui(gitscm)
	https://git-scm.com/download
- vs2010 express(free and small)
	https://microsoft-visual-cpp-express.soft32.com/free-download/?dm=0

## nginx 
- pcre
- perl ( activeperl for me )
- openssl
- zlib
>to generante nginx.exe, just look there https://github.com/tjliupeng/nginx-build-windows or 

## nginx-vod-module
I got some problems
- inttypes.h could not found
	>get it from http://code.google.com/p/msinttypes/, just put it to vs10/include 
- ngx_config.h
	> Add '#include "ngx_config.h' to all C files of this module - for the files under the root folder of the module it's fine, but the files under the vod folder are currently abstracted from nginx, so that would be far from ideal.
- warning treat as error
	open Makefile
		CFLAGS =  -O2  -W4  -nologo -MT -Zi -DFD_SETSIZE=1024 -DNO_SYS_TYPES_H
	just delete -WX flags

## summary
- everything above was packaged in my repository,include the final nginx.exe

## generate Makefile
./configure \
--with-cc=cl \
--builddir=objs \
--prefix= \
--conf-path=conf/nginx.conf \
--pid-path=logs/nginx.pid \
--http-log-path=logs/access.log \
--error-log-path=logs/error.log \
--sbin-path=nginx.exe \
--http-client-body-temp-path=temp/client_body_temp \
--http-proxy-temp-path=temp/proxy_temp \
--http-fastcgi-temp-path=temp/fastcgi_temp \
--with-cc-opt=-DFD_SETSIZE=1024 \
--with-pcre=objs/lib/pcre-8.40 \
--with-zlib=objs/lib/zlib \
--with-openssl=objs/lib/openssl \
--with-openssl-opt=no-asm \
--with-select_module  \
--with-http_ssl_module \
--add-module=objs/lib/nginx-rtmp-module