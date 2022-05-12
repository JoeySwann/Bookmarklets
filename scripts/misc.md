# Misc. Bookmarklets
### Autoclicker
Counts in seconds and includes a nice prompt asking 'How many seconds do you want to wait before clicking again?'

    javascript:clicker:{"use strict";const{Number}=self;const milliseconds=Number.parseInt(self.prompt("How many seconds do you want to wait before clicking again?%22,%271%27),10);if(false===Number.isSafeInteger(milliseconds)){self.alert(%22Input%20was%20not%20an%20integer%22);break%20clicker;}let%20clientX=0,clientY=0;const{document}=self;self.setInterval(()=%3E{document.elementFromPoint(clientX,clientY)?.click?.();},milliseconds);document.addEventListener(%22mousemove%22,event=%3E{({clientX,clientY}=event);},{passive:true});}
### Change Background Color
_Sometimes this may not work due to scripts in the page specifying other backgrounds.<br>
Google made an [unpacked extension](https://github.com/GoogleChrome/chrome-extensions-samples/tree/main/tutorials/getting-started) that might do the work better._

    javascript:void(document.body.style.backgroundColor=prompt("Pick a Color...",""))
### Embed Site [Template]
_Place URL in the spot 'Insert URL here'._

    javascript:var frame = document.createElement('iframe'); frame.src="Insert URL here"; frame.style.position="fixed"; frame.style.top="0%"; frame.style.right="0%"; frame.style.height="600px"; frame.style.width="1300px"; frame.style.zIndex="100000"; document.body.appendChild(frame); var btn= document.createElement("button"); btn.style.position="fixed"; btn.style.top="5%"; btn.style.right="25%"; btn.zIndex="100000"; innerHTML="HIDE"; document.body.appendChild(btn);
### Freeze
This breaks the computer in various ways.<br>
DON'T TRY IT unless you are VERY CAREFUL.

    javascript:while (true) { window.location.reload(true); };
### No Color
    javascript: (function() {var newSS, styles = '* { background: white ! important; color: black !important } :link, :link * { color: #0000EE%20!important%20}%20:visited,%20:visited%20*%20{%20color:%20#551A8B%20!important%20}';if%20(document.createStyleSheet)%20{document.createStyleSheet(%22javascript:'%22%20+%20styles%20+%20%22'%22);}%20else%20{newSS%20=%20document.createElement('link');newSS.rel%20=%20'stylesheet';newSS.href%20=%20'data:text/css,'%20+%20escape(styles);document.getElementsByTagName(%22head%22)[0].appendChild(newSS);}})();
### Popup Window [Template]
_Place URL in the spot 'Insert URL here'._

    javascript:window.open('Insert URL here'),%20%27%27,%20%27top=15,left=15,scrollbar=yes,width=500,height=600%27)
### Snow
    javascript: (t => {function i() {this.D = function() {const t = h.atan(this.i / this.d);l.save(), l.translate(this.b, this.a), l.rotate(-t), l.scale(this.e, this.e * h.max(1, h.pow(this.j, .7) / 15)), l.drawImage(m, -v / 2, -v / 2), l.restore()}}window;const h = Math,r = h.random,a = document,o = Date.now;e = (t => {l.clearRect(0, 0, _, f), l.fill(), requestAnimationFrame(e);const i = .001 * y.et;y.r();const s = L.et * g;for (var n = 0; n < C.length; ++n) {const t = C[n];t.i = h.sin(s + t.g) * t.h, t.j = h.sqrt(t.i * t.i + t.f), t.a += t.d * i, t.b += t.i * i, t.a > w && (t.a = -u), t.b > b && (t.b = -u), t.b < -u && (t.b = b), t.D()}}), s = (t => {for (var e = 0; e < p; ++e) C[e].a = r() * (f + u), C[e].b = r() * _}), n = (t => {c.width = _ = innerWidth, c.height = f = innerHeight, w = f + u, b = _ + u, s()});class d {constructor(t, e = !0) {this._ts = o(), this._p = !0, this._pa = o(), this.d = t, e && this.s()}get et() {return this.ip ?%20this._pa%20-%20this._ts%20:%20o()%20-%20this._ts}get%20rt()%20{return%20h.max(0,%20this.d%20-%20this.et)}get%20ip()%20{return%20this._p}get%20ic()%20{return%20this.et%20%3E=%20this.d}s()%20{return%20this._ts%20=%20o()%20-%20this.et,%20this._p%20=%20!1,%20this}r()%20{return%20this._pa%20=%20this._ts%20=%20o(),%20this}p()%20{return%20this._p%20=%20!0,%20this._pa%20=%20o(),%20this}st()%20{return%20this._p%20=%20!0,%20this}}const%20c%20=%20a.createElement(%22canvas%22);H%20=%20c.style,%20H.position%20=%20%22fixed%22,%20H.left%20=%200,%20H.top%20=%200,%20H.width%20=%20%22100vw%22,%20H.height%20=%20%22100vh%22,%20H.zIndex%20=%20%22100000%22,%20H.pointerEvents%20=%20%22none%22,%20a.body.insertBefore(c,%20a.body.children[0]);const%20l%20=%20c.getContext(%222d%22),p%20=%20300,g%20=%205e-4,u%20=%2020;let%20_%20=%20c.width%20=%20innerWidth,f%20=%20c.height%20=%20innerHeight,w%20=%20f%20+%20u,b%20=%20_%20+%20u;const%20v%20=%2015.2,m%20=%20a.createElement(%22canvas%22),E%20=%20m.getContext(%222d%22),x%20=%20E.createRadialGradient(7.6,%207.6,%200,%207.6,%207.6,%207.6);x.addColorStop(0,%20%22hsla(255,255%,255%,1)%22),%20x.addColorStop(1,%20%22hsla(255,255%,255%,0)%22),%20E.fillStyle%20=%20x,%20E.fillRect(0,%200,%20v,%20v);let%20y%20=%20new%20d(0,%20!0),C%20=%20[],L%20=%20new%20d(0,%20!0);for%20(var%20j%20=%200;%20j%20%3C%20p;%20++j)%20{const%20t%20=%20new%20i;t.a%20=%20r()%20*%20(f%20+%20u),%20t.b%20=%20r()%20*%20_,%20t.c%20=%201%20*%20(3%20*%20r()%20+%20.8),%20t.d%20=%20.1%20*%20h.pow(t.c,%202.5)%20*%2050%20*%20(2%20*%20r()%20+%201),%20t.d%20=%20t.d%20%3C%2065%20?%2065%20:%20t.d,%20t.e%20=%20t.c%20/%207.6,%20t.f%20=%20t.d%20*%20t.d,%20t.g%20=%20r()%20*%20h.PI%20/%201.3,%20t.h%20=%2015%20*%20t.c,%20t.i%20=%200,%20t.j%20=%200,%20C.push(t)}s(),%20EL%20=%20a.addEventListener,%20EL(%22visibilitychange%22,%20()%20=%3E%20setTimeout(n,%20100),%20!1),%20EL(%22resize%22,%20n,%20!1),%20e()})()
