<properties>
	<page>
		<title>Wall of Fame</title>
	</page>
	<menu>
		<position> Handleiding / Rest API </position> 
		<title>Authenthication</title>
	</menu>
</properties>

# Rest API authentication #




## Introduction ##
The Hybrid SaaS rest API is using a API key to gain access to the system. The API key is hashed with the HmacSHA256 algorithm. This hash is required to receive data from the rest api. This article shows you some examples and how to do this in code.


## What is HmacSHA256? ##

<a href="https://en.wikipedia.org/wiki/Hash-based_message_authentication_code">Click here for to read more about Hmac hasing.</a>

## How to acces the rest api (in code example) ##

To get information from the rest api, you need to do a http request. To execute a http request you can use the code library JQuery in JavaScript.

<!--<!doctype html>
<html>
 <head>
  <title>Authenthication preview</title>
 </head>
 <body>
	<!--Imports JQuery library.-->
	<script src="//code.jquery.com/jquery-2.1.4.min.js"></script>
	<!--Imports the hasing algorithm (hmac256)-->
	<script src="//crypto-js.googlecode.com/svn/tags/3.1.2/build/rollups/hmac-sha256.js"></script>
	<script>
		//Your rest api key contains two values. The first part before the ":" is the application id an the second part after the ":" contains the secretId.
		//You can receive those id's from the login function of the rest API.
		var API_KEY = 'applicationId:secretId';

		//This will split the application id and the secret id in an array. 
		//apiSplit[0] is applicationId
		//apisplit[1] is secretId
		var apiSplit = API_KEY.split(':');

		var applicationId = apiSplit[0];
		var secret = apiSplit[1];
		
		//Get the epoch timestamp (Epoch timestamp is the number of seconds since January 1, 1970)
		var timeStamp = new Date().getTime();

		//the relative path (with query) of the request.. eg: /test
		var url = '/rest/api/organizations';
		var type = 'GET';

		//Creates the string to put in the header.
		var stringToHash = [];
			stringToHash.push( applicationId );
			stringToHash.push( type.toLowerCase() );
			stringToHash.push( url.substring(url) );
			stringToHash.push( timeStamp );

		//Create hash with the Hmac algorithm.
		var hash = CryptoJS.HmacSHA256(stringToHash.join(''), secret);

		//Create authentication header:
		var headerValue = [];

		//The hashing method in lowercase
		headerValue.push( 'hmac256' );

		//Application id
		headerValue.push( applicationId );

		//The epoch
		headerValue.push( timeStamp );

		//The hash
		headerValue.push( hash );

		var requestInfo = {
			headers: {},
			url: url,
			dataType: 'json', 
			processData: false,
			contentType: 'application/json; charset=utf-8',
			type: type
		};
		
		requestInfo.headers["Authentication"] = headerValue.join(' ');

		$.ajax( requestInfo )
		.done( function (data)
		{
			//variable 'data' is now a JSON object with your data.
		})
		.fail( function (data)
		{
		  //This functions handles if you request contains an error.
		});
	</script>
 </body>
</html>




