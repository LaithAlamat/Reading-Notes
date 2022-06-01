# MVC && Cookies
An HTTP cookie (web cookie, browser cookie) is a small piece of data that a server sends to a user's web browser. The browser may store the cookie and send it back to the same server with later requests. Typically, an HTTP cookie is used to tell if two requests come from the same browser—keeping a user logged in, for example. It remembers stateful information for the stateless HTTP protocol.

Cookies were once used for general client-side storage. Now modern API's are used for such use.

Cookies are sent with every request, so they can worsen performance (especially for mobile data connections).

The browser usually stores the cookie and sends it with requests made to the same server inside a Cookie HTTP header.

 You can specify an expiration date or time period after which the cookie shouldn't be sent.

 The Domain and Path attributes define the scope of a cookie: what URLs the cookies should be sent to.

## Cookies Benefits
- Session management:

Logins, shopping carts, game scores, or anything else the server should remember

- Personalization:

User preferences, themes, and other settings

- Tracking

Recording and analyzing user behavior

### Set-Cookie
The Set-Cookie HTTP response header sends cookies from the server to the user agent. A simple cookie is set like this:

    Set-Cookie: <cookie-name>=<cookie-value>


### Lifetime of a Cookie


The lifetime of a cookie can be defined in two ways:

- Session cookies are deleted when the current session ends. The browser defines when the "current session" ends, and some browsers use session restoring when restarting. This can cause session cookies to last indefinitely.

- Permanent cookies are deleted at a date specified by the Expires attribute, or after a period of time specified by the Max-Age attribute.

### Restrict access to cookies
You can ensure that cookies are sent securely and aren't accessed by unintended parties or scripts in one of two ways: with the Secure attribute and the HttpOnly attribute.

A cookie with the HttpOnly attribute is inaccessible to the JavaScript Document.cookie API; it's only sent to the server.

### Automatic cookie removal
There are a few reasons why a cookie might be automatically removed by the browser:

- Session cookies are removed when the session is over (browser is closed).

- Persistent cookies are removed when the expiration date and time have been reached.

- If the browser’s cookie limit is reached, then cookies will be removed to make room for the most recently created cookie. For more details, see my post on cookie restrictions.

- Cookie management is important to avoid any of these automatic removal cases when they are unintended.

### Subcookies
Due to the cookie number limit, developers have come up with the idea of subcookies to increase the amount of storage available to them. Subcookies are name-value pairs stored within a cookie value