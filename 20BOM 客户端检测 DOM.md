## BOM

提供了与网页无关的浏览器功能对象

1. ### window对象

   - Global作用域
     - 因为window对象被复用为ECMAScript的Global对象，所以通过var声明的所有全局变量和函数都会变成window对象的属性和方法
   - 窗口关系
   - 窗口位置与像素比
   - 窗口大小
     - 所有现代浏览器都支持4个属性：innerWidth、innerHeight、outerWidth和outerHeight
   - 视口位置
   - 导航与打开新窗口
     - window.open()方法可以用于导航到指定URL，也可以用于打开新浏览器窗口。这个方法接收4个参数：要加载的URL、目标窗口、特性字符串和表示新窗口在浏览器历史记录中是否替代当前加载页面的布尔值。通常，调用这个方法时只传前3个参数，最后一个参数只有在不打开新窗口时才会使用
   - 定时器
   - 系统对话框
     - alert()警告框、confirm()确认框和prompt()提示框

2. ### location对象

   - location是最有用的BOM对象之一，提供了当前窗口中加载文档的信息，以及通常的导航功能。这个对象独特的地方在于，它既是window的属性，也是document的属性
   - 查询字符串
   - 操作地址

3. ### navigator对象

4. ### screen对象

5. ### history对象



## 客户端检测

能力检测

- if(object.propetryInQuestion)

1. 安全能力检测
2. 基于能力检测进行浏览器分析
   - 检测特性
   - 检测浏览器

用户代理检测

- 用户代理检测通过浏览器的用户代理字符串确定使用的是什么浏览器。用户代理字符串包含在每个HTTP请求的头部，在JavaScript中可以通过navigator.userAgent访问

浏览器分析

- window.navigator.userAgent

软件与硬件检测

## DOM

文档对象模型（DOM，Document  Object  Model）

1. ### 节点层级

   - HTML和XML文档 DOM树

     1. Node类型

        - 每个节点都有nodeType属性，表示该节点的类型。节点类型由定义在Node类型上的12个数值常量表示
          1. nodeName与nodeValue
          2. 节点关系 dom树结构
          3. 操纵节点

   2. Document类型

    ​    Document类型是JavaScript中表示文档节点的类型。在浏览器中，文档对象document是HTMLDocument的实例（HTMLDocument继承Document），表示整个HTML页面。document是window对象的属性，因此是一个全局对象
       1. Element类型
       2. Text类型
       3. Comment类型
       4. CDATASection类型
       5. DocumentType类型
       6. DocumentFragment类型

       4. Attr类型

 2. ### DOM编程

    1. 动态脚本 js
    2. 动态样式css
    3. 操作表格
    4. NodeList

3. ### MutationObserver接口

4. 性能、内存与垃圾回收

##     DOM拓展

1. Selectors API 
   1. querySelector() 接受css选择符参数 返回第一个匹配的节点
   2. querySelectorAll()返回所有匹配的节点 为Nodelist实例
   3. matches()接收一个CSS选择符参数，如果元素匹配则该选择符返回true，否则返回false
2. 元素遍历
3. HTML5
   1. css拓展
   2. 焦点管理
   3. HTMLDocument 拓展
   4. 字符集属性
   5. 自定义数据属性
   6. 插入标记

