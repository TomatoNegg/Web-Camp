# QG工作室网络组后台邓博文第五周周记
## 生活随记
这周大英老师比较坑，有毒。明明说好的四级过了的，考勤就会有三次免死金牌，结果无端端被用掉2次，总共一学期才3次点名。（明明就没点名）然后就被坑去大英了，不过上大英也好，巩固一下自己的英文。感觉像第一次上大英一样。教室都不知走去哪。这周我哥还从澳大利亚回来了，死定了，看到我整天窝在宿舍打码，不知会有什么感觉，应该会被骂惨。嗯嗯，一定会的，没错一定会。
## 学习情况
##### 1.  servlet学习
现在进入复习阶段，上周看到其他工作室考核的人都基本已经做出了自己的项目，而自己还在深入了解servlet，感觉差距瞬间被拉大了，真是没有对比就没有伤害。不过，我还是会坚持自己的路线，现在我也基本做出了其他的考核题。在servlet学习中，分清楚了sessionConfig，以及ServletConfig，然后了解到在Attribute可以在session，Servlet中设置，其实属性就像是抛一个球，然后在另一个地方把它接住。比如在servlet中设置一个book属性，然后转到service中再getAttribute（），这样去得到这个对象。然后在不断地实践中，也了解到设计一个项目功能，最好的呢就是先设计好数据库，然后再写好Dao层，写好Dao层后，接下来就会相对轻松很多。servlet，model，servlce层都比较容易弄。有时候，许多功能都是差不多的，不知道这是不是个模板来的，都是在servlet收集参数，或者与前端交互的处理，然后如果需要给其他的servlet去处理，再getRequestDispatcher（）.forward()或者include()。然后呢可以调用service层方法，其中要将sevlet的参数用model层的对象打包封装，然后再将model传到service层，或者设置属性，在service层中得到属性。Service层在调用Dao层方法，与数据库进行互动。整个流程大概就是这样。
##### 2. HTML/CSS/JS学习
讲真，HTML，CSS，JS都几好使，好多野在前端就可以搞掂了。插入一个背景图，用CSS控制，JS进行事件的响应，不过一点就是HTML中的<div>标签还不够熟练掌握，我看了很多网站的前端，发现大量使用<div>，基本都是这个标签构成的前端。然后不断去搜查各大网站的HTML元素，在里面学习他们的用法。然后再去W3scool中查看标签。组长说的没错，前端后台配合的好的话，真的可以省下一大堆功夫，现在突然好想找人写前端。泪奔.jpg。
> 然后再这周学习时。做好一个简单的后台，然后让一些师兄来进行测试，妈个鸡，师兄随便输入点什么，然后就截取了我的管理员密码。要命，还好他没有删库跑路。个人觉得如果他把我数据库给删了，会同佢死过！！！！

##### 3. MySQL学习
这周还继续深入学习了MYSQL，之前看是看完了，但基础不扎实，讲真，基础不扎实，真系寸步难行。现在回头再看一遍，觉得之前漏掉了点重要的。然后在做学生成绩管理系统时，对怎样去设计数据库有一定的困惑。就是不清楚怎样多对多。哎，继续学吧。
## 存在问题
问题挺多的，首先在进行插入数据库时出现了乱码，然后细心，耐心，有心的我发现是自己粗心的没有设置request.setCharacterEncoding（），在响应时没有写response.setContentType()。

其次，在JS验证中，不想每次都弹出一个框，增加用户的操作成本。然后想直接提示说你账号输错了这样。但对着网上一些教程来进行书写时，发现比之前更差了。然后就特别困惑，onfocus(),onblur()这样的属性难道用不了吗，js函数中明明谢了innerHTML的，为甚么在相应的位置没有出现中文提示。这是一个令人困惑的地方。然后我再在W3scool上的模拟器上进行实操。发现还是不行。这就很奇怪了。其他属性也是可以的呀。

然后还生出了另一个疑惑，就是后台开发中，是不是都按照刚刚说的那样做呢，有没有别的路径去实现。在写学生成绩管理系统时，一个困惑就是如果学校新增了课程，新设了专业，或者学生课程有所变化，那我的这个管理系统肯定存在设计上的问题。不能做到灵活应对。这不是一个好的方法。因此我会更加努力去探求跟多的解决办法。

## 一周总结
这周收获至少比上周大得多。上周真的无fuck说。看来努力就会有结果，决定要比更多人努力才能有更大的收获。去探求更多的知识，巩固现在的知识。把servletJSP，JSTL都理解透，才能得心应手。当出现问题时，一定要善于借助网络。还有要记笔记

## 下周规划
继续开发项目，同时学习前端，被喷的够惨了。然后同时完善项目，使得代码更加健壮。程序更加安全
