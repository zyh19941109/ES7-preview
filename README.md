## ES7-preview

### 函数参数容忍度

```javascript
	ES7
	
	function show(a,b,c,){//最后一个逗号在ES7中可容忍
		console.log(a,b,c)
	}
	show(1,2,3)
```

### 字符串前、后填充

```javascript
	/*
		padStart/padEnd
		字符串的前、后填充
	*/
	console.log('zyh'.padStart(4, '0')); // 0zyh
	console.log('zyh'.padEnd(5, '0')); //zyh00
```

### Object.entries()

```javascript
	Object.entries() 返回一个数组
	
	let obj = {a:'zyh',b:123}
	
	for(var key of Object.keys(obj)){
		console.log(key)
	}
	for(var value of Object.values(obj)){
		console.log(value)
	}
	for(var entry of Object.entries(obj)){
		console.log(entry)
	}
	//也可以使用ES6解构
	for(var [k,v] of Object.entries(obj)){
		console.log(k,v)
	}
```

### async await

> 1.它作为一个关键字放到函数前面，用于表示函数是一个异步函数，因为async就是异步的意思， 异步函数也就意味着该函数的执行不会阻塞后面代码的执行。

> 2.async函数返回一个 Promise 对象。async函数内部return语句返回的值，会成为then方法回调函数的参数。async函数内部抛出错误，会导致返回的 Promise 对象变为reject状态。抛出的错误对象会被catch方法回调函数接收到。

```javascript
	//	async function readData(){
	//		let data1 = await $.ajax({url: 'data/arr.txt', dataType: 'json'});
	//		let data2 = await $.ajax({url: 'data/json.txt', dataType: 'json'});
	//	
	//		console.log(data1, data2);
	//	}
		
		let readData = async () =>{
		  let data1 = await $.ajax({url: 'data/arr.txt', dataType: 'json'});
		  let data2 = await $.ajax({url: 'data/json.txt', dataType: 'json'});
		
		  console.log(data1, data2);
		}
		
		readData();
```
