# Web Searching Bookmarklets
### Define (selected text)
    javascript:d=""+(window.getSelection?window.getSelection():document.getSelection?document.getSelection():document.selection.createRange().text);d=d.replace(/\r\n|\r|\n/g,%22%20,%22);if(!d)d=prompt(%22Enter%20the%20words:%22,%20%22%22);if(d!=null)location=%22http://www.google.com/search?q=define:%22+escape(d).replace(/%20/g,%22+%22);void(0);
### Find Similar Words (selected text)
    javascript:var%20q=escape(window.getSelection()),i,ii;if(!q){for(i=0;i%3Cframes.length;i++){var%20fr=frames[i];try{q=escape(fr.getSelection())}catch(e){};if(q)break;else{for(ii=0;ii%3Cfr.frames.length;ii++){try{q=escape(fr.frames[ii].getSelection())}catch(e){};if(q)break;}}}}if(!q)void(q=prompt('Enter%20the%20word%20you%20want%20synonyms%20for%3A',''));if(q)void(location.href='http://www.thesaurus.com/cgi-bin/search?config=roget&words=%27+q);
### Search Archives (page URL)
    javascript: void(location.href = 'http://web.archive.org/web/*/' + escape(location.href));
### Search Google (selected text)
    javascript: q = "" + (window.getSelection ?%20window.getSelection()%20:%20document.getSelection%20?%20document.getSelection()%20:%20document.selection.createRange().text);if%20(!q)%20q%20=%20prompt(%22You%20didn%27t%20select%20any%20text.%20Enter%20a%20search%20phrase:%22,%20%22%22);if%20(q%20!=%20null)%20location%20=%20(%22http://www.google.com/search?num=100&q=site:%22%20+%20escape(location.hostname)%20+%20%22%20\%22%22%20+%20escape(q.replace(/\%22/g,%20%22%22))%20+%20%22\%22%22).replace(/%20/g,%20%22+%22);void%200
### Translate (selected text)
    javascript:var t=((window.getSelection&&window.getSelection())||(document.getSelection&&document.getSelection())||(document.selection &&document.selection.createRange&&document.selection.createRange().text));var e=(document.charset||document.characterSet);if(t!=''){location.href='http://translate.google.com/translate_t?text=%27+t+%27&hl=en&tbb=1&ie=%27+e;}else{location.href=%27http://translate.google.com/translate?u=%27+escape(location.href)+%27&hl=en&tbb=1&ie=%27+e;};
