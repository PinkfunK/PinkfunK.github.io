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

