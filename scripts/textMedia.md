# Text/Media Bookmarklets
### ALL CAPS
   javascript: (function() {var i, t, D = document;for (i = 0; t = D.getElementsByTagName('textarea')[i]; ++i) t.value = t.value.toLowerCase(); var newSS, styles = '*{text-transform:uppercase}input,textarea{text-transform:none}';if (D.createStyleSheet) {D.createStyleSheet("javascript:'" + styles + "'");} else {newSS = D.createElement('link');newSS.rel = 'stylesheet';newSS.href = 'data:text/css,' + escape(styles);D.getElementsByTagName("head")[0].appendChild(newSS);}})()
### Capatalize All Words
    javascript: (function() {var i, t, D = document;for (i = 0; t = D.getElementsByTagName('textarea')[i]; ++i) t.value = t.value.toLowerCase(); var newSS, styles = '*{text-transform:capitalize}input,textarea{text-transform:none}';if (D.createStyleSheet) {D.createStyleSheet("javascript:'" + styles + "'");} else {newSS = D.createElement('link');newSS.rel = 'stylesheet';newSS.href = 'data:text/css,' + escape(styles);D.getElementsByTagName("head")[0].appendChild(newSS);}})()
### Change Font
    javascript:void(document.body.style.fontFamily=prompt("Pick a font. Complex fonts won't work.",""))
### Check Text Details
    javascript: void((function(d) {    var e = d.createElement('script');    e.setAttribute('type', 'text/javascript');    e.setAttribute('charset', 'UTF-8');    e.setAttribute('src', '//www.typesample.com/assets/typesample.js?r=%27%20+%20Math.random()%20*%2099999999);%20%20%20%20d.body.appendChild(e)})(document));
### Edit Content
_Note: some text is actually an image, so don't complain this doesn't work._<br>
To EDIT content:

    javascript:document.body.contentEditable = true; void 0;
To STOP EDITING, use this script (this doesn't DELETE your edits/make them permanent):

    javascript:document.body.contentEditable = false; void 0;
### Flip Images
    javascript:(function(){['', '-ms-', '-webkit-', '-o-', '-moz-'].map(function(prefix){Array.prototype.slice.call(document.querySelectorAll('img')).map(function(el){el.style[prefix + 'transform'] = 'rotate(180deg)';});});}())
### Images FLY!
    javascript:R=0; x1=.1; y1=.05; x2=.25; y2=.24; x3=1.6; y3=.24; x4=300; y4=200; x5=300; y5=200; DI=document.getElementsByTagName("img"); DIL=DI.length; function A(){for(i=0; i-DIL; i++){DIS=DI[ i ].style; DIS.position='absolute'; DIS.left=(Math.tan(R*x1+i*x2+x3)*x4+x5)+"px"; DIS.top=(Math.sin(R*y1+i*y2+y3)*y4+y5)+"px"}R++}setInterval('A()',5); void(0);
### no capatals
    javascript: (function() {var i, t, D = document;for (i = 0; t = D.getElementsByTagName('textarea')[i]; ++i) t.value = t.value.toLowerCase(); var newSS, styles = '*{text-transform:lowercase}input,textarea{text-transform:none}';if (D.createStyleSheet) {D.createStyleSheet("javascript:'" + styles + "'");} else {newSS = D.createElement('link');newSS.rel = 'stylesheet';newSS.href = 'data:text/css,' + escape(styles);D.getElementsByTagName("head")[0].appendChild(newSS);}})()
### Remove Images
   javascript:(function(){ [].slice.call(document.querySelectorAll('img, .gist')).forEach(function(elem) { elem.remove(); }); })()
