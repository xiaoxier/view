- 1.promise 手写
```
function Promise(callback){
	var self = this;
	self.status = 'PENDING';
	self.data = undefined;//promise的值
	self.onResolvedCallback = [];//resolve回调函数集
	self.onRejectedCallback = [];//reject回调函数集
	callback(resove,reject);//执行executor并传入相应的参数

	function resolve(value){
		if (self.status=='PENDING') {
			self.status='resolved';
			self.data = value;
                   // 依次执行成功之后的函数栈
			for(var i = 0;i<self.onResolvedCallback.length;i++){
				self.onResolvedCallback[i](value)
			}
		}
	}
	function reject(error){
		if (self.status=='PENDING') {
			self.status = 'rejected';
			self.data = error;
                   // 依次执行失败之后的函数栈
			for(var i = 0;i<self.onRejectedCallback.length,i++){
				self.onRejectedCallback[i](error)
			}
		}
	}
```
- 2.promise.all 手写
```
const p = Promise.all([p1, p2, p3]);

Promise.all = arr => {
    let aResult = [];    //用于存放每次执行后返回结果
    return new _Promise(function (resolve, reject) {
      let i = 0;
      next();    //开始逐次执行数组中的函数
      function next() {
        arr[i].then(function (res) {
          aResult.push(res);    //执行后返回的结果放入数组中
          i++;
          if (i == arr.length) {    //如果函数数组中的函数都执行完，便把结果数组传给then
            resolve(aResult);
          } else {
            next();
          }
        })
      }
    })
  };
  ```
  - 3.Generator 手写
  ```
	function  mackIter(parms){
	 	let i =0;
	 	return {
	 		next(){
	 			let done = (i>=parms.length);
	 			let value = !done?parms[i++]:undefined;
	 			return {
	 				value:value,
	 				done:done
	 			}
	 		}
	 	}
	 }

	 let Iterator = mackIter(['1','2']);

	//Generator 生成迭代器
	function*  gener(){
		yield "1";
		yield "2";
	}

	let Iterator = gener();

	//改造 Generator 
	let mackgener = function* (parms){
		for (var i = 0; i < parms.length; i++) {
			yield parms[i];
		}
	}
	let Iterator = mackgener(['1','2']);


	 console.log(Iterator.next());//{value:"1",done:false}
	 console.log(Iterator.next());//{value:"2",done:false}
	 console.log(Iterator.next());//{value:undefined,done:true}
  ```
- 4.js进出任务队列示例及执行过程解释

```
const async1 = async () => {
  console.log('async1');
  setTimeout(() => {
    console.log('timer1')
  }, 2000)
  await new Promise(resolve => {
    console.log('promise1')
  })
  console.log('async1 end')
  return 'async1 success'
} 
console.log('script start');
async1().then(res => console.log(res));
console.log('script end');
Promise.resolve(1)
  .then(2)
  .then(Promise.resolve(3))
  .catch(4)
  .then(res => console.log(res))
setTimeout(() => {
  console.log('timer2')
}, 1000)
'script start'
'async1'
'promise1'
'script end'
1
'timer2'
'timer1'
//async函数中await的new Promise要是没有返回值的话则不执行后面的内容
//.then函数中的参数期待的是函数，如果不是函数的话会发生穿透
//注意定时器的延迟时间
```
- 5.内存指向
 栈内存：存储基本数据类型及对象变量得指针
 堆内存：存储引用类型

- 6.const原理
 const声明基本数据类型不允许改变，引用类型不能改变引用地址/指针 
 ```
 示例：
 const name = 'Friday'
    name = 'Sunday'  //直接报错

    const people = {
        name: 'Jack',
        age: 21
    }
    people.age = 22
    console.log(people) //{ name: 'Jack', age: 22 }
 ```
 - 7.websocket 和http里面的 keep-alive区别
  http里得长连接本质还是属于客户端发送请求，服务端发送响应，是单向通信；
  websocket长连接是双向通信协议，建立连接后，WebSocket服务器端和客户端都能主动向对方发送或接收数据