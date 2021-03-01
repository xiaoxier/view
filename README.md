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
- 4.伪数组特性 常见伪数组
- 4.伪数组转数组  
- 5.函数防抖与函数节流?   防抖是最后一次触发后空闲一段时间执行（没空闲完永远不执行）节流是间隔一段时间就被触发一次，节流会稀释函数执行频率。
- 6.遍历的方法有哪些?  keys()  values()  entries() forEach for...in  for...of for every some map  filter reduce reduceRight find findIndex  
- 7.js数字计算精度丢失怎么解决? 0.1+0.2  ?
- 10.事件流是什么? 事件委托怎么实现？ 触发事件元素(e.target)和绑定事件元素(e.currentTarget)怎么获取？
- 11.什么是模块化？
- 12.例举3种强制类型转换和2种隐式类型转换？
- 13.实现异步的方式? 回调函数、promise、Generator、async/await、事件监听、发布/订阅
- 13.promise 自身api  原型上方法 作用 
- 13.es6语法用过哪些?
- 13.async/await作用?
- 14.库和框架区别
- 15.MVC MVVM区别
- 15.面向对象？
- 16.ajax封装？

**es6:**
>  
1)let const
>  
2)解构赋值 let {a,b} = {a:1,b:2}
>  
3)箭头函数
>  
4)字符串模板 
>  
5)扩展运算符 ...
>  
6)数组方法 map/filter
>  
7)class关键字 类
>  
8)promise
>  
9)函数参数默认值 fn(a=1){}
>  
10)对象属性简写 
```
	const name='Ming', age='18', city='Shanghai';
	const student ={
	    name:name,
	    age:age,
	    city:city
	};
	console.log(student);
```
>  
11)模块化 import  export default

**es7:**
>
1)[23,1,2].includes(1) //true

**es8:**
>
1)async/await
**es9:**
>
1)promise.finally()
**es10:**
>
1)Array.flat()  Array.flatMap()
```
	let multi = [1,2,3,[4,5,6,[7,8,9,[10,11,12]]]];
	multi.flat();               // [1,2,3,4,5,6,Array(4)]
	multi.flat().flat();        // [1,2,3,4,5,6,7,8,9,Array(3)]
	multi.flat().flat().flat(); // [1,2,3,4,5,6,7,8,9,10,11,12]
	multi.flat(Infinity);       // [1,2,3,4,5,6,7,8,9,10,11,12]

	array.flatMap(v => [v, v * 2]);
	[1, 2, 2, 4, 3, 6, 4, 8, 5, 10]
```
- 15.介绍下 Set、Map、WeakSet 和 WeakMap 的区别？  防止内存泄漏 弱引用
- 16.map和forEach区别
- 17.实现原生拖拽
 -18.组件化与模块化的区别


 vue:
___
- 1.VUE响应式原理？双向数据绑定原理？
- 1.怎么理解vue中的虚拟DOM?
- 1.怎么操作虚拟DOM?
- 1.$nextTick原理及使用场景?
- 1.如果在vue实例创建之后添加新的属性到实例上，不会触发视图更新？
- 1.vue-loader是什么?  是基于webpack的一个loader,负责解析转换.vue文件,提取script/style/templete,在分别交给对应loader处理. 
- 2.组件之间如何通信？ 父子/隔代/任意
- 3.vuex的原理?   状态管理工具,能够实现多组件共享数据.
```
	1.state     状态管理工具，存储的是数据，所以状态即数据
	2.mutations 里面放的是处理state数据的方法，都是同步操作
	3.actions   用于存放异步操作方法，也可以处理同步，由于操作state数据需要mutations里的方法所以需要在其内部提交mutations方法
	4.getters   是一种计算属性用于数据监听，监听的是state里面的数据，要用return返回监听数据
```
- 4.ui框架??
- 5.React / Vue 项目时为什么要在列表组件中写 key，其作用是什么？
- 6.什么是动态组件？他的作用是什么？原理是什么? include exclude max
- 6.路由传参  params  query 
- 6.$router(是vueRouter的实例) $route($route为当前路由跳转对象) 区别
- 6.导航钩子有几种（导航守卫）具体怎么用的
- 7.vue组件中的data为什么是函数？
- 8.如何阻止Vue中的绑定事件不发生冒泡 。  .stop
- 9.$set原理
- 9.v-if 和 v-show 的区别，适合场景
- 10.了解Vue3.0嘛
- 11.$ref与props区别  怎么调用子组件得属性和方法
- 11.vue按键修饰符 .tab .enter  .esc .space  .delete(捕获"删除"和"空格"键) .up  .down .left .right
- 11.v-model 的修饰符有哪些，分别作用是什么  .trim  .lazy  .number 
- 12.vue2.0与vue3.0得区别
- 13.子组件生命周期
```
	1.初始化阶段：父组件beforeCreate=>父组件Created=>父组件beforeMount=>子组件beforeCreate=>子组件Created=>子组件beforeMount=>子组件mounted=>父组件mounted
	2.数据更新阶段：父组件beforeUpdate=>子组件beforeUpdate=>子组件updated=>父组件updated
	3.实例销毁阶段：父组件beforeDistory=>子组件beforeDistory=>子组件distoryed=>父组件distoryed
```
- 13.vue生命周期每个阶段做了什么
- 13.父组件怎么获取子组件的生命周期
- 14.echart常用配置项
```
	图表标题 title
	图例  legend
	值域 dataRange
	提示框 tooltip
	区域缩放控制器 dataZoom
	网格 grid
	类目轴 categoryAxis
	值型坐标轴默认参数 valueAxis
	柱形图默认参数 bar
	折线图默认参数 line
	散点图默认参数 scatter
	饼图默认参数 pie
	默认标志图形类型列表 symbolList
	可计算特性配置, 孤岛, 提示颜色 calculable
```

 浏览器:
___
- 1.什么是跨域？
- 2.js运行机制  同步任务在主线程上形成一个执行栈，主线程外，事件触发线程管理一个任务队列(eventloop队列)，在任务队列中依次放置异步任务。
- 2.为什么说js是单线程的? 一次只做一件事，当前任务完成才执行队列中下一个任务。宏任务【同步任务-微任务-宏任务【同步任务-微任务-宏任务[...]】】
- 3.浏览器地址栏输入url后发生了什么?  重排重绘
- 4.什么时候引起回流?
- 5.做过优化吗?
- 6.node常用模块？
- 7.本地缓存与浏览器缓存机制
- 7.token作用:token是服务端生成的'令牌',来识别不同的身份  1.防止表单重复提交 2.判断用户是否登录
- 8.websoket



 http:
 ___
- 1.说一下200和304的理解和区别

工程化:
- 1.git常用命令? 删除远程分支   git  push origin --delete branch
- 2.git版本管理规范?  功能  开发   预发布 生产  hotfix  



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



