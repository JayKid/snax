# Bookmark focus highlight

_Enable and force highlight styles for focus state._

Create a bookmark and paste this in the URL/Location field:

```js
javascript:(function() {var styleTag = document.createElement('style');styleTag.innerHTML = decodeURIComponent("*:focus {border: 3px solid rebeccapurple !important;}");document.querySelector('head').appendChild(styleTag);})();
```

Use your bookmark while navigating the site to add focus styles to it :)