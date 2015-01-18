来自<http://www.cnblogs.com/ilexcai/archive/2011/08/20/2147173.html>
##函数和方法的差异
1.getYear()方法
```js
var year = new Date().getYear();
console.log(year);
```
IE:2010 FF:110 在 Firefox 里面 getYear 返回的是 "当前年份-1900" 的值
*兼容方法*

加上对年份的判断：
```js
var year= new Date().getYear();
year = (year<1900?(1900+year):year);
console.log(year);
```
也可以通过 getFullYear getUTCFullYear 去调用:
```js
var year = new Date().getFullYear();
console.log(year);
```
获取年份的时候用 getFullYear()方法。
