#Checking Account

##Get Checking Account

```shell
curl --request GET \
  --url 'https://api.ando.la/v1/checkingAccount/:companyID' \
  --header 'Authorization: Bearer Ec2_giC2EuDGPvXBvQ-ej4SF4bpB4rAF9PKH8XSqMmmZ4VLh062P1s1EBFYm_xP5ox9QtFXjEw9odekbuqyKop0zEHokJJsQdrK9X-fzuVEH-0IOq-c2IgxbmCB5NBDKJR1tYIN7NEob5UG5iLgcpsjsqJzbY_257moesQ0dD0Pxhg5P_SHWn-Xd_-WC5TIq4DRUNWFcft35-o2cskrw9zt_klG8PmjJXYRP83EK7las3rKwxs_EozTZ1cOnzK_-Jjppg_gUkFBgrLi6QFRdM8FhY8fdAD5fU4f0d4UUGCo'
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
    "account"
  ],
  "headers": {
    "Authorization": "Bearer Ec2_giC2EuDGPvXBvQ-ej4SF4bpB4rAF9PKH8XSqMmmZ4VLh062P1s1EBFYm_xP5ox9QtFXjEw9odekbuqyKop0zEHokJJsQdrK9X-fzuVEH-0IOq-c2IgxbmCB5NBDKJR1tYIN7NEob5UG5iLgcpsjsqJzbY_257moesQ0dD0Pxhg5P_SHWn-Xd_-WC5TIq4DRUNWFcft35-o2cskrw9zt_klG8PmjJXYRP83EK7las3rKwxs_EozTZ1cOnzK_-Jjppg_gUkFBgrLi6QFRdM8FhY8fdAD5fU4f0d4UUGCo"
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

req.end();
```

```ruby
require 'uri'
require 'net/http'

url = URI("https://api.ando.la/v1/checkingAccount/:companyID")

http = Net::HTTP.new(url.host, url.port)

request = Net::HTTP::Get.new(url)
request["Authorization"] = 'Bearer Ec2_giC2EuDGPvXBvQ-ej4SF4bpB4rAF9PKH8XSqMmmZ4VLh062P1s1EBFYm_xP5ox9QtFXjEw9odekbuqyKop0zEHokJJsQdrK9X-fzuVEH-0IOq-c2IgxbmCB5NBDKJR1tYIN7NEob5UG5iLgcpsjsqJzbY_257moesQ0dD0Pxhg5P_SHWn-Xd_-WC5TIq4DRUNWFcft35-o2cskrw9zt_klG8PmjJXYRP83EK7las3rKwxs_EozTZ1cOnzK_-Jjppg_gUkFBgrLi6QFRdM8FhY8fdAD5fU4f0d4UUGCo'

response = http.request(request)
puts response.read_body
```

```python
import requests

url = "https://api.ando.la/v1/checkingAccount/:companyID"

headers = {'Authorization': 'Bearer Ec2_giC2EuDGPvXBvQ-ej4SF4bpB4rAF9PKH8XSqMmmZ4VLh062P1s1EBFYm_xP5ox9QtFXjEw9odekbuqyKop0zEHokJJsQdrK9X-fzuVEH-0IOq-c2IgxbmCB5NBDKJR1tYIN7NEob5UG5iLgcpsjsqJzbY_257moesQ0dD0Pxhg5P_SHWn-Xd_-WC5TIq4DRUNWFcft35-o2cskrw9zt_klG8PmjJXYRP83EK7las3rKwxs_EozTZ1cOnzK_-Jjppg_gUkFBgrLi6QFRdM8FhY8fdAD5fU4f0d4UUGCo'}

response = requests.request("GET", url, headers=headers)

print(response.text)
```

