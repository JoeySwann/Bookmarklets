# Coding Bookmarklets
### Inject jQuery
    javascript:void(function(){document.body.appendChild(document.createElement('script')).src='https://code.jquery.com/jquery-3.6.0.js' })();

### Inject Script
    javascript:(function()%7Bvar%20x%20%3D%20prompt('Script%20URL%3A%5Cn%5CnIf%20you%5C're%20importing%20from%20Github%2C%20open%20it%20raw.')%3B%0A%20%20try%20%7B%0A%20%20%20%20document.body.appendChild(document.createElement('script')).src%20%3D%20x%3B%0A%20%20%20%20alert('Script%20injected!')%3B%0A%20%20%7D%20catch%20(e)%20%7B%0A%20%20%20%20alert('Error%20injecting%20script.%20Most%20likely%20that%20you%20didn%5C't%20get%20the%20right%20URL.%5Cn%5CnError%20(for%20devs)%3A%20'%20%2B%20e)%3B%0A%20%20%7D%7D)()%3B