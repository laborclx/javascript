1.区分IE和非IE浏览器
*IE11不支持*
```js
  if(!+[1,]){
    alert("IE");
  }else{
    alert("非IE");
  }
```
2.将日期直接转换为数值
```js
  +new Date();
```
3.非IE浏览器下将类数组对象“arguments”转为数组
```js
  Array.prototype.slice.call(arguments);
```
4.单链式运算
```js
  console.log(a++ -1);
```
*先执行“a-1”，再执行“a=a+1”*
5.实现ECMAScript 5中的Object.create()函数
```js
  function clone(proto){
    function _clone(){};
    _clone.prototype = proto;
    _clone.prototype.constructor = _clone;
    return new _clone();
  }
```
*原型链形式的继承，构造函数重新指向新创建的对象*
