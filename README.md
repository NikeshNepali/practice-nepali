# Nikesh Nepali
## Axis Band
I like the band because their **musics are soothing** because of the __track and lyrics are also touching__.
---
## Order List (Ordered List)
---
1. Sushant KC
2. Sajjan Raj Vaidya
3. Ed Sheeran

## Books (Unordered List)
- Atomic Habits
- 48 Laws of Power
- How Habits Work.

## Visitng Places
---
Here are the fours listings of the country and places that I would Like to visit through out my life span.
|Place|Reason|Distance|Budget|
|---|---|---|---|
|Europe|Country|3810 miles|$1000|
|ABC|Beauty|43 miles|$700|
|Mustang|Culture|90 miles|$1100|
|Japan|Technology|3173 miles|$2000|

## Favourite Quotes
---
> If you miss the train I'm on, you will know that I am gone
You can hear the whistle blow a hundred miles

> Not a shirt on my back
Not a penny to my name
Lord, I can't go a-home this a-way

*-Peter, Paul and Mary*

## Code Fencing
---
This Node.js script creates a simple HTTP server that listens on port 8080 and saves any POST data sent by clients into a file called output. It uses a writable stream to efficiently write incoming data directly to the file and handles any errors that occur during writing. After receiving all the data, the server responds with a placeholder HTML form so users can submit more data. Essentially, it functions as a minimal web server that stores submitted data and provides a way for clients to continue sending more data.


```javascript
const http = require('http');
const fileSystem = require('fs');

http.createServer((request, response) => {
	// This opens up the writeable stream to `output`
	const writeStream = fileSystem.createWriteStream('./output');

	// This pipes the POST data to the file
	request.pipe(writeStream);

	// After all the data is saved, respond with a simple html form so they can post more data
	request.on('end', function() {
		response.writeHead(200, {
			"content-type": "text/html"
		});
		response.end('[-- Insert generic html FORM element here --]');
	});

	// This is here incase any errors occur
	writeStream.on('error', function(err) {
		console.log(err);
	});
}).listen(8080);```

[Node.js Snippet Source](https://pieces.app/collections/nodejs)

[My Location](MyLocation.md)
