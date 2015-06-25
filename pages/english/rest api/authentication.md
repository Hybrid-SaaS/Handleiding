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

## What is JQuery?##
Jquery is a JavaScript framework. For more information <a ahref="www.http://jquery.com/">Click here</a>

## What is (Unix) Epoch timestamp?
The Unix Epoch timestamp is the time in seconds since January 1, 1970. <a href="http://www.unixtimestamp.com/">Click here to read more</a>

## How to acces the rest api (in code example) ##

There is some information that is required in order to communicate with the rest api. You need to build a http request for the login page, because you will need the application id and the secret key in order to communicate with the rest api. With that information you need to hash to variables and put them in the header of the browser. All this steps will be explained in steps and code samples.

**Step one**

I recommend to import the JQuery script first. If you import this script you will be able to use functions from JQuery. 

<a href="http://code.jquery.com/jquery-2.1.4.min.js">Download JQuery here</a>

To load the JQuery script in your html page you need to add this:
	
	<script src="JQueryLocation/jquery-2.1.4.min.js"></script>


**Step two**

You need your **application id** and **secret key** from the login function in order to continue. You are able to get this information at the page: "/rest/api/login". To receive your crendentials you need to post a JSON to the login page. For example:
	
	//Attention! This example uses JQuery.
	//First import the JQuery script in your html page.
	
	$.ajax({
			method: 'POST',
			url: '/rest/api/login',
			data : '{ "username": "testUsername", "password": "testPassword", "application": "rest" }'	
	}).done(function (data) {
		//In variable data is your response.
		//To get your application id and secret key you can use this code:
		var applicationId = data.applicationId;
		var secretId = data.secret;
	});

You have now received the application id and the secret id from the rest api. In the variable "data" are the values stored. You can acces the values by using **data.variableName;**

**Step three**

When step two is completed you are now able to make a valid authenthication code. The rest api key consists of 2 parts. The first part is your application id and the second part is the secret key. In this part you need to hash the applicationId, the method of your action ("GET" or "POST"), the url you are calling (example: /rest/api/organization) and the timestamp (Epoch timestamp). Place the values in this order in a string:

>1. Application id
>2. Method type
>3. Url you are calling
>4. Epoch timestamp

The string will look like this:
> ApplicationIdTypeUrlTimestamp

**Notice: put all values together without space!**

After you put them in a string you can hash them with this function:


	var hash = CryptoJS.HmacSHA256(your_string, secret);

CryptoJS.HmacSHA256 return the hash value into the variable hash. This hash is a part that is required for the header of your browser.

Now you need to create the final string that is going to be used as a authenthication key.

Example. The authenthication key looks like this: 
>hmac256 applicationId  timeStamp hash 

**Notice: put all values together WITH A SPACE BETWEEN THE VALUES**


Now you are able to put the authenthication string into the header of the browser.

For example. I want to receive organizations:

	var headers = {};
	var authenthicationString = "hmac256 applicationId  timeStamp hash"; 
	headers["Authentication"] = authenthicationString;

	$.ajax({
			method: 'GET',
			url: '/rest/api/organizations',
			headers: headers
	}).done(function (data) {
		//In variable data is your response.
		//To get your application id and secret key you can use this code:
		var applicationId = data.applicationId;
		var secretId = data.secret;
	});



This is the full script that i have created to acces the rest api:


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



