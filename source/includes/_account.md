#Account

## Get My Account
```shell
curl --request GET \
  --url 'https://api.ando.la/v1/user?email=raulmatadero@gmail.com&token=x5hjZCSKds2TeHatAvoX4FTLONOSmKsjWh5Av6tIZ8oxxaMH780jvcpELMub6XtJFJ_WReZnGHahrLdj_0GRyX-XgTazgFKueD12pSbX-Cg4xCplQF-qlC6UPd3nQINA5qpBxVDb1h3am4swKzHBq2PBCymNtKJ9QtUMvQHVNhP_XX9H6zLhXDLzJ0hjT3iCe6l_S_1qMm_EzkKPI5wJdGmlbGCMjkzsx9PmApokz1TJguA0zMrVF9iHHXaqazk_FwSXUIv4nFyhRmMqHwC0Gdwx_P25l0CjB207KNuhKRo'
```

```javascript
var http = require("http");

var options = {
  "method": "GET",
  "hostname": [
    "https://api.ando.la"
  ],
  "path": [
    "v1",
    "user"
  ],
  "headers": {}
};

var req = http.request(options, function (res) {
  var chunks = [];

  res.on("data", function (chunk) {
    chunks.push(chunk);
  });

  res.on("end", function () {
    var body = Buffer.concat(chunks);
    console.log(body.toString());
  });
});

req.end();
```

```ruby
require 'uri'
require 'net/http'

url = URI("https://api.ando.la/v1/user?email=raulmatadero@gmail.com&token=x5hjZCSKds2TeHatAvoX4FTLONOSmKsjWh5Av6tIZ8oxxaMH780jvcpELMub6XtJFJ_WReZnGHahrLdj_0GRyX-XgTazgFKueD12pSbX-Cg4xCplQF-qlC6UPd3nQINA5qpBxVDb1h3am4swKzHBq2PBCymNtKJ9QtUMvQHVNhP_XX9H6zLhXDLzJ0hjT3iCe6l_S_1qMm_EzkKPI5wJdGmlbGCMjkzsx9PmApokz1TJguA0zMrVF9iHHXaqazk_FwSXUIv4nFyhRmMqHwC0Gdwx_P25l0CjB207KNuhKRo")

http = Net::HTTP.new(url.host, url.port)

request = Net::HTTP::Get.new(url)

response = http.request(request)
puts response.read_body
```

```python
import requests

url = "https://api.ando.la/v1/user"

querystring = {"email":"raulmatadero@gmail.com","token":"x5hjZCSKds2TeHatAvoX4FTLONOSmKsjWh5Av6tIZ8oxxaMH780jvcpELMub6XtJFJ_WReZnGHahrLdj_0GRyX-XgTazgFKueD12pSbX-Cg4xCplQF-qlC6UPd3nQINA5qpBxVDb1h3am4swKzHBq2PBCymNtKJ9QtUMvQHVNhP_XX9H6zLhXDLzJ0hjT3iCe6l_S_1qMm_EzkKPI5wJdGmlbGCMjkzsx9PmApokz1TJguA0zMrVF9iHHXaqazk_FwSXUIv4nFyhRmMqHwC0Gdwx_P25l0CjB207KNuhKRo"}

response = requests.request("GET", url, params=querystring)

print(response.text)
```

```php
<?php

$curl = curl_init();

curl_setopt_array($curl, array(
  CURLOPT_URL => "https://api.ando.la/v1/user?email=raulmatadero@gmail.com&token=x5hjZCSKds2TeHatAvoX4FTLONOSmKsjWh5Av6tIZ8oxxaMH780jvcpELMub6XtJFJ_WReZnGHahrLdj_0GRyX-XgTazgFKueD12pSbX-Cg4xCplQF-qlC6UPd3nQINA5qpBxVDb1h3am4swKzHBq2PBCymNtKJ9QtUMvQHVNhP_XX9H6zLhXDLzJ0hjT3iCe6l_S_1qMm_EzkKPI5wJdGmlbGCMjkzsx9PmApokz1TJguA0zMrVF9iHHXaqazk_FwSXUIv4nFyhRmMqHwC0Gdwx_P25l0CjB207KNuhKRo",
  CURLOPT_RETURNTRANSFER => true,
  CURLOPT_ENCODING => "",
  CURLOPT_MAXREDIRS => 10,
  CURLOPT_TIMEOUT => 30,
  CURLOPT_HTTP_VERSION => CURL_HTTP_VERSION_1_1,
  CURLOPT_CUSTOMREQUEST => "GET",
));

$response = curl_exec($curl);
$err = curl_error($curl);

curl_close($curl);

if ($err) {
  echo "cURL Error #:" . $err;
} else {
  echo $response;
}
```

