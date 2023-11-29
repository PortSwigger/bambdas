# Proxy HTTP
Documentation: [Filtering the HTTP history with Bambdas](https://portswigger.net/burp/documentation/desktop/tools/proxy/http-history/bambdas)
## [FilterOnCookieValue.bambda](https://github.com/PortSwigger/bambdas/blob/main/Proxy/HTTP/FilterOnCookieValue.bambda)
### Filters Proxy HTTP history for requests with a specific Cookie value.
#### Author: LostCoder
```java
if (requestResponse.request().hasParameter("foo", HttpParameterType.COOKIE)) {
	var cookieValue = requestResponse
		.request()
		.parameter("foo", HttpParameterType.COOKIE)
		.value();

	return cookieValue.contains("1337");
}

return false;

```
## [FilterOutOptionsRequests.bambda](https://github.com/PortSwigger/bambdas/blob/main/Proxy/HTTP/FilterOutOptionsRequests.bambda)
### Filter out OPTIONS requests.
#### Author: Trikster
```java
return !requestResponse.request().method().equals("OPTIONS");

```
## [FindJSONresponsesWithIncorrectContentType.bambda](https://github.com/PortSwigger/bambdas/blob/main/Proxy/HTTP/FindJSONresponsesWithIncorrectContentType.bambda)
### Finds JSON responses with wrong Content-Type  The content is probably json but the content type is not application/json
#### Author: albinowax
```java
var contentType = requestResponse.hasResponse() ? requestResponse.response().headerValue("Content-Type") : null;

if (contentType != null && !contentType.contains("application/json")) {
 String body = requestResponse.response().bodyToString().trim();

 return body.startsWith( "{" ) || body.startsWith( "[" );
}

return false;

```
## [FindRolesWithinJWTClaims.bambda](https://github.com/PortSwigger/bambdas/blob/main/Proxy/HTTP/FindRolesWithinJWTClaims.bambda)
### Find role within JWT claims
#### Author: Trikster
```java
return requestResponse.annotations().highlightColor().equals(HighlightColor.CYAN);
```