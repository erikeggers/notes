# HTTP
## Meaning
**Hypertext Transfer Protocol**
A set of rules for how computers should communicate.

Current version is HTTP 1.1

## REST
Representational State Transfer

### Meaning
There are resources on a remote computer, and I want to be able to fetch, manipulate, and delete those resources.

RESTful URLs can be accessed as well named resources.

e.g. https://github.com/jacobthemyth/dotfiles means get the `dotfiles` repository from the `jacobthemyth` user.

## URLs, Methods, Statuses
### URL
The parts of the URL should represent different resources, some of which are nested.

### Methods
- GET: fetches the resource
- POST: create the resource
- PUT: update the resource
- DELETE: deletes the resource.
- PATCH: update the resource (not supported in IE8)

Great example: https://developer.github.com/v3/repos/

## $.ajax and JSON APIs
### jQuery.ajax
Ajax requests are sent using the method `$.ajax`. There are many options and
settings for this method, so be sure to check [the
documentation](http://api.jquery.com/jquery.ajax/).

### jqXHR
Calling `$.ajax` returns an object called the jqXHR. See the documentation to
see examples of executing functions after the request is finished:
http://api.jquery.com/jquery.ajax/#jqXHR

#### Further Reading
http://jqfundamentals.com/chapter/ajax-deferreds

### Content type
The content type is the type of content you're sending to the server.

Usually we would use the header `Content-Type: application/json` when sending
JSON, but you should check the documentation of the API to see what the
requirements are for that particular API. For example, some APIs require the
data to be sent as form data, which is the default of $.ajax.

```js
$.ajax({
  url: apiURL,
  contentType: 'application/json'
});
```

### Data type
The data type is the type of content you're expecting back from the server.

Usually jQuery will automatically detect this based on the type of data you put
in the `data` property, but sometimes it's necessary to say, for example, that
you're expecting jsonp instead of json.

```js
$.ajax({
  url: apiURL,
  data: {title: "Cool"},
  dataType: 'jsonp'
});
```

### Statuses
http://httpstatus.es/
The ones you should be most familiar with:
- 200
- 201
- 400
- 404
- 401
- 500

