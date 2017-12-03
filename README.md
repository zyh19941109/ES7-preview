## ES7-preview

### 函数参数容忍度

		ES7
		
		function show(a,b,c,){//最后一个逗号在ES7中可容忍
			console.log(a,b,c)
		}
		show(1,2,3)

### 字符串前、后填充

		/*
			padStart/padEnd
			字符串的前、后填充
		*/
    	console.log('zyh'.padStart(3, '0'));
    	console.log('zyh'.padEnd(4, '0'));

### Object.entries()

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

### async await

> 1.不依赖于外部的runner	=>		标准统一、性能提升

> 2.可以用箭头函数

```html
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