```go
package main

import (
	"fmt"
	"net/http"
	"io/ioutil"
)

func main() {

	url := "https://api.ando.la/v1/user?email=raulmatadero@gmail.com&token=x5hjZCSKds2TeHatAvoX4FTLONOSmKsjWh5Av6tIZ8oxxaMH780jvcpELMub6XtJFJ_WReZnGHahrLdj_0GRyX-XgTazgFKueD12pSbX-Cg4xCplQF-qlC6UPd3nQINA5qpBxVDb1h3am4swKzHBq2PBCymNtKJ9QtUMvQHVNhP_XX9H6zLhXDLzJ0hjT3iCe6l_S_1qMm_EzkKPI5wJdGmlbGCMjkzsx9PmApokz1TJguA0zMrVF9iHHXaqazk_FwSXUIv4nFyhRmMqHwC0Gdwx_P25l0CjB207KNuhKRo"

	req, _ := http.NewRequest("GET", url, nil)

	res, _ := http.DefaultClient.Do(req)

	defer res.Body.Close()
	body, _ := ioutil.ReadAll(res.Body)

	fmt.Println(res)
	fmt.Println(string(body))

}
```
### HTTP Request

`GET https://api.ando.la/v1/user?email=raulmatadero@gmail.com&token=4b73b4b73b11dc60ee75959eca2c117614e9741dfc99a`

Header | Content
--------- | -----------
Authorization | Bearer 4b73b11dc60ee75959eca2c117614e9741dfc99a
Content-type | application/json

### URL Parameters

Parameter | Description
--------- | -----------
Email | Your email.
Token | Your Bearer Token.

## Recover Password

```shell
curl --request POST \
  --url 'https://api.ando.la/v1/recover/password' \
  --header 'Content-Type: application/json' \
  --data '{
"email": "francogoytia@gmail.com"  
}'
```

```javascript
var http = require("http");

var options = {
  "method": "POST",
  "hostname": [
    "https://api.ando.la"
  ],
  "path": [
    "v1",
    "recover",
    "password"
  ],
  "headers": {
    "Content-Type": "application/json"
  }
};

var req = http.request(options, function (res) {
  var chunks = [];

  res.on("data", function (chunk) {
    chunks.push(chunk);
  });

  res.on("end", function () {
    var body = Buffer.concat(chunks);
    console.log(body.toString());
  });
});

req.write(JSON.stringify({ email: 'francogoytia@gmail.com' }));
req.end();
```

```ruby
require 'uri'
require 'net/http'

url = URI("https://api.ando.la/v1/recover/password")

http = Net::HTTP.new(url.host, url.port)

request = Net::HTTP::Post.new(url)
request["Content-Type"] = 'application/json'
request.body = "{ \n\"email\": \"francogoytia@gmail.com\"  \n}"

response = http.request(request)
puts response.read_body
```

```python
import requests

url = "https://api.ando.la/v1/recover/password"

payload = "{ \n\"email\": \"francogoytia@gmail.com\"  \n}"
headers = {'Content-Type': 'application/json'}

response = requests.request("POST", url, data=payload, headers=headers)

print(response.text)
```

```php
<?php

$curl = curl_init();

curl_setopt_array($curl, array(
  CURLOPT_URL => "https://api.ando.la/v1/recover/password",
  CURLOPT_RETURNTRANSFER => true,
  CURLOPT_ENCODING => "",
  CURLOPT_MAXREDIRS => 10,
  CURLOPT_TIMEOUT => 30,
  CURLOPT_HTTP_VERSION => CURL_HTTP_VERSION_1_1,
  CURLOPT_CUSTOMREQUEST => "POST",
  CURLOPT_POSTFIELDS => "{ \n\"email\": \"francogoytia@gmail.com\"  \n}",
  CURLOPT_HTTPHEADER => array(
    "Content-Type: application/json"
  ),
));

$response = curl_exec($curl);
$err = curl_error($curl);

curl_close($curl);

if ($err) {
  echo "cURL Error #:" . $err;
} else {
  echo $response;
}
```

```go
package main

import (
	"fmt"
	"strings"
	"net/http"
	"io/ioutil"
)

func main() {

	url := "https://api.ando.la/v1/recover/password"

	payload := strings.NewReader("{ \n\"email\": \"francogoytia@gmail.com\"  \n}")

	req, _ := http.NewRequest("POST", url, payload)

	req.Header.Add("Content-Type", "application/json")

	res, _ := http.DefaultClient.Do(req)

	defer res.Body.Close()
	body, _ := ioutil.ReadAll(res.Body)

	fmt.Println(res)
	fmt.Println(string(body))

}
```

```json
{
  "email": "francogoytia@gmail.com"  
}
```

### HTTP Request

`POST https://api.ando.la/v1/recover/password`

Header | Content
--------- | -----------
Authorization | Bearer 4b73b11dc60ee75959eca2c117614e9741dfc99a
Content-type | application/json

### BODY Parameters

Parameter | Description
--------- | -----------
email | Email which password to recover.

## Signup

```shell
curl --request POST \
  --url 'https://api.ando.la/v1/signup' \
  --header 'Content-Type: application/json' \
  --data '{
"firstName": "Nahuel",
"lastName": "Candia",
"email": "a1@gmail.com",
"password": "rasengan2203",
"phone":"0111523456789",
"type": "merchant",
"PersonalID_number":39908762,
"PersonalID_type":"dni"
}'
```

