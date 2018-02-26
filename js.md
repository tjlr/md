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
```

### between
```js
String.prototype.between = function(prefix, suffix) {
  s = this;
  var i = s.indexOf(prefix);
  if (i >= 0) {
    s = s.substring(i + prefix.length);
  }
  else {
    return '';
  }
  if (suffix) {
    i = s.indexOf(suffix);
    if (i >= 0) {
      s = s.substring(0, i);
    }
    else {
      return '';
    }
  }
  return s;
}

var dupa = '#80349__jaks-tekst'.between('#','__');
alert(dupa);
```

### color rows
```js
  var myTR = document.getElementsByTagName('tr'); /* To use with lists, just change 'tr' to 'li' */
  for (var i=0;i<myTR.length;i++) {
    if (i%2) {
      myTR[i].className = 'rowTint';
    }
  }
```

### escapeHtml
```js
function escapeHtml(s) {
  s = s.replace(/&/g, '&amp;');
  s = s.replace(/</g, '&lt;');
  s = s.replace(/>/g, '&gt;');
  s = s.replace(/"/g, '&quot;');
  s = s.replace(/'/g, '&#39;');
  return s;
}
```

### toggle element by css selector
```js
function escapeHtml(css) {
  el = document.querySelector(css);
  if (typeof window.getComputedStyle != "undefined") { styleObj = window.getComputedStyle(el, null); } else if (el.currentStyle != "undefined") { styleObj = el.currentStyle; }
  if(styleObj.display == "none" || styleObj.display == '') { el.style.display = "block"; } else { el.style.display = "none"; }
}
```
