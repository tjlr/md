```js
function _(el){return document.getElementById(el);}
function _q(el){return document.querySelector(el);}
function _a(el){return document.querySelectorAll(el);}
function _cr(el){return document.createElement(''+el+'');}
function _rm(el){el.parentNode.removeChild(el);}
function _ap(el,dest){dest.appendChild(el);}
// function _pp(el,dest){dest.insertBefore(el,dest.firstChild);}
function _i(el,html){el.innerHTML=html;}
function _e(el){el.innerHTML='';}
function _sa(el,at,v){el.setAttribute(at,v);}
// _u update async
function _u(u,c) {var x=new XMLHttpRequest();x.open("GET",u,true);x.onreadystatechange=function(){if(x.readyState==4){c.call();}};x.send(null);}
function _j(u,c) {var x=new XMLHttpRequest();x.open("GET",u,true);x.onreadystatechange=function(){if(x.readyState==4){c.call(x.responseText);}};x.overrideMimeType("application/json");x.send(null);}
```
