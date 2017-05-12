# Detect SEO Crawler
Node.js module that detect SEO Bot's. This module detects requests from search engine bots and crawlers, and replies with boolen value.

Installation
----------
Install via npm.
`npm install seo-bot-detect --save`

Usage with Express.js
----------
```
var express = require('express'), 
	http = require('http'),
	request = require('request'),
	seo-bot-detect = require('seo-bot-detect');
var app = express();

app.set('port', process.env.PORT || 3000);

app.use(express.static(__dirname + '/public/images'));

app.get('/',function(req,res,next){	
	res.send(seo-bot-detect(req));
});

http.createServer(app).listen(app.get('port'), function(){
 console.log('Express server listening on port ' + app.get('port'));
});

```
