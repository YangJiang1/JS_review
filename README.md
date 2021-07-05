### day1自我总结

#### JavaScript三部分

 * ECMAScript （欧洲计算机制造协会，定义语法规范）
 * BOM (browser object model 浏览器对象模型)
 * DOM (document object model 文档对象模型)

#### ES6之前六大数据类型

 * Number/String/Boolean/NULL/undefined/Object
 * 值类型
    * Number 
    * String (他的值是不可改变的，而当将一个已经存在的字符串赋予新值的时候，实际上在次过程中分配了一个新字符串,原有的字符串将被GC回收)
    * boolean
    * undefined
    * null(至于存在那里，这取决于解释器的具体实现)
 * 引用类型
    * Object(Array,Function,Date .....)

####  页面的渲染过程

* 打开页面,页面标签和css进行解析

* 在解析过程中如果遇见js,则暂停html的渲染

* js执行完后,才会去渲染html页面,执行时间过长会导致页面阻塞

* 因为js是单线程的,所以我们一般把js写在底部,这也是解决页面阻塞的办法之一.

  ```javascript
  async(异步)和defer(延迟)的区别是什么?
  	首先他们两都是为了解决页面的阻塞问题.
  	async是等页面渲染完成后,立即执行.哪个js先加载,就会去执行哪个js,不保证js的执行顺序.
  	defer是等页面渲染完成后,按顺序执行js.
  
  	JavaScipt脚本阻塞问题。当前最稳妥的办法还是把Script标签放在body的底部，没有兼容性问题。不会因此产生白屏问题，没有执行顺序问题。
  ```

#### 碎片知识点

 * alert(); 会造成页面阻塞 不建议使用

 * 选择首选项->键盘快捷方式->搜索comment  修改块注释快捷键 ctrl+shift+/

 * 开启鼠标滚轮缩放 设置->搜索Mouse Wheel Zoom->开启

 * 搜狗输入法设置 中文时使用英文标点 提高开发效率

 * Ctrl+B 开关左边的导航栏

 * mynam 能组成多少个不同的字母? 1x2x3x4x5 = 120

 * 如何解决 0.1+0.2 不等于0.3

   > 因为在js中,计算0.1和0.2,计算机只认识二进制,先会把他们转换成二进制相加再将其转换为10进制,转换为2进制的过程会有无限循环,所以导致转换为10进制后不准确.
   >
   > 解决办法是(0.1 * 10 +  0.2 * 10) / 10

 * 进制转换过了一遍

   