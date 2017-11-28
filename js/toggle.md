```js
	el = document.getElementById(elID);
	if (typeof window.getComputedStyle != "undefined") { styleObj = window.getComputedStyle(el, null); } else if (el.currentStyle != "undefined") { styleObj = el.currentStyle; }
	if(styleObj.display == "none" || styleObj.display == '') { el.style.display = "block"; } else { el.style.display = "none"; } 
```
