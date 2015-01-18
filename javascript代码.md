1.区分IE和非IE浏览器
```js
  if(!+[1,]){
    alert("IE");
  }else{
    alert("非IE");
  }
```
>IE11不支持
2.将日期直接转换为数值
```
  +new Date();
```
