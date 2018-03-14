## summaryQuestions
#### DNA重复序列（Repeated DNA Sequences）
* Q:Write a function to find all the 10-letter-long sequences (substrings) that occur more than once in a DNA molecule. **
* For example:
``` javascript
var s = "AAAAACCCCCAAAAACCCCCCAAAAAGGGTTT"
Return:
["AAAAACCCCC", "CCCCCAAAAA"].
```  
##### 题意：给出一串字符串，找出其中长度为10的出现次数大于1的子串。
* A:
``` javascript
	var answer = []
	var  ass = 'AAAAACCCCCAAAAACCCCCCAAAAAGGGTTT';
	function repeatess(a){
		var arr = []
		for(var i = 0;arr.push(a.slice(i,i+10));i++){
			if(i == ass.length-10){
				break;
			}
		}
		return arr
	}
	function returnAnswer(arr){
		var rel = [];
		for(var i = 0;i<arr.length;i++){
			if(!~rel.indexOf(arr[i])){
				rel.push(arr[i])
			}else{
				!~answer.indexOf(arr[i])&&answer.push(arr[i])
			}
		}
		return answer;
	}
	returnAnswer(repeatess(ass)) //["AAAAACCCCC", "CCCCCAAAAA"]
```
#### 什么是闭包？代码执行结果
```
function fun(arr){
	var i , len
	for(var i = 0,len = arr.length ; i<len ;i ++ ){
		(function(i){
			setTimeout(function(){
				console.log(i)
			},i*1000)
		})(i)
	}
}
fun(new Array(5))
输出结果：每一秒输出一个数
0  1  2  3  4  5
```
#### 在遍历数组或对象时会想到这两个方法：`for…in` 与`for …of `
这两个方法的区别有：  
1、in遍历的是对象的键名、数组的成员下标（为字符串类型，不能进行运算，访问的时候都要用【键名】的形式）。  
2、of不能遍历对象。只可以遍历iterable类型；而iterable类型包括（Array、Map和Set类型。对象不属于iterable类型。）
