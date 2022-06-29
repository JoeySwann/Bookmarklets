# Coding Bookmarklets
### Inject jQuery
    javascript:void(function(){document.body.appendChild(document.createElement('script')).src='http://code.jquery.com/jquery-1.7.2.min.js' })();

### Inject Script
_Insert the script into the 'http://SCRIPT-URL/SCRIPT.JS'_<br>

    javascript:(function(){document.body.appendChild(document.createElement('script')).src='http://SCRIPT-URL/SCRIPT.JS' })();

### Remove Cookies
    javascript: (function() {C = document.cookie.split("; ");for (d = "." + location.host; d; d = ("" + d).substr(1).match(/\..*$/))for (sl = 0; sl < 2; ++sl)for (p = "/" + location.pathname; p; p = p.substring(0, p.lastIndexOf('/')))for (i in C)if (c = C[i]) {document.cookie = c + "; domain=" + d.slice(sl) + "; path=" + p.slice(1) + "/" + "; expires=" + new Date((new Date).getTime() - 1e11).toGMTString()}})()
