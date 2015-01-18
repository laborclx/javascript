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
*先执行“a-1”，再执行“a=a+1”*
```js
  console.log(a++ -1);
```
5.实现ECMAScript 5中的Object.create()函数
*原型链形式的继承，构造函数重新指向新创建的对象*
```js
  function clone(proto){
    function _clone(){};
    _clone.prototype = proto;
    _clone.prototype.constructor = _clone;
    return new _clone();
  }
```
6.脚本永不出错
```js
  window.onerror = function(){
    return true;
  }
```
7.javascript处理字符与ASCII码之间的转换
*charCodeAt()返回指定位置字符的Unicode编码，fromCharCode()接受一个指定的Unicode值，返回一个字符串*
```js
  console.log("a".charCodeAt(0)); //97
  console.log(String.fromCharCode(75)); //K
```

>惰性载入是第一次执行代码后，用函数代码内部的方法覆盖原有代码。

8.实现对Windows、Mac、linux、UNIX操作系统的判断
*navigator.userAgent表示用户代理*
```js
  var osType = "",
      windows = (navigator.userAgent.indexOf("Windows", 0) != -1) ? 1 : 0,
      mac = (navigator.userAgent.toLowerCase().indexOf("mac", 0) != -1) ? 1 : 0,
      linux = (navigator.userAgent.indexOf("Linux", 0) != -1) ? 1 : 0,
      unix = (navigator.userAgent.indexOf("X11", 0) != -1) ? 1 : 0;
  if(windows){
    osType = "Windows";
  }else if(mac){
    osType = "Mac";
  }else if(linux){
    osType = "Liunx";
  }else if(unix){
    soType = "Unix";
  }
```
9.用原生javascript判断是否是移动设备浏览器
```js
  var mobileReg = /iphone|ipod|android.*mobile|windows.*phone|blackberry.*mobile/i;
```
