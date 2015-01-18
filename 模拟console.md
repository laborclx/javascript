对不支持console做模拟
```js
  <p id="result"></p> //html
  var eleResult = document.getElementById("result");
  if (!window.console) {
    window.console = {};
  }
  console.log = function(result) {
    var text = document.createTextNode(result), br = document.createElement("br");
    eleResult.appendChild(text);
    eleResult.appendChild(br);
  };
```
