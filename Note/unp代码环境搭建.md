#### unp代码环境搭建
@(unp)
> 
准备把网络搞起，so准备啃啃unp，首先准备下代码运行环境，环境CentOS 6.5 x64(虚拟机)/Mac OS 10.10
>- 按照README的说明，在代码目录中执行
`./configure` 
`cd lib`
`make`
`cd ../libfree`
`make`
报错
        inet_ntop.c: In function 'inet_ntop':
        inet_ntop.c:61: error: argument 'size'  doesn't match prototype
        /usr/include/arpa/inet.h:65: error:  prototype declaration
解决方法:
        inet_ntop.c第60行 size_t size 改成 socklen_t size 
>- Mac上继续下一步编译不报错，可见Mac比CentOS给力啊-*-
`cd ../libroute`
`make`

        
