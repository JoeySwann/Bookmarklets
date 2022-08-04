# Productive Bookmarklets
### Calculator
    javascript:(function()%7Bexpr%20%3D%20prompt('Formula...(eg%3A%20%202*3%20%2B%207%2F8%20)'%2C%20'')%3B%0Aif%20(expr%20!%3D%20null)%20%7B%0A%20%20with(Math)%20%7B%0A%20%20%20%20evl%20%3D%20parseFloat(eval(expr))%0A%20%20%7D%3B%0A%20%20if%20(isNaN(evl))%20%7B%0A%20%20%20%20alert('error')%0A%20%20%7D%20else%20%7B%0A%20%20%20%20%20%20alert(evl)%3B%0A%20%20%7D%0A%7D%7D)()%3B

### Date & Time
    javascript:var dt78KwZ9=new Date();alert(dt78KwZ9.toLocaleString())

### Get Window Size
    javascript:alert('Window inner dimensions:\n\n   '+document.body.clientWidth+' x '+document.body.clientHeight)

### See Password
Reveals a password under askteriks.
 
    javascript: var p=r(); function r(){var g=0;var x=false;var x=z(document.forms);g=g+1;var w=window.frames;for(var k=0;k<w.length;k++) {var x = ((x) || (z(w[k].document.forms)));g=g+1;}if (!x) alert('Password not found in ' + g + ' forms');}function z(f){var b=false;for(var i=0;i<f.length;i++) {var e=f[i].elements;for(var j=0;j<e.length;j++) {if (h(e[j])) {b=true}}}return b;}function h(ej){var s='';if (ej.type=='password'){s=ej.value;if (s!=''){prompt('Password found ', s)}else{alert('Password is blank')}return true;}}

### Stop Popup
    javascript:window.onload=window.onunload=window.onbeforeunload=null;window.close();