```php
<?php

$curl = curl_init();

curl_setopt_array($curl, array(
  CURLOPT_URL => "https://api.ando.la/v1/checkingAccount/:companyID",
  CURLOPT_RETURNTRANSFER => true,
  CURLOPT_ENCODING => "",
  CURLOPT_MAXREDIRS => 10,
  CURLOPT_TIMEOUT => 30,
  CURLOPT_HTTP_VERSION => CURL_HTTP_VERSION_1_1,
  CURLOPT_CUSTOMREQUEST => "GET",
  CURLOPT_HTTPHEADER => array(
    "Authorization: Bearer Ec2_giC2EuDGPvXBvQ-ej4SF4bpB4rAF9PKH8XSqMmmZ4VLh062P1s1EBFYm_xP5ox9QtFXjEw9odekbuqyKop0zEHokJJsQdrK9X-fzuVEH-0IOq-c2IgxbmCB5NBDKJR1tYIN7NEob5UG5iLgcpsjsqJzbY_257moesQ0dD0Pxhg5P_SHWn-Xd_-WC5TIq4DRUNWFcft35-o2cskrw9zt_klG8PmjJXYRP83EK7las3rKwxs_EozTZ1cOnzK_-Jjppg_gUkFBgrLi6QFRdM8FhY8fdAD5fU4f0d4UUGCo"
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
	"net/http"
	"io/ioutil"
)

func main() {

	url := "https://api.ando.la/v1/checkingAccount/:companyID"

	req, _ := http.NewRequest("GET", url, nil)

	req.Header.Add("Authorization", "Bearer Ec2_giC2EuDGPvXBvQ-ej4SF4bpB4rAF9PKH8XSqMmmZ4VLh062P1s1EBFYm_xP5ox9QtFXjEw9odekbuqyKop0zEHokJJsQdrK9X-fzuVEH-0IOq-c2IgxbmCB5NBDKJR1tYIN7NEob5UG5iLgcpsjsqJzbY_257moesQ0dD0Pxhg5P_SHWn-Xd_-WC5TIq4DRUNWFcft35-o2cskrw9zt_klG8PmjJXYRP83EK7las3rKwxs_EozTZ1cOnzK_-Jjppg_gUkFBgrLi6QFRdM8FhY8fdAD5fU4f0d4UUGCo")

	res, _ := http.DefaultClient.Do(req)

	defer res.Body.Close()
	body, _ := ioutil.ReadAll(res.Body)

	fmt.Println(res)
	fmt.Println(string(body))

}
```

```json
Response Example
{
    "total": 10,
    "payment_day": "2018-04-10T23:44:11.719Z",
    "status": "ENABLED"
}
```

The users can check their account balances, using the Bearer Token given from Login. The total (account balance) given from this endpoint is needed in order to add funds to a MercadoPago account.   

### HTTP Request

`GET https://api.ando.la/v1/checkingAccount/:companyID`

Header | Content
--------- | -----------
Authorization | Bearer 4b73b11dc60ee75959eca2c117614e9741dfc99a
Content-type | application/json

### URL Parameters

Parameter | Description
--------- | -----------
Token | Your Bearer Token.

##Validate MercadoPago

```shell
curl --request POST \
  --url 'https://api.ando.la/v1/checkingAccount/:companyID/balance/mercadoPago' \
  --header 'Content-Type: application/json' \
  --data '{
    "companyID": 10,
	"total": 10
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

req.write(JSON.stringify({ companyID: 10, total: 10 }));
req.end();
```

```ruby
require 'uri'
require 'net/http'

url = URI("https://api.ando.la/v1/checkingAccount/:companyID/balance/mercadoPago")

http = Net::HTTP.new(url.host, url.port)

request = Net::HTTP::Post.new(url)
request["Content-Type"] = 'application/json'
request.body = "{ \n\"companyID\": 10, \n\"total\": 10 \n}"

response = http.request(request)
puts response.read_body
```

```python
import requests

url = "https://api.ando.la/v1/checkingAccount/:companyID/balance/mercadoPago"

payload = "{ \n\"companyID\": 10, \n\"total\": 10 \n}"
headers = {'Content-Type': 'application/json'}

response = requests.request("POST", url, data=payload, headers=headers)

print(response.text)
```


```php
<?php

$curl = curl_init();

curl_setopt_array($curl, array(
  CURLOPT_URL => "https://api.ando.la/v1/checkingAccount/:companyID/balance/mercadoPago",
  CURLOPT_RETURNTRANSFER => true,
  CURLOPT_ENCODING => "",
  CURLOPT_MAXREDIRS => 10,
  CURLOPT_TIMEOUT => 30,
  CURLOPT_HTTP_VERSION => CURL_HTTP_VERSION_1_1,
  CURLOPT_CUSTOMREQUEST => "POST",
  CURLOPT_POSTFIELDS => "{ \n\"companyID\": 10, \n\"total\": 10 \n}",
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

	url := "https://api.ando.la/v1/checkingAccount/:companyID/balance/mercadoPago"

	payload := strings.NewReader("{ \n\"companyID\": 10, \n\"total\": 10 \n}")

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
Request Example
{
    "companyID": 10,
    "total": 10
}
Response Example
{
    "link": "https://www.mercadopago.com/mla/checkout/start?pref_id=111111111"
}
```

The users can add funds to their MercadoPago accounts using the companyID and total (account balance). The 'total' parameter is given from 'Get Checking Account' endpoint.

### HTTP Request

`POST https://api.ando.la/v1/checkingAccount/:companyID/balance/mercadoPago`

Header | Content
--------- | -----------
Authorization | Bearer 4b73b11dc60ee75959eca2c117614e9741dfc99a
Content-type | application/json

### BODY Parameters

Parameter | Description
--------- | -----------
companyID | ID of the company to check.
total     | Account balance given from Get Checking Account Endpoint