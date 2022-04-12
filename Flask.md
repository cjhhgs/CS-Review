低层由socket实现网络间进程交流。flask开通监听端口，并根据路由，选择执行操作。

flask框架如果要返回给用户复杂的内容时,需要借助jinja2模板来实现对模板的处理，即：**将模板和数据进行渲染，将渲染后的字符串返回给用户浏览器**







#### flask_login

认证后的用户，进行一次操作（一个GET操作、一次[POST](https://so.csdn.net/so/search?q=POST&spm=1001.2101.3001.7020)操作或者其他），会话信息会以Cookie：value的方式传送给flask应用，flask应用开启一个进程或者线程进行处理。

会根据[Cookie](https://so.csdn.net/so/search?q=Cookie&spm=1001.2101.3001.7020)的值解析出一些会话信息，根据这些会话信息内容判断用户的身份、权限等，进行相应的操作。

上面的这些会话信息会存在请求上下文里(request contents)【变量[session](https://so.csdn.net/so/search?q=session&spm=1001.2101.3001.7020)】。请求的时候，使用内存存储这些会话信息。请求结束，销毁变量，释放内存。