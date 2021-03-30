## JSON

JSON不属于JavaScript，它们只是拥有相同的语法而已

1. ### 语法

   1. 简单值

      - 字符串、数值、布尔值和null可以在JSON中出现，就像在JavaScript中一样。特殊值undefined不可以

   2. 对象

      - JSON中的对象必须使用双引号把属性名包围起来，与JS不同，JSON中没有变量，也没有分号

   3. 数组

      - 在JSON中数组是以JS字面量形式表示
   
2. ### 解析与序列化

   1. JSON对象

      - stringify()和parse()方法
      - JSON.stringify()会将JS对象序列化为一个JSON字符串 默认不含空格或缩进并且在序列化JavaScript对象时，所有函数和原型成员都会有意地在结果中省略。此外，值为undefined的任何属性也会被跳过
      - JSON.Parse()会将json转换成JS值

   2. 序列化选项

      - JSON.stringify()方法除了要序列化的对象，还可以接收两个参数。这两个参数可以用于指定其他序列化JavaScript对象的方式。第一个参数是过滤器，可以是数组或函数；第二个参数是用于缩进结果JSON字符串的选项

      - toJSON()自定义JSON序列化

        ```javascript
        let person={
            name:'lukas',
            tel:15324558125,
            hobbys:['soccer','majiang','movie'],
            age:45,
            toJson:function sayhi(){
                return this.name;
            }
        }
        let context = JSON.stringify(person,null,1);
        console.log(person.toJson())
        // console.log(context)
        //lukas
        ```

   3. 解析选项

      - JSON.parse()方法也可以接收一个额外的参数，这个函数会针对每个键/值对都调用一次。为区别于传给JSON.stringify()的起过滤作用的替代函数（replacer），这个函数被称为还原函数（reviver）。实际上它们的格式完全一样，即还原函数也接收两个参数，属性名（key）和属性值（value），另外也需要返回值

   

   

   

   

   

   

      

      

      

      

      

      

      

      

      

      

      

      

      

      

      
