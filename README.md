[SSC](https://slatestarcodex.com/archives/):
```
var articles = []; for (article of document.querySelectorAll('div.sya_postcontent > a')) { if (!article.href.toString().includes('open-thread')) { articles.push(article.href.toString()); }; } copy(articles);
```

[ACX](https://astralcodexten.substack.com/archive):
```
var articles = []; for (article of document.querySelectorAll('div.post-preview-content > a.post-preview-title')) { if (!article.href.toString().includes('hidden')) { articles.push(article.href.toString()); }; } copy(articles);
```

Further filtering:
```
grep -v "open-thread"
grep -vP "\/ot\d+"
grep -vP "links-for"
grep -vP "links-\d+"
```