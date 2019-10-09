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

Example code:

```c#
            RESTClient client = new RESTClient("your_user_id", "your_api_key");

            var _params = new NameValueCollection();
            _params["list_id"] = "list_id";
            _params["email"] = "test@example.com";
            _params["firstname"] = "firstname";
            _params["lastname"] = "lastname";
            _params["ip"] = "::1";
            _params["props[source]"] = "source";
            _params["props[city]"] = "city";

            var response = client.CallMethod("subscriber", "saveSubscribe", _params);

            Response.Write(response);
```

# String Encoding

Please make sure all strings are `UTF-8` encoded.
