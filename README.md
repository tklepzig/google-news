# Google News API
JavaScript API for querying Google News, written in CoffeeScript.
&nbsp;

Underneat it uses Google News' RSS feeds.  
It then caches the results in-memory for comparison between poll's and only delivers the deltas as a stream.
&nbsp;

---
## Documentation

### Usage (CoffeeScript)

  	GoogleNews = require('google-news')
  	googleNews = new GoogleNews()
  
  	track = 'Volvo'
  	
  	googleNews.stream track, (stream) ->
  
    	stream.on GoogleNews.DATA, (data) ->
      		console.log 'Data Event received... '+ data.title
  
    	stream.on GoogleNews.ERROR, (error) ->
      		console.log 'Error Event received... '+ error


### Usage (JavaScript)
    
	var GoogleNews, googleNews, track;
      
    GoogleNews = require('google-news');
    googleNews = new GoogleNews();
    
    track = 'Volvo';
    
    googleNews.stream(track, function(stream) {
      
      stream.on(GoogleNews.DATA, function(data) {
        return console.log('Data Event received... ' + data.title);
      });
      
      stream.on(GoogleNews.ERROR, function(error) {
        return console.log('Error Event received... ' + error);
      });
    });
    
---

## Author
Peter Andreas Moelgaard ([GitHub](https://github.com/pmoelgaard), [Twitter](https://twitter.com/petermoelgaard))

## License
Licensed under the Apache License, Version 2.0: [http://www.apache.org/licenses/LICENSE-2.0](http://www.apache.org/licenses/LICENSE-2.0)