```javascript
var http = require("http");

var options = {
  "method": "POST",
  "hostname": [
    "https://api.ando.la"
  ],
  "path": [
    "v1",
    "signup"
  ],
  "headers": {
    "Content-Type": "application/json"
  }
};

var req = http.request(options, function (res) {
  var chunks = [];

  res.on("data", function (chunk) {
    chunks.push(chunk);
  });

  res.on("end", function () {
    var body = Buffer.concat(chunks);
    console.log(body.toString());
  });
});

req.write(JSON.stringify({ firstName: 'Nahuel',
  lastName: 'Candia',
  email: 'a1@gmail.com',
  password: 'rasengan2203',
  phone: '0111523456789',
  type: 'merchant',
  PersonalID_number: 39908762,
  PersonalID_type: 'dni' }));
req.end();
```

```ruby
require 'uri'
require 'net/http'

url = URI("https://api.ando.la/v1/signup")

http = Net::HTTP.new(url.host, url.port)

request = Net::HTTP::Post.new(url)
request["Content-Type"] = 'application/json'
request.body = "{\n\"firstName\": \"Nahuel\",\n\"lastName\": \"Candia\",\n\"email\": \"a1@gmail.com\",\n\"password\": \"rasengan2203\", \n\"phone\":\"0111523456789\",\n\"type\": \"merchant\",\n\"PersonalID_number\":39908762,\n\"PersonalID_type\":\"dni\"\n}"

response = http.request(request)
puts response.read_body
```

```python
import requests

url = "https://api.ando.la/v1/signup"

payload = "{\n\"firstName\": \"Nahuel\",\n\"lastName\": \"Candia\",\n\"email\": \"a1@gmail.com\",\n\"password\": \"rasengan2203\", \n\"phone\":\"0111523456789\",\n\"type\": \"merchant\",\n\"PersonalID_number\":39908762,\n\"PersonalID_type\":\"dni\"\n}"
headers = {'Content-Type': 'application/json'}

response = requests.request("POST", url, data=payload, headers=headers)

print(response.text)
```

```php
<?php

$curl = curl_init();

curl_setopt_array($curl, array(
  CURLOPT_URL => "https://api.ando.la/v1/signup",
  CURLOPT_RETURNTRANSFER => true,
  CURLOPT_ENCODING => "",
  CURLOPT_MAXREDIRS => 10,
  CURLOPT_TIMEOUT => 30,
  CURLOPT_HTTP_VERSION => CURL_HTTP_VERSION_1_1,
  CURLOPT_CUSTOMREQUEST => "POST",
  CURLOPT_POSTFIELDS => "{\n\"firstName\": \"Nahuel\",\n\"lastName\": \"Candia\",\n\"email\": \"a1@gmail.com\",\n\"password\": \"rasengan2203\", \n\"phone\":\"0111523456789\",\n\"type\": \"merchant\",\n\"PersonalID_number\":39908762,\n\"PersonalID_type\":\"dni\"\n}",
  CURLOPT_HTTPHEADER => array(
    "Content-Type: application/json"
  ),
));

$response = curl_exec($curl);
$err = curl_error($curl);

curl_close($curl);

if ($err) {
  echo "cURL Error #:" . $err;
} else {
  echo $response;
}
```

```go
package main

import (
	"fmt"
	"strings"
	"net/http"
	"io/ioutil"
)

func main() {

	url := "https://api.ando.la/v1/signup"

	payload := strings.NewReader("{\n\"firstName\": \"Nahuel\",\n\"lastName\": \"Candia\",\n\"email\": \"a1@gmail.com\",\n\"password\": \"rasengan2203\", \n\"phone\":\"0111523456789\",\n\"type\": \"merchant\",\n\"PersonalID_number\":39908762,\n\"PersonalID_type\":\"dni\"\n}")

	req, _ := http.NewRequest("POST", url, payload)

	req.Header.Add("Content-Type", "application/json")

	res, _ := http.DefaultClient.Do(req)

	defer res.Body.Close()
	body, _ := ioutil.ReadAll(res.Body)

	fmt.Println(res)
	fmt.Println(string(body))

}
```

```json
{
  "firstName": "Nahuel",
  "lastName": "Candia",
  "email": "a1@gmail.com",
  "password": "rasengan2203",
  "phone":"0111523456789",
  "type": "merchant",
  "PersonalID_number":39908762,
  "PersonalID_type":"dni"
}
```

### HTTP Request

`POST https://api.ando.la/v1/signup`

Header | Content
--------- | -----------
Authorization | Bearer 4b73b11dc60ee75959eca2c117614e9741dfc99a
Content-type | application/json

### BODY Parameters

Parameter | Description
--------- | -----------
firstName | Customers' first name.
lastName | Customers' last name.
email | Customers' email.
password | Customers' password.
phone | Customers' phone.
type | Customers' type.
PersonalID_number | Customers' Personal ID Number (DNI).
PersonalID_type | Customers' personal ID type, can be `CUIT` or `DNI`.
