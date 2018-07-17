# Newsman .NET API Client - version 1.2

This is the Newsman App .NET API client for API version 1.2.

## Newsman - Smart Email Service Provider

[Newsman](http://www.newsmanapp.com "Smart Email Service Provider") is a Smart Email Service Provider. 
We send newsletters on behalf of our customers.

## About Newsman API - version 1.2

Our current API version is 1.2. API documentation can be found here:

* RO: http://kb.newsman.ro/api/
* EN: http://kb.newsmanapp.com/api/
* FR: http://kb.newsman.fr/api/
 
Our API requires an API KEY which you can generate in your Account and your Newsman user id.
The API exposes XML RPC and REST interfaces.

### REST

The REST *call type* is done over HTTP POST.

* using System.Net;

Example code:

```php
<?php
RESTClient client = new RESTClient("userid", "apikey");
var _params = new NameValueCollection();
    _params["list_id"] = "listid";
var response = client.CallMethod("subscriber", "saveSubscribe", _params);
?>
```

# String Encoding

Please make sure all strings are `UTF-8` encoded.