<properties>
	<page>
		<title>Rest API Authenthication</title>
	</page>
	<menu>
		<position> Handleiding / Rest API </position> 
		<title>Authenthication</title>
	</menu>
</properties>

# Rest API authentication #
All Hybrid SaaS Rest API-interaction is signed with a Hash-based Message Authentication Code (HMAC) by using the <label keyword="hmacsha256">SHA256 hash function</label>

## Sample ##
The given sample is using a HTML-page with jQuery and CryptoJS. jQuery is a JavaScript framework. For more information <a ahref="http://jquery.com/">Click here</a>. CryptoJS is a collection of standard and secure cryptographic algorithms implemented in JavaScript using best practices and patterns. For more information <a ahref="https://code.google.com/p/crypto-js/">Click here</a>.

## How to access the Rest Api (in this code example) ##
In order to communicate with the Rest API you will need a application id and a secret. These can be obtained by requestion the */rest/api/login*-endpoint. With those variables you can sign the requests and(in the header of the request). All steps will be explained with code samples.

##Pre requirements##
Firstly, we need to include jQuery and CryptoJs in the HTML-page..

To load the jQuery script you need to add this:
	
	<script src="//code.jquery.com/jquery-2.1.4.min.js"></script>

To load the CryptoJS script you need to add this:
	
	<script src="//crypto-js.googlecode.com/svn/tags/3.1.2/build/rollups/hmac-sha256.js"></script>


##Needed variables##
You will need your **application id** and **secret key** from the login function in order to continue. You are able to get this information at the page: "/rest/api/login". To receive your crendentials you need to post a JSON to the login page:
	
	//Attention! This example uses jQuery.
	//First import the jQuery script in your html page.
	
	$.ajax({
			method: 'POST',
			url: '/rest/api/login',
			data : '{ "username": "testUsername", "password": "testPassword", "application": "rest" }'	
	}).done(function (data) {
		//In data is your response.
		//To get your application id and secret key you can use this code:
		var applicationId = data.applicationId;
		var secretId = data.secret;
	});

You have now received the application id and the secret id from the Rest API. In the variable "data" are the values stored. You can access the values by using **data.variableName;**

##Creating the hash for the request##
Each Rest API-request has to be signed. To sign the request you need the **Application Id,** the **HTTP-method**, the url you are calling (example: /rest/api/organization) and a timestamp (Epoch timestamp) and the **Secret**. 

The following values have to be concatenated in a single string in the following fixed order:

>1. Application id
>2. HTTP-method in lowercase
>3. (Relative) url you are calling
>4. Epoch timestamp


##Creating string to hash##

In this example we are going to request the organizations-endpoint, for this request we have a the following parameters:

>1. Application id: a9a0d2640fa940af8011596e3686e397
>2. Http-Method: GET
>3. Url: /rest/api/organizations?envelope=1
>4. Timestamp: 1435235082725
>5. Secret: 5ff72d0084c831a918a52b2d5c2008e53ec0d29b2c49f84ec1abd582680dcd9a

When we concatenate these values into the following format:

&lt;Application Id&gt; &lt;Http-Method&gt; &lt;Url&gt; &lt;Timestamp&gt;

we obtain the following result:

*a9a0d2640fa940af8011596e3686e397get/rest/api/organizations?envelope=11435235082725*


<div class="info">
- The Http-method has to be in lowercase
- The url has to include the trailing forward slash
</div>

<div class="warning">
Concatenate the values without spaces
</div>


##Signing the string##

The result can be hashed with the HmacSHA256 using the secret:

After you put them in a string you can hash them with this function:
	var hash = CryptoJS.HmacSHA256(string_to_hash, secret);

CryptoJS.HmacSHA256 returns the hash value into the variable hash. This hash is a part that is required to sign the request.


##Creating the Authentication header##

Now you need to create the final string that is going to be used as a authenthication key.

The authenthication key looks like this: 

&lt;Hashing protocol&gt; &lt;Application Id&gt; &lt;Timestamp&gt; &lt;Resulting Hash&gt;

<div class="warning">
Concatenate the values WITH spaces
</div>

Now you are able to put this authenthication string into the header of the request.

Example:

	var headers = {
		Authentication: "hmac256 applicationId  timeStamp hash"
	};
	$.ajax({
			method: 'GET',
			url: '/rest/api/organizations',
			headers: headers
		}
	).done(function (data) {
		//In variable data is your response.
		//To get your application id and secret key you can use this code:
		var applicationId = data.applicationId;
		var secretId = data.secret;
	});


##Working example##
This is the full script to access the Rest API

	<!--Imports jQuery library.-->
	<script src="//code.jquery.com/jquery-2.1.4.min.js"></script>
	<!--Imports the hasing algorithm (hmac256)-->
	<script src="//crypto-js.googlecode.com/svn/tags/3.1.2/build/rollups/hmac-sha256.js"></script>
	<script>
		//the applicationid and secret have already been obtained and stored in there variables:
	
		var applicationId = "a9a0d2640fa940af8011596e3686e397 ";
		var secret = "5ff72d0084c831a918a52b2d5c2008e53ec0d29b2c49f84ec1abd582680dcd9a";
		
		//Get the epoch timestamp (Epoch timestamp is the number of seconds since January 1, 1970)
		var timeStamp = new Date().getTime(); // = 1435235082725 

		//the relative path (with query) of the request.. eg: /test
		var url = '/rest/api/organizations';
		var type = 'GET';

		//Create an array with the following values.
		var stringToHash = [];
			stringToHash.push( applicationId );
			stringToHash.push( type.toLowerCase() );
			stringToHash.push( url.substring(url) ); ///make sure this is lowercase
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
			headers: {
				Authentication: headerValue.join(' ')
			},
			url: url,
			dataType: 'json', 
			processData: false,
			contentType: 'application/json; charset=utf-8',
			type: type
		};
		
		$.ajax( requestInfo )
			.done( function (data)
			{
				//alert the result
				alert( JSON.stringify(data) );
			})
			.fail( function (data)
			{
				alert('Something went wrong');
			});
	</script>



