# Bookmark focus highlight

_Enable and force highlight styles for focus state._

Create a bookmark and paste this in the URL/Location field:

```js
javascript:(function() {var styleTag = document.createElement('style');styleTag.innerHTML = decodeURIComponent("*:focus {border: 3px solid rebeccapurple !important;}");document.querySelector('head').appendChild(styleTag);})();
```

Or if you want the version where pressing '0' toggles the color use this one:

```js
javascript:(function(){var e=["lime","rebeccapurple","orange","blue"],t="*:focus {border: 5px solid COLOR !important;}";this.currentColorIndex=0,this.getNextColor=function(){return this.currentColorIndex=(this.currentColorIndex+1)%e.length,e[this.currentColorIndex]},this.generateStyleTagContents=function(e){var n=t.replace("COLOR",e);return decodeURIComponent(n)},this.createAndAppendStyleTag=function(){var e=document.createElement("style");e.setAttribute("id","bfh");var t=this.getNextColor();e.innerHTML=this.generateStyleTagContents(t),document.querySelector("head").appendChild(e)},this.toggleColorOnZeroPressed=function(e){if(e&&48===e.keyCode){var t=document.querySelector("#bfh"),n=this.getNextColor();t.innerHTML=this.generateStyleTagContents(n)}},this.bindKeyboardShortcuts=function(){document.addEventListener("keyup",this.toggleColorOnZeroPressed.bind(this))},this.createAndAppendStyleTag(),this.bindKeyboardShortcuts()})();
```

Use your bookmark while navigating the site to add focus styles to it :)