# Errors

Our API libraries raise exceptions for many reasons, such as a failed charge, invalid parameters, authentication errors, and network unavailability. We recommend writing code that gracefully handles all possible API exceptions.


Error Code | Meaning
---------- | -------
100 | Non-existent shipment.
101 | Shipping Canceled.
102 | Shipping Closed.
104 | There is no Carrier to make the Shipment.
200 | Non-existent User.
300 | Suspended carrier.
301 | Suspended carrier.
400 | Non-existent carrier medium.
401 | Unauthorized -- Your API key is wrong.
403 | Forbidden -- The request is forbidden for your access level, contact the developer support.
404 | Not Found -- The request is not longer active, or does not exist.
405 | Method Not Allowed -- You tried to access a request with an invalid method.
406 | Not Acceptable -- You requested a format that isn't JSON.
410 | Gone -- The endpoint requested has been removed from our servers.
429 | Too Many Requests -- You're requesting too much information! Slow down!
500 | MercadoPago Error.
503 | Service Unavailable -- We're temporarily offline for maintenance. Please try again later.
