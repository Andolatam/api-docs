#Authentication

##Get Token

```shell
curl --request POST \
  --url 'https://api.ando.la/v1/login'\
  --header 'Content-Type: application/json' \
  --data '{
	  "email": "you@domain.com",
	  "password": "your-passw0rd",
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
    "login"
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

req.write(JSON.stringify({ 
  email: 'you@domain.com',
  password: 'your-passw0rd'
}));

req.end();
```

```ruby
require 'uri'
require 'net/http'

url = URI("https://api.ando.la/v1/login")

http = Net::HTTP.new(url.host, url.port)

request = Net::HTTP::Post.new(url)
request.body = "{\n\t\"email\": \"you@domain.com\",\n\t\"password\": \"your-passw0rd\"\n}"

response = http.request(request)
puts response.read_body
```

```python
import requests

url = "https://api.ando.la/v1/login"

payload = "{\n\t\"email\": \"you@domain.com\",\n\t\"password\": \"your-passw0rd\"}"
headers = {'Content-Type': 'application/json'}

response = requests.request("POST", url, data=payload, headers=headers)

print(response.text)
```

```php
<?php

$curl = curl_init();

curl_setopt_array($curl, array(
  CURLOPT_URL => "https://api.ando.la/v1/login",
  CURLOPT_RETURNTRANSFER => true,
  CURLOPT_ENCODING => "",
  CURLOPT_MAXREDIRS => 10,
  CURLOPT_TIMEOUT => 30,
  CURLOPT_HTTP_VERSION => CURL_HTTP_VERSION_1_1,
  CURLOPT_CUSTOMREQUEST => "POST",
  CURLOPT_POSTFIELDS => "{\n\t\"email\": \"you@domain.com\",\n\t\"password\": \"your-passw0rd\"\n}",
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
	"net/http"
	"io/ioutil"
)

func main() {

  url := "https://api.ando.la/v1/login"
  
  payload := strings.NewReader("{\n\t\"email\": \"you@domain.com\",\n\t\"password\": \"your-passw0rd\"\n}")

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
	"email": "you@domain.com",
	"password": "your-passw0rd"
}
```

Endpoint to POST a Login Request. First ask for an access token, using your login credentials. a TOKEN will be returned and shall be included in the HEADER of all your request as Bearer. If Login was successful will return the following JSON:

`{
    "email": "useremail@gmail.com",
    "userID": 1,
    "token": "USER_TOKEN",
    "expirationToken": "DATE_TOKEN"
}`

###HTTP Request

`POST https://api.ando.la/v1/login`

Header | Content
--------- | -----------
Authorization | Bearer 4b73b11dc60ee75959eca2c117614e9741dfc99a
Content-type | application/json

Parameter | Description
--------- | -----------
email | email@domain.com
password | your-password
