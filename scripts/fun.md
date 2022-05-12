# Fun Bookmarklets
### Crooked Page
    javascript:(function(){['', '-ms-', '-webkit-', '-o-', '-moz-'].map(function(prefix){Array.prototype.slice.call(document.querySelectorAll('div,p,span,img,a,body')).map(function(el){el.style[prefix + 'transform'] = 'rotate(' + (Math.floor(Math.random() * 3) - 1) + 'deg)';});});}())

### Piano
    javascript:(function(){var js=document.body.appendChild(document.createElement("script"));js.onerror=function(){alert("Sorry, the script could not be loaded.")};js.src="https://rawgit.com/Krazete/bookmarklets/master/piano.js"})();

### Ponies
    https://panzi.github.io/Browser-Ponies/

### Rotate Page 360
    javascript:(function(){var s=document.createElement('style');s.innerHTML='%40-moz-keyframes roll { 100%25 { -moz-transform: rotate(129600deg); } } %40-o-keyframes roll { 100%25 { -o-transform: rotate(129600deg); } } %40-webkit-keyframes roll { 100%25 { -webkit-transform: rotate(129600deg); } } body{ -moz-animation-name: roll; -moz-animation-duration: 1440s; -moz-animation-iteration-count: 360; -o-animation-name: roll; -o-animation-duration: 1440s; -o-animation-iteration-count: 360; -webkit-animation-name: roll; -webkit-animation-duration: 1440s; -webkit-animation-iteration-count: 360; }';document.getElementsByTagName('head')[0].appendChild(s);}());

### Snake
_Essentially a basic game - the snake goes for the apple.<br>
Google has a fancy version if you search for the word 'snake', but this is pretty good too.<br>
Original:_
    
    javascript:for(Q=80,m=b=Q*Q,a=[P=l=u=d=p=S=w=0],u=89,f=(h=j=t=(b+Q)/2)-1,(B=(D=document).body).appendChild(x=D.createElement('p')),(X=x.style).position='fixed',X.left=X.top=0,X.background='#FFF',x.innerHTML='%3Cp%3E%3C/p%3E%3Ccanvas%3E',v=(s=x.childNodes)[0],(s=s[1]).width=s.height=Q*5,c=s.getContext('2d'),onkeydown=onblur=F=function(e,z){z?a[f]?(w+=m,f=Math.random(l+=8)*(R=Q-2)*R|(u=0),F(f+=Q+1+(f/R|0)*2,z)):F(f):e%3C0?(l?--l:(y=t,t=a[t]-2,F(y)),S+=(w*=.8)/4,m=999/(u+++10),a[h+=[-1,-Q,1,Q][d=p]]?B.removeChild(x,alert('Game%20Over')):(F(h),F(e,j=h),v.innerHTML=P?(setTimeout(F,50,e,0),S|0):'Press%20P')):-e?(y=(a[e]=e%3CQ|e%3E=Q*Q-Q|!(e%Q)|e%Q==Q-1|(e==h)*2)+(e==f),e==h&&(a[j]=2+h),c.fillStyle='hsl('+!a[e]*142+','+m*2+'%,'+y*31+'%)',c.fillRect(e%Q*5,(e/Q|0)*5,5,5)):isNaN(y=e.keyCode-37)|y==43?(P=y&&!P)&&F(-1):p=!P|y&-4|!(y^2^d)?p:y;return!1};--b;F(b));void%20F(-1)

_With grid:_

    javascript:for(Q=80,m=b=Q*Q,a=[P=l=u=d=p=S=w=0],u=89,f=(h=j=t=(b+Q)/2)-1,(B=(D=document).body).appendChild(x=D.createElement('p')),(X=x.style).position='fixed',X.left=X.top=0,X.background='#FFF',x.innerHTML='%3Cp%3E%3C/p%3E%3Ccanvas%3E',v=(s=x.childNodes)[0],(s=s[1]).width=s.height=Q*5,c=s.getContext('2d'),onkeydown=onblur=F=function(e,z){z?a[f]?(w+=m,f=Math.random(l+=8)*(R=Q-2)*R|(u=0),F(f+=Q+1+(f/R|0)*2,z)):F(f):e%3C0?(l?--l:(y=t,t=a[t]-2,F(y)),S+=(w*=.8)/4,m=999/(u+++10),a[h+=[-1,-Q,1,Q][d=p]]?B.removeChild(x,alert('Game%20Over')):(F(h),F(e,j=h),v.innerHTML=P?(setTimeout(F,50,e,0),S|0):'Press%20P')):-e?(y=(a[e]=e%3CQ|e%3E=Q*Q-Q|!(e%Q)|e%Q==Q-1|(e==h)*2)+(e==f),e==h&&(a[j]=2+h),c.fillStyle='hsl('+!a[e]*105+','+m*69+'%,'+y*30+'%)',c.fillRect(e%Q*5,(e/Q|0)*5,4,4)):isNaN(y=e.keyCode-37)|y==43?(P=y&&!P)&&F(-1):p=!P|y&-4|!(y^2^d)?p:y;return!1};--b;F(b));void%20F(-1)

### Spinny Cursor
    javascript:iV33MaET=0;Cu4Xg8Y=new Array('n-resize','nw-resize','w-resize','sw-resize','s-resize','se-resize','e-resize','ne-resize');setInterval('iV33MaET++;document.body.style.cursor=Cu4Xg8Y[iV33MaET%8]',150)

### Star Wars
    javascript:(function(c){var a=c.body.style;c.documentElement.style.background=a.background="black";a.color="yellow";a.height=a.width="100%";a.position="fixed";a.overflowY="scroll";a.top="-15%";a.webkitTransform=a.MozTransform=a.transform="matrix3d(1,0,0,0,0,1,0,-0.0015,0,0,1,0,0,0,0,1)";for(var a=c.body.children,b=0;b<a.length;b++)"SCRIPT"!=a[b].nodeName&&(a[b].style.overflowY="scroll",a[b].style.maxHeight="100%");var b=new Audio();b.src="https://archive.org/download/StarWarsThemeSongByJohnWilliams/Star Wars Theme Song By John Williams.mp3";var f=function(){for(var a,b=0;a=c.body.children[b];b++)"SCRIPT"!=a.nodeName&&(a.scrollTop+=2);setTimeout(f,50)};setTimeout(f,1000);b.load();b.play()})(document)
