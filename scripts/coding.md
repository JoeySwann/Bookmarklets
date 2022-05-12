# Coding Bookmarklets
### Developer Console
    javascript:(function()%7B(function() %7Bvar x %3D document.createElement("script")%3Bx.src %3D "https%3A%2F%2Fcdn.jsdelivr.net%2Fgh%2FSnowLord7%2Fdevconsole%40master%2Fmain.js"%3Bx.onload %3D alert("Loaded Developer Console!")%3Bdocument.head.appendChild(x)%3B%7D)()%7D)()

### Excecute HTML
    javascript:var txt='';function getSelText(wndw){var sel='';if(document.all){sel=wndw.document.selection.createRange().text;}else{sel=wndw.window.getSelection();}return sel;}void(frms=window.frames);if(frms.length==0){txt=getSelText(window);}else{for(iQA=0;iQA&lt;frms.length;iQA++){void(txt=getSelText(frms[iQA]));if(txt.length&gt;0){break;}}}while(txt.length==0){txt=promt('Input:');}win=window.open('','','');void(win.document.write(txt));void(win.document.close())

### Inject jQuery
    javascript:void(function(){document.body.appendChild(document.createElement('script')).src='http://code.jquery.com/jquery-1.7.2.min.js' })();

### Inject Script
_Insert the script into the 'http://SCRIPT-URL/SCRIPT.JS'_<br>

    javascript:(function(){document.body.appendChild(document.createElement('script')).src='http://SCRIPT-URL/SCRIPT.JS' })();

### Remove Cookies
    javascript: (function() {C = document.cookie.split("; ");for (d = "." + location.host; d; d = ("" + d).substr(1).match(/\..*$/))for (sl = 0; sl < 2; ++sl)for (p = "/" + location.pathname; p; p = p.substring(0, p.lastIndexOf('/')))for (i in C)if (c = C[i]) {document.cookie = c + "; domain=" + d.slice(sl) + "; path=" + p.slice(1) + "/" + "; expires=" + new Date((new Date).getTime() - 1e11).toGMTString()}})()

### View Cookies
Removed for issues

### View Source
    javascript: function getSelSource() {x = document.createElement("div");x.appendChild(window.getSelection().getRangeAt(0).cloneContents());return x.innerHTML;}function makeHR() {return nd.createElement("hr");}function makeParagraph(text) {p = nd.createElement("p");p.appendChild(nd.createTextNode(text));return p;}function makePre(text) {p = nd.createElement("pre");p.appendChild(nd.createTextNode(text));return p;}nd = window.open().document;ndb = nd.body;if (!window.getSelection || !window.getSelection().rangeCount || window.getSelection().getRangeAt(0).collapsed) {nd.title = "Generated Source of: " + location.href;ndb.appendChild(makeParagraph("No selection, showing generated source of entire document."));ndb.appendChild(makeHR());ndb.appendChild(makePre("<html>\n" + document.documentElement.innerHTML + "\n</html>"));} else {nd.title = "Partial Source of: " + location.href;ndb.appendChild(makePre(getSelSource()));};void 0
