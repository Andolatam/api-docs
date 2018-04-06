# Errors

Our API libraries raise exceptions for many reasons, such as a failed charge, invalid parameters, authentication errors, and network unavailability. We recommend writing code that gracefully handles all possible API exceptions.


Error Code | Meaning
---------- | -------
100	| Non-existent shipment. There is not quoteID.
429	| Too Many Requests -- You're sending many requests and are unsupported by server.
500	| MercadoPago Error.
503	| Service Unavailable -- We're temporarily offline for maintenance. Please try again later.
600	| The package is too big.
601	| Wrong budget params.
602	| Promo Code does not exist.
603	| Transport does not exist.
604	| No available riders using this method.
605	| Location does not exist.
607	| Wrong email/password.
608	| User already exists. Sign up is not allowed.
609	| Incomplete params.
610	| Error Starting shipping.
611	| Error Cancelling shipping.
612	| Year must be 4 digits long.
613	| The Card is invalid.
614	| Error adding Credit Card to the user.
615	| Tracking ID doesn't exist.
616	| Invalid/Expired token.
617	| Error to find history.
