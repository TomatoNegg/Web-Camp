# servlet
#### 1. 为什么Http请求为GET时，自动调用doget（）？
- 因为在HTTPServlet中有一个service方法，这是处理HTTP相关的服务流程。HTTP有请求来了，那么容器调用service方法，因为service方法中定义的，基本是判断HTTP请求的方式，以及处理这些请求的方法，如doget（），doPost（），doHead（）等等。请求来了，判断是哪种请求，自动调用处理这种请求的方法。



#### 2. 为什么要在继承Httpservice之后重新定义doget（）
- 在helloservlet中，继承了Httpservlet后，重新定义了doget（）方法，就好像说，你不想用父类那套陈旧的方法，想标新立异，那么就自己写一套出来，于是你就重写了父类的处理doget（）的方法，想用自己方式处理GET（），Post（）请求等等。就是子类的重写，覆盖了父类的方法，当有请求来的时候，首先访问的是子类的方法
- 

#### 3. 用eclise Tomcat有个错误就是@webServlet（“/HelloWorld”），然后运行tomcat时会弹出Server Tomcat 版本 Server at localhost failed to start
- 这是因为在eclipse写serlet时，@webServlet这个注释已经帮我们写好了。每次我们新建一个servlet后在web.xml文件中配置映射关系，这样才能在浏览器敲入一个地址后，地址发来的请求能让服务器接收到请求并将请求交给指定的servlet去处理。真相其实说白了就是web。xml配置与自动生成的注释冲突了。所以解决办法可以删除web，xml中的映射，也可以将自动生成的注解注释掉。就是让他们没有冲突就可以了

#### 4. Servlet中上传文件的文件名记录因浏览器不同而不同
##### 描述：要上传文件或者图片时，在Content-Disposition中的filename因浏览器不同而不一样的，有的浏览器会记录整个文件和图片的路径名，有的却只记录文件或图片的名字。
- 解决：遇到这种情况，应先用getReader()获取标头的信息，看下你浏览器支持哪种类型，当然我的错误就是我用的是Microsoft edge浏览器，其中filename中是完整记录路径名的，但是书本中却不是这样的。因此在上传前要查看下标头信息，再在servlet中截取filename，用java的indexOf和lastIndexOf获取字符串吧。