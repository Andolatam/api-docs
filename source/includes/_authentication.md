#Authentication

Ando uses OAuth2 to allow access to the API. You can access to the APIs using your own personal account, and asking for special access to the other functionalities [by email](mailto:developers@ando.la?subject=Solicitud de API Key&body=Hola, mi nombre es _____________ y solicito una API Key para desarrollar ________________________________________ para la empresa _______________ radicada en ____________________ . Mi email de contacto es __________________ y telefono __________________ .).

First ask for an access token, using your login credentials. a TOKEN will be returned and shall be included in the HEADER of all your request as Bearer.

HTTP Request:

`POST https://api.ando.la/v1/token`

Parameter | Description
--------- | -----------
grant_type | password
username | email@domain.com
password | your-password
