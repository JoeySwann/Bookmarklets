# Fun Bookmarklets
### Crooked Page
    javascript:(function(){['', '-ms-', '-webkit-', '-o-', '-moz-'].map(function(prefix){Array.prototype.slice.call(document.querySelectorAll('div,p,span,img,a,body')).map(function(el){el.style[prefix + 'transform'] = 'rotate(' + (Math.floor(Math.random() * 3) - 1) + 'deg)';});});}())

### Piano
    javascript:(function(){var js=document.body.appendChild(document.createElement("script"));js.onerror=function(){alert("Sorry, the script could not be loaded.")};js.src="https://rawgit.com/Krazete/bookmarklets/master/piano.js"})();

### Ponies
    https://panzi.github.io/Browser-Ponies/

### Rotate Page 360
    javascript:(function(){var s=document.createElement('style');s.innerHTML='%40-moz-keyframes roll { 100%25 { -moz-transform: rotate(129600deg); } } %40-o-keyframes roll { 100%25 { -o-transform: rotate(129600deg); } } %40-webkit-keyframes roll { 100%25 { -webkit-transform: rotate(129600deg); } } body{ -moz-animation-name: roll; -moz-animation-duration: 1440s; -moz-animation-iteration-count: 360; -o-animation-name: roll; -o-animation-duration: 1440s; -o-animation-iteration-count: 360; -webkit-animation-name: roll; -webkit-animation-duration: 1440s; -webkit-animation-iteration-count: 360; }';document.getElementsByTagName('head')[0].appendChild(s);}());

### Star Wars
    javascript:(function(c){var a=c.body.style;c.documentElement.style.background=a.background="black";a.color="yellow";a.height=a.width="100%";a.position="fixed";a.overflowY="scroll";a.top="-15%";a.webkitTransform=a.MozTransform=a.transform="matrix3d(1,0,0,0,0,1,0,-0.0015,0,0,1,0,0,0,0,1)";for(var a=c.body.children,b=0;b<a.length;b++)"SCRIPT"!=a[b].nodeName&&(a[b].style.overflowY="scroll",a[b].style.maxHeight="100%");var b=new Audio();b.src="https://archive.org/download/StarWarsThemeSongByJohnWilliams/Star Wars Theme Song By John Williams.mp3";var f=function(){for(var a,b=0;a=c.body.children[b];b++)"SCRIPT"!=a.nodeName&&(a.scrollTop+=2);setTimeout(f,50)};setTimeout(f,1000);b.load();b.play()})(document)
