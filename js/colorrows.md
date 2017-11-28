```js
  var myTR = document.getElementsByTagName('tr'); /* To use with lists, just change 'tr' to 'li' */
  for (var i=0;i<myTR.length;i++) {
    if (i%2) {
      myTR[i].className = 'rowTint';
    }
  }
```
