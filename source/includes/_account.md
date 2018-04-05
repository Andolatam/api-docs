#Account

## Get My Account
```shell
curl --request GET \
  --url 'https://api.ando.la/v1/account' \
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

url = URI("https://api.ando.la/v1/account")

http = Net::HTTP.new(url.host, url.port)

request = Net::HTTP::Get.new(url)
request["Authorization"] = 'Bearer Ec2_giC2EuDGPvXBvQ-ej4SF4bpB4rAF9PKH8XSqMmmZ4VLh062P1s1EBFYm_xP5ox9QtFXjEw9odekbuqyKop0zEHokJJsQdrK9X-fzuVEH-0IOq-c2IgxbmCB5NBDKJR1tYIN7NEob5UG5iLgcpsjsqJzbY_257moesQ0dD0Pxhg5P_SHWn-Xd_-WC5TIq4DRUNWFcft35-o2cskrw9zt_klG8PmjJXYRP83EK7las3rKwxs_EozTZ1cOnzK_-Jjppg_gUkFBgrLi6QFRdM8FhY8fdAD5fU4f0d4UUGCo'

response = http.request(request)
puts response.read_body
```

```python
import requests

url = "https://api.ando.la/v1/account"

headers = {'Authorization': 'Bearer Ec2_giC2EuDGPvXBvQ-ej4SF4bpB4rAF9PKH8XSqMmmZ4VLh062P1s1EBFYm_xP5ox9QtFXjEw9odekbuqyKop0zEHokJJsQdrK9X-fzuVEH-0IOq-c2IgxbmCB5NBDKJR1tYIN7NEob5UG5iLgcpsjsqJzbY_257moesQ0dD0Pxhg5P_SHWn-Xd_-WC5TIq4DRUNWFcft35-o2cskrw9zt_klG8PmjJXYRP83EK7las3rKwxs_EozTZ1cOnzK_-Jjppg_gUkFBgrLi6QFRdM8FhY8fdAD5fU4f0d4UUGCo'}

response = requests.request("GET", url, headers=headers)

print(response.text)
```

```php
<?php

$curl = curl_init();

curl_setopt_array($curl, array(
  CURLOPT_URL => "https://api.ando.la/v1/account",
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

	url := "https://api.ando.la/v1/account"

	req, _ := http.NewRequest("GET", url, nil)

	req.Header.Add("Authorization", "Bearer Ec2_giC2EuDGPvXBvQ-ej4SF4bpB4rAF9PKH8XSqMmmZ4VLh062P1s1EBFYm_xP5ox9QtFXjEw9odekbuqyKop0zEHokJJsQdrK9X-fzuVEH-0IOq-c2IgxbmCB5NBDKJR1tYIN7NEob5UG5iLgcpsjsqJzbY_257moesQ0dD0Pxhg5P_SHWn-Xd_-WC5TIq4DRUNWFcft35-o2cskrw9zt_klG8PmjJXYRP83EK7las3rKwxs_EozTZ1cOnzK_-Jjppg_gUkFBgrLi6QFRdM8FhY8fdAD5fU4f0d4UUGCo")

	res, _ := http.DefaultClient.Do(req)

	defer res.Body.Close()
	body, _ := ioutil.ReadAll(res.Body)

	fmt.Println(res)
	fmt.Println(string(body))

}
```
### HTTP Request

`GET https://api.ando.la/v1/user?email=you@domain.com&token=4b73b11dc60ee75959eca2c117614e9741dfc99a`

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
"email": "you@domain.com"  
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

req.write(JSON.stringify({ email: 'you@domain.com' }));
req.end();
```

```ruby
require 'uri'
require 'net/http'

url = URI("https://api.ando.la/v1/recover/password")

http = Net::HTTP.new(url.host, url.port)

request = Net::HTTP::Post.new(url)
request["Content-Type"] = 'application/json'
request.body = "{ \n\"email\": \"you@domain.com\"  \n}"

response = http.request(request)
puts response.read_body
```

```python
import requests

url = "https://api.ando.la/v1/recover/password"

payload = "{ \n\"email\": \"you@domain.com\"  \n}"
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
  CURLOPT_POSTFIELDS => "{ \n\"email\": \"you@domain.com\"  \n}",
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

	payload := strings.NewReader("{ \n\"email\": \"you@domain.com\"  \n}")

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
  "email": "you@domain.com"  
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
	"firstName": "John",
	"lastName": "Doe",
	"email": "you@domain.com",
	"password": "your-passw0rd",
	"phone":"000000000",
	"type": "merchant",
	"PersonalID_number":30000000,
	"PersonalID_type":"DNI"
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

req.write(JSON.stringify({ firstName: 'John',
  lastName: 'Doe',
  email: 'you@domain.com',
  password: 'your-passw0rd',
  phone: '000000000',
  type: 'merchant',
  PersonalID_number: 30000000,
  PersonalID_type: 'DNI' }));
req.end();
```

```ruby
require 'uri'
require 'net/http'

url = URI("https://api.ando.la/v1/signup")

http = Net::HTTP.new(url.host, url.port)

request = Net::HTTP::Post.new(url)
request["Content-Type"] = 'application/json'
request.body = "{\n\t\"firstName\": \"John\",\n\t\"lastName\": \"Doe\",\n\t\"email\": \"you@domain.com\",\n\t\"password\": \"your-passw0rd\", \n\t\"phone\":\"000000000\",\n\t\"type\": \"merchant\",\n\t\"PersonalID_number\":30000000,\n\t\"PersonalID_type\":\"DNI\"\n}"

response = http.request(request)
puts response.read_body
```

```python
import requests

url = "https://api.ando.la/v1/signup"

payload = "{\n\t\"firstName\": \"John\",\n\t\"lastName\": \"Doe\",\n\t\"email\": \"you@domain.com\",\n\t\"password\": \"your-passw0rd\", \n\t\"phone\":\"000000000\",\n\t\"type\": \"merchant\",\n\t\"PersonalID_number\":30000000,\n\t\"PersonalID_type\":\"DNI\"\n}"
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
  CURLOPT_POSTFIELDS => "{\n\t\"firstName\": \"John\",\n\t\"lastName\": \"Doe\",\n\t\"email\": \"you@domain.com\",\n\t\"password\": \"your-passw0rd\", \n\t\"phone\":\"000000000\",\n\t\"type\": \"merchant\",\n\t\"PersonalID_number\":30000000,\n\t\"PersonalID_type\":\"DNI\"\n}",
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

	payload := strings.NewReader("{\n\t\"firstName\": \"John\",\n\t\"lastName\": \"Doe\",\n\t\"email\": \"you@domain.com\",\n\t\"password\": \"your-passw0rd\", \n\t\"phone\":\"000000000\",\n\t\"type\": \"merchant\",\n\t\"PersonalID_number\":30000000,\n\t\"PersonalID_type\":\"DNI\"\n}")

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
	"firstName": "John",
	"lastName": "Doe",
	"email": "you@domain.com",
	"password": "your-passw0rd",
	"phone":"000000000",
	"type": "merchant",
	"PersonalID_number":30000000,
	"PersonalID_type":"DNI"
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