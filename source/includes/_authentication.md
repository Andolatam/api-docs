#Authentication

##Get Token

```shell
curl --request POST \
  --url 'https://api.ando.la/v1/login?email=you@domain.com&password=yourp4ssw0rd'
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

url = URI("https://api.ando.la/v1/login?email=you@domain.com&password=yourp4ssw0rd")

http = Net::HTTP.new(url.host, url.port)

request = Net::HTTP::Post.new(url)

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
  CURLOPT_URL => "https://api.ando.la/v1/login?email=you@domain.com&password=yourp4ssw0rd",
  CURLOPT_RETURNTRANSFER => true,
  CURLOPT_ENCODING => "",
  CURLOPT_MAXREDIRS => 10,
  CURLOPT_TIMEOUT => 30,
  CURLOPT_HTTP_VERSION => CURL_HTTP_VERSION_1_1,
  CURLOPT_CUSTOMREQUEST => "POST",
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

	url := "https://api.ando.la/v1/login?email=you@domain.com&password=yourp4ssw0rd"

	req, _ := http.NewRequest("POST", url, nil)

	res, _ := http.DefaultClient.Do(req)

	defer res.Body.Close()
	body, _ := ioutil.ReadAll(res.Body)

	fmt.Println(res)
	fmt.Println(string(body))

}
```

First ask for an access token, using your login credentials. a TOKEN will be returned and shall be included in the HEADER of all your request as Bearer.

###HTTP Request

`POST https://api.ando.la/v1/login?email=you@domain.com&password=yourp4ssw0rd`

Parameter | Description
--------- | -----------
email | email@domain.com
password | your-password
