 js基础:
 ___
- 1.数据类型有什么? 对象作为函数参数按值传递。 基本/引用 
- 2.对象深拷贝的方法?
- 3.this的用法?  new一个构造函数  构造函数中return一个对象，生成的实例this指向谁？  不return指向谁
- 3.call/apply/bind  改变this指向 obj.myFun.apply(db,['成都','上海']);  /obj.myFun.call(db,'成都','上海');　/  obj.myFun.bind(db,'成都','上海')();
- 3.new 操作符做了什么  1.创建新对象 2.函数内部this代表新对象 3.执行函数体 4.自动返回新对象
- 3.闭包的概念 场景？
- 3.怎么理解作用域链？
- 4.数组常用的方法有哪些? 哪些会改变原数组？
- 4.判断是数据类型方法?  怎么判断一个对象是数组  4 Object.prototype.toString.call(a)
- 5.函数防抖与函数节流?   防抖是最后一次触发后空闲一段时间执行（没空闲完永远不执行）节流是间隔一段时间就被触发一次，节流会稀释函数执行频率。
- 6.遍历的方法有哪些?  keys()  values()  entries() forEach for...in  for...of for every some map  filter reduce reduceRight find findIndex  
- 7.js数字计算精度丢失怎么解决? 0.1+0.2  ?
- 10.事件流是什么? 事件委托怎么实现？ 触发事件元素(e.target)和绑定事件元素(e.currentTarget)怎么获取？
- 11.什么是模块化？
- 12.例举3种强制类型转换和2种隐式类型转换？
- 13.实现异步的方式? 回调函数、promise、Generator、async/await、事件监听、发布/订阅
- 13.es6语法用过哪些?

**es6:**
*   1)let const
*   2)解构赋值 let {a,b} = {a:1,b:2}
*   3)箭头函数
*   4)字符串模板 
*   5)扩展运算符 ...
*   6)数组方法 map/filter
*   7)class关键字 类
*   8)promise
*   9)函数参数默认值 fn(a=1){}
*   10)对象属性简写 
``
const name='Ming', age='18', city='Shanghai';
const student ={
    name:name,
    age:age,
    city:city
};
console.log(student);
``
*   11)模块化 import  export default
**es7:**


15.介绍下 Set、Map、WeakSet 和 WeakMap 的区别？  防止内存泄漏 弱引用
16.map和forEach区别
17.实现原生拖拽


 vue:
___
1.VUE响应式原理？双向数据绑定原理？
2.组件之间如何通信？ 父子/隔代/任意
3.vuex的原理?
4.ui框架??
5.React / Vue 项目时为什么要在列表组件中写 key，其作用是什么？
6.什么是动态组件？他的作用是什么？include exclude max
7.为什么组件中的data属性的值必须是一个函数？
8.如何阻止Vue中的绑定事件不发生冒泡 。  .stop
9.$set原理
10.了解Vue3.0嘛
11.$ref与props区别  怎么调用子组件得属性和方法
12.vue2.0与vue3.0得区别
13.父组件怎么获取子组件的生命周期

 浏览器:
___
1.什么是跨域？
2.EventLoop?  同步任务在主线程上形成一个执行栈，主线程外，事件触发线程管理一个任务队列，在任务队列中依次放置异步任务。
2.为什么说js是单线程的? 一次只做一件事，当前任务完成才执行队列中下一个任务。宏任务【同步任务-微任务-宏任务【同步任务-微任务-宏任务[...]】】
3.浏览器地址栏输入url后发生了什么?  重排重绘
4.什么时候引起回流?
5.做过优化吗?
6.node常用模块？


 http:
 ___
1.说一下200和304的理解和区别

工程化:
1.git常用命令? 删除远程分支   git  push origin --delete branch
2.git版本管理规范?  功能  开发   预发布 生产  hotfix  


 css:
___
设置小于12px字体  {font-size:12px; -webkit-transform:scale(0.8);}
flex布局属性  flex-direction/ flex-wrap/ justify-content /align-items/align-content:/flex-flow
css选择器优先级
h5怎么做适配? em rem px 区
1px问题怎么解决?原因是什么?
浮动的特性?清浮动的方法?
300ms延迟 
BFC
垂直水平居中
css三角形  
div {
      width: 0;
      height: 0;
      border: 20px solid transparent;
      border-width: 40px 20px 0 0;
      border-right-color: #f99;
    }





 软实力题:
___
1.工作中  产品需求不合理?  怎么办
1.项目过程中，有遇到什么问题吗？怎么解决的
1.你最大的优点是什么？那你最大的缺点呢？
1.身边的朋友通常对你的评价是什么
1.喜欢什么样的工作氛围
1.怎么理解前端技术的大趋势？自己在做哪方面的知识储备？
2.对以后自己的前端职业路线，怎么规划
2.到岗时间?期望薪资?



