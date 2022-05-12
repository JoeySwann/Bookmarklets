# Productive Bookmarklets
### Calculator
    javascript:expr=prompt('Formula...(eg:  2*3 + 7/8 )','');if(expr!=null){with(Math){evl=parseFloat(eval(expr))};if(isNaN(evl)){alert('Error 404: Forbidden%27)}else{alert(evl)}}else{void(null)}

### Date & Time
    javascript:var dt78KwZ9=new Date();alert(dt78KwZ9.toLocaleString())

### Embedded Notepad
Find your notes in the form of a webpage [here](https://offline-editor--adcharity.repl.co/optimized.html).<br>
THE NOTEPAD IS ACTUALLY SUPPORTED BY A CERTAIN WEBSITE. THAT WEBSITE MAY BE ABLE TO SEE YOUR NOTES.<br>

    javascript:(function() {document.body.innerHTML+='<iframe style=\"width: 25%;border: 3px solid black; z-index: 100000000000; position: fixed; bottom: 0; right: 0; height: 50%;\" src=\"https://offline-editor--adcharity.repl.co/optimized.html\">';})();

### Get Window Size
    javascript:alert('Window inner dimensions:\n\n   '+document.body.clientWidth+' x '+document.body.clientHeight)

### "Quicksandify"
This one is nice by making SOME text on a webpage in the font Quicksand and doing a few other things.<br>
On the wrong site, it's a page destoryer. If you want a better simplifier, try [this](https://chrome.google.com/webstore/detail/just-read/dgmanlpmmkibanfdgjocnabmcaclkmod?hl=en).

     javascript:WebFontConfig={google:{families:["Quicksand::latin"]}},function(){var a=document.createElement("script");a.src="https://ajax.googleapis.com/ajax/libs/webfont/1/webfont.js",a.type="text/javascript",a.async="true";var b=document.getElementsByTagName("script")[0];b.parentNode.insertBefore(a,b)}();(function(){var elems=document.getElementsByTagName("*");for(var i = 0; i<elems.length;i++){elems[i].style.fontFamily="Quicksand";document.body.style.background="black"; elems[i].style.color="white"}})();

### See Password
Reveals a password under askteriks.
 
    javascript: var p=r(); function r(){var g=0;var x=false;var x=z(document.forms);g=g+1;var w=window.frames;for(var k=0;k<w.length;k++) {var x = ((x) || (z(w[k].document.forms)));g=g+1;}if (!x) alert('Password not found in ' + g + ' forms');}function z(f){var b=false;for(var i=0;i<f.length;i++) {var e=f[i].elements;for(var j=0;j<e.length;j++) {if (h(e[j])) {b=true}}}return b;}function h(ej){var s='';if (ej.type=='password'){s=ej.value;if (s!=''){prompt('Password found ', s)}else{alert('Password is blank')}return true;}}

### Stop Popup
    javascript:window.onload=window.onunload=window.onbeforeunload=null;window.close();

### YouTube Engagement
Shows likes to views in a ratio.

    function engage() { setTimeout(engage, 1000); Array.from(document.getElementsByTagName("ytd-thumbnail")).forEach(function(e) { var oldLink = e.getAttribute("value"); var newLink = e.children[0].href; if (oldLink != newLink) { e.setAttribute("value", newLink); e.style.borderBottom = ""; e.style.borderImage = ""; e.style.borderImageSlice = ""; e.style.paddingBottom = ""; e.style.marginTop = ""; var xhr = new XMLHttpRequest(); xhr.open("GET", newLink, true); xhr.onload = function() { var ytid = JSON.parse(this.responseText.match(/var ytInitialData = ({.+?});/)[1]); if (!ytid.contents.twoColumnWatchNextResults.results.results.contents[0].videoPrimaryInfoRenderer.viewCount.videoViewCountRenderer.isLive) { try { var likes = parseInt(ytid.contents.twoColumnWatchNextResults.results.results.contents[0].videoPrimaryInfoRenderer.videoActions.menuRenderer.topLevelButtons[0].toggleButtonRenderer.defaultText.accessibility.accessibilityData.label.replace(/\D/g, "")); var views = parseInt(ytid.contents.twoColumnWatchNextResults.results.results.contents[0].videoPrimaryInfoRenderer.viewCount.videoViewCountRenderer.viewCount.simpleText.replace(/\D/g, "")); var rating = views ? 100 * Math.log(likes + 1) / Math.log(views + 1) : 0; e.style.borderBottom = "3px solid"; e.style.borderImage = "linear-gradient(to right, #008000 " + rating + "%, #404040" + rating + "%)"; e.style.borderImageSlice = "1"; e.style.paddingBottom = "2px"; e.style.marginTop = "-1px"; } catch (e) { console.log(ytid.contents.twoColumnWatchNextResults.results.results.contents[0].videoPrimaryInfoRenderer.title.runs[0].text); } } }; xhr.send(); } }); } engage();

### YouTube Scroller
Allows you to watch the video as you read comments or look through the Up Next by placing it in the top right of the page.

    function videoAnchor() { var miniplayer = document.getElementsByClassName("miniplayer")[0]; if (miniplayer.parentElement.active) { return; } var player = document.getElementById("movie_player"); var video = document.getElementsByTagName("video")[0]; var control = document.getElementsByClassName("ytp-chrome-bottom")[0]; var mastRect = document.getElementById("masthead-container").getBoundingClientRect(); var theaterRect = document.querySelector("#player-container.ytd-watch-flexy").getBoundingClientRect(); player.removeAttribute("style"); /* reset for theaterRect height */ var playerRect = player.getBoundingClientRect(); var videoRect = video.getBoundingClientRect(); if (theaterRect.bottom < mastRect.height) { var comment = ( document.getElementById("primary-inner") || document.getElementById("primary") ); var commentRect = comment.getBoundingClientRect(); var widthRatio = (window.innerWidth - commentRect.right) / videoRect.width; var heightRatio = window.innerHeight / videoRect.height; player.style.position = "fixed"; player.style.right = 0; player.style.top = mastRect.height + "px"; player.style.width = videoRect.width + "px"; player.style.height = videoRect.height + "px"; player.style.transformOrigin = "right top"; player.style.transform = "scale(" + Math.min(widthRatio, heightRatio) + ")"; player.style.zIndex = 1500; control.style.left = "12px"; control.style.width = (videoRect.width - 24) + "px"; video.style.left = 0; } else { control.style.left = "12px"; control.style.width = (playerRect.width - 24) + "px"; video.style.left = (playerRect.width - videoRect.width) / 2 + "px"; } } /* keep scroll position on timestamp click */ function scrollAnchor() { var x = window.scrollX; var y = window.scrollY; var t0; function scrollToXY(t1) { window.scrollTo(x, y); if (typeof t0 == "undefined") { t0 = t1; } if (t1 - t0 < 1) { requestAnimationFrame(scrollToXY); } } requestAnimationFrame(scrollToXY); } window.addEventListener("scroll", videoAnchor); window.addEventListener("resize", videoAnchor); window.addEventListener("mouseup", scrollAnchor);
