---
title: js方法-数组
author: cxy
date: 2021-07-25 12:32:00 +0800
categories: [JavaScript, methods]
tags: [Array]
---

## slice()
可从已有的数组中返回选定的元素  
arrarObject.slice(start,end)  
start 必需，规定从何处开始取。负数表示从数组尾部算起，-1指最后一个元素，-2指倒数第二个元素。  
end 可选，规定从何处结束，是数组片段结束处的下标，未指定表示从start到结尾，负数同上。  
arr.slice(0)得到一个和arr相同的新数组

## splice() 
向/从数组中添加/删除项目，然后返回被删除的项目 （该方法会改变数组）
arrayObject.splice(index,howmany,item1,.....,itemX)  
index 必需，规定添加/删除项目的位置，负数表示从数组结尾开始  
howmany 必需，需要删除的项目数量，0则不删除  
item1,.....,itemX 可选，像数组添加的新项目  
 										
arr.splice()返回被删除的元素  
arr 返回删除后剩余的元素  

## concat()
用于连接两个或多个数组，不改变现有数组，返回被连接数组的一个副本  
arrayObject.concat(arrayX,arrayX,......,arrayX)  
arrayX	必需。该参数可以是具体的值，也可以是数组对象。可以是任意多个。

## push()  
方法可向数组的末尾添加一个或多个元素，并返回新的长度。

## unshift() 
可向数组的开头添加一个或更多元素，并返回新的长度。

## shift() 
用于把数组的第一个元素从其中删除，并返回第一个元素的值。

## reduce()
接收一个函数作为累加器，数组中的每个值（从左至右）开始缩减，最终计算为一个值。

### 改变原数组的方法 

改变原数组的：
1、 shift：将第一个元素删除并且返回删除元素，空即为undefined
```js
let a = arr.shift()
console.log(a)         // a
console.log(arr)       // ['b', 'c', 'd']
```

2、unshift：向数组开头添加元素，并返回新的长度
```js
let a = arr.unshift(0)
console.log(a)        // 5 返回数组长度
console.log(arr)      // [0, 'a', 'b', 'c', 'd']
```

3、pop：删除最后一个并返回删除的元素
```js
let a = arr.pop()
console.log(a)        // d
console.log(arr)      // ['a', 'b', 'c']
```

4、push：向数组末尾添加元素，并返回新的长度
```js
let a = arr.push('f')
console.log(a)        // 5 返回数组长度
console.log(arr)      // ['a', 'b', 'c', 'd', 'f']
```

5、reverse：颠倒数组顺序
```js
let a = arr.reverse()
console.log(a)        // ["d", "c", "b", "a"]
console.log(arr)      // ["d", "c", "b", "a"]
```

6、sort：对数组排序
```js
let arr = ['c', 'a', 'd', 'b']
let a = arr.sort()
console.log(a)        // ['a', 'b', 'c', 'd']
console.log(arr)      // ['a', 'b', 'c', 'd']
```

7、splice:splice(start,length,item)删，增，替换数组元素，返回被删除数组，无删除则不返回
```js
let a = arr.splice(1, 2, 'f')
console.log(a)        // 返回被删除的元素数组['b', 'c'] 
console.log(arr)      // 在添加的地方添加元素后的数组["a", "f", "d"]
```

8、copyWithin:方法浅复制数组的一部分到同一数组中的另一个位置，并返回它，不会改变原数组的长度。
```js
let a = arr.copyWithin(1, 2,3)
console.log(a)  //返回被复制的元素数组 ['a', 'c', 'c', 'd']
console.log(arr)  //原元素数组已经改变 ['a', 'c', 'c', 'd']
```

9、fill:用一个元素填充原来的数组
```js
let a = arr.fill('e', 2, 4);
console.log(a) // 返回它会改变调用它的 `this` 对象本身, 然后返回它['a', 'b', 'e', 'e'] 
console.log(arr) // ['a', 'b', 'e', 'e']
```

10、map: 只有当arr为基本数据类型时，map方法才不会改变原始数组，arr为引用类型时，还是会改变原数组的
```js
const citys = [{ name: 'shenzhen' }, { name: 'hanghzhou' }];
const newCitys = citys.map((item) => {
    item.country = 'china';
    return item;
});
 console.log('citys', citys); //[{ name: 'shenzhen', country: 'china' },{ name: 'hanghzhou', country: 'china' }]
 console.log('newCitys', newCitys); //[{ name: 'shenzhen', country: 'china' },{ name: 'hanghzhou', country: 'china' }]
 ```


### 不改变原数组的方法
1、concat：targetArr.concat(otherArr[,anyOtherArr])连接多个数组，返回新的数组
```js
let a = arr.concat(['e', 'f'])
console.log(a)        // 新数组 ["a", "b", "c", "d", "e", "f"]
console.log(arr)      // ["a", "b", "c", "d"] 不变
```

2、join：将数组中所有元素以参数作为分隔符放入一个字符
```js
let a = arr.join('-')
console.log(a)        // 字符串 a-b-c-d
console.log(arr)      // ["a", "b", "c", "d"] 不变
```

3、slice：slice(start,end)，返回选定元素
```js
let a = arr.slice(1)
console.log(a)        // ["b", "c", "d"]
console.log(arr)      // ["a", "b", "c", "d"] 不变
```

4、filter,forEach,some,every,reduce等不改变原数组 map一个基本类型数组时



