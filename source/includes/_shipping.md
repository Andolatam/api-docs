#Shipping

## Get Shipping History

```shell
curl --request GET \
  --url 'https://api.ando.la/v1/shipment/history?userId=306' \
  --header 'Authorization: Bearer qmYU2SwQG_-9Zr3lM8vKk8IPaBLwyM1p4fDrnNlQpaoJguwXODMgM9_cHq_dJO29d4CQT_DcxiaVfRuzKHeCFo4KnSp37oxy33ZG0q9DevEYoLbVIeABnUF4pQBMsRVovfNCWIePvUEjcK5_EkJ7HDA8pJLocugxpYVPv_Bfm8vfUIYcXy2BuXLAMeLvLyQ4lVOJKUagrnisE12AaUuSRWaMv-T0l5ikQ-tspeqxEtyyTFRqM5YzPUNTxQwNggHrn2fPivY61yYOZwgRAa7IfFUmIbQ49BcdE-LBwQrnuc4' \
  --header 'Content-Type: application/json'
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
    "shipment",
    "history"
  ],
  "headers": {
    "Content-Type": "application/json",
    "Authorization": "Bearer qmYU2SwQG_-9Zr3lM8vKk8IPaBLwyM1p4fDrnNlQpaoJguwXODMgM9_cHq_dJO29d4CQT_DcxiaVfRuzKHeCFo4KnSp37oxy33ZG0q9DevEYoLbVIeABnUF4pQBMsRVovfNCWIePvUEjcK5_EkJ7HDA8pJLocugxpYVPv_Bfm8vfUIYcXy2BuXLAMeLvLyQ4lVOJKUagrnisE12AaUuSRWaMv-T0l5ikQ-tspeqxEtyyTFRqM5YzPUNTxQwNggHrn2fPivY61yYOZwgRAa7IfFUmIbQ49BcdE-LBwQrnuc4"
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

url = URI("https://api.ando.la/v1/shipment/history?userId=306")

http = Net::HTTP.new(url.host, url.port)

request = Net::HTTP::Get.new(url)
request["Content-Type"] = 'application/json'
request["Authorization"] = 'Bearer qmYU2SwQG_-9Zr3lM8vKk8IPaBLwyM1p4fDrnNlQpaoJguwXODMgM9_cHq_dJO29d4CQT_DcxiaVfRuzKHeCFo4KnSp37oxy33ZG0q9DevEYoLbVIeABnUF4pQBMsRVovfNCWIePvUEjcK5_EkJ7HDA8pJLocugxpYVPv_Bfm8vfUIYcXy2BuXLAMeLvLyQ4lVOJKUagrnisE12AaUuSRWaMv-T0l5ikQ-tspeqxEtyyTFRqM5YzPUNTxQwNggHrn2fPivY61yYOZwgRAa7IfFUmIbQ49BcdE-LBwQrnuc4'

response = http.request(request)
puts response.read_body
```

```python
import requests

url = "https://api.ando.la/v1/shipment/history"

querystring = {"userId":"306"}

headers = {
    'Content-Type': "application/json",
    'Authorization': "Bearer qmYU2SwQG_-9Zr3lM8vKk8IPaBLwyM1p4fDrnNlQpaoJguwXODMgM9_cHq_dJO29d4CQT_DcxiaVfRuzKHeCFo4KnSp37oxy33ZG0q9DevEYoLbVIeABnUF4pQBMsRVovfNCWIePvUEjcK5_EkJ7HDA8pJLocugxpYVPv_Bfm8vfUIYcXy2BuXLAMeLvLyQ4lVOJKUagrnisE12AaUuSRWaMv-T0l5ikQ-tspeqxEtyyTFRqM5YzPUNTxQwNggHrn2fPivY61yYOZwgRAa7IfFUmIbQ49BcdE-LBwQrnuc4"
    }

response = requests.request("GET", url, headers=headers, params=querystring)

print(response.text)
```

```php
<?php

$curl = curl_init();

curl_setopt_array($curl, array(
  CURLOPT_URL => "https://api.ando.la/v1/shipment/history?userId=306",
  CURLOPT_RETURNTRANSFER => true,
  CURLOPT_ENCODING => "",
  CURLOPT_MAXREDIRS => 10,
  CURLOPT_TIMEOUT => 30,
  CURLOPT_HTTP_VERSION => CURL_HTTP_VERSION_1_1,
  CURLOPT_CUSTOMREQUEST => "GET",
  CURLOPT_HTTPHEADER => array(
    "Authorization: Bearer qmYU2SwQG_-9Zr3lM8vKk8IPaBLwyM1p4fDrnNlQpaoJguwXODMgM9_cHq_dJO29d4CQT_DcxiaVfRuzKHeCFo4KnSp37oxy33ZG0q9DevEYoLbVIeABnUF4pQBMsRVovfNCWIePvUEjcK5_EkJ7HDA8pJLocugxpYVPv_Bfm8vfUIYcXy2BuXLAMeLvLyQ4lVOJKUagrnisE12AaUuSRWaMv-T0l5ikQ-tspeqxEtyyTFRqM5YzPUNTxQwNggHrn2fPivY61yYOZwgRAa7IfFUmIbQ49BcdE-LBwQrnuc4",
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

	url := "https://api.ando.la/v1/shipment/history?userId=306"

	req, _ := http.NewRequest("GET", url, nil)

	req.Header.Add("Content-Type", "application/json")
	req.Header.Add("Authorization", "Bearer qmYU2SwQG_-9Zr3lM8vKk8IPaBLwyM1p4fDrnNlQpaoJguwXODMgM9_cHq_dJO29d4CQT_DcxiaVfRuzKHeCFo4KnSp37oxy33ZG0q9DevEYoLbVIeABnUF4pQBMsRVovfNCWIePvUEjcK5_EkJ7HDA8pJLocugxpYVPv_Bfm8vfUIYcXy2BuXLAMeLvLyQ4lVOJKUagrnisE12AaUuSRWaMv-T0l5ikQ-tspeqxEtyyTFRqM5YzPUNTxQwNggHrn2fPivY61yYOZwgRAa7IfFUmIbQ49BcdE-LBwQrnuc4")

	res, _ := http.DefaultClient.Do(req)

	defer res.Body.Close()
	body, _ := ioutil.ReadAll(res.Body)

	fmt.Println(res)
	fmt.Println(string(body))

}
```

### HTTP Request

`GET https://api.ando.la/v1/shipment/history?userId=306`

Header | Content
--------- | -----------
Authorization | Bearer 4b73b11dc60ee75959eca2c117614e9741dfc99a
Content-type | application/json

### URL Parameters

Parameter | Description
--------- | -----------
userId | User ID of the customer which shipment history will be retrieved.

## Get Shipping Quote

```shell
curl --request POST \
  --url 'https://api.ando.la/v1/shipment/quote' \
  --header 'Authorization: Bearer M1ia9-OmZ-h2orVTv_0AS2KR8wyecBnG4LUxk4YNueOch95QA0l01bhVDj7dH_ydTA8gBI-xdgTcM7TqT-72K5-owr-Obe_LoUfxjDMZeT9YAn-CMkP95pr9XjBoKCqv66kYRF-GN8nYi7mTyyEqgeAzkVWqPyeFCZb-x8K_QH5vfrqMWVpWkDOl5Ii9C0-qCWuOfp_4rCIFYjjwylU3WGfL7D9a9Qd5p8Zw33AxzHNydE3BVdaMb9UVKHiN-KgYeRNJ0zstVgplUKaepDl0bLAnbMKLCFgmB3QsG_RRQ9k' \
  --header 'Content-Type: application/json' \
  --data '{  "sender_userID":306,
	"shipTo_firstName":"Ax",
	"shipTo_lastName":"candia",
    "shipTo_email":"opcional@gmail.com",
    "shipTo_phone":"1123456789",
   "shipFrom_province":"Catamarca",
   "shipFrom_addressStreet":"Catamarca",
   "shipFrom_addressNumber":"4424",
   "shipFrom_city":"Buenos Aires",
   "shipFrom_country":"Argentina",
   "startSpecialInstructions":"tocar timbre",
   "shipTo_addressStreet":"Guemes",
   "shipTo_addressNumber":"4424",
   "shipTo_city":"Buenos Aires",
   "shipTo_province":"Baires",
   "shipTo_country":"Argentina",
   "endSpecialInstructions":"tocar timbre",
   "packageWidth":2,
   "packageLarge":2,
   "packageHeight":2,
   "packageWeight":1,
   "shippingMethod":"MOTO",
   "digitalSignature":false,
   "currency":"ARS",
   "promocode":"INFINITRM"
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
    "shipment",
    "quote"
  ],
  "headers": {
    "Content-Type": "application/json",
    "Authorization": "Bearer M1ia9-OmZ-h2orVTv_0AS2KR8wyecBnG4LUxk4YNueOch95QA0l01bhVDj7dH_ydTA8gBI-xdgTcM7TqT-72K5-owr-Obe_LoUfxjDMZeT9YAn-CMkP95pr9XjBoKCqv66kYRF-GN8nYi7mTyyEqgeAzkVWqPyeFCZb-x8K_QH5vfrqMWVpWkDOl5Ii9C0-qCWuOfp_4rCIFYjjwylU3WGfL7D9a9Qd5p8Zw33AxzHNydE3BVdaMb9UVKHiN-KgYeRNJ0zstVgplUKaepDl0bLAnbMKLCFgmB3QsG_RRQ9k"
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

req.write(JSON.stringify({ sender_userID: 306,
  shipTo_firstName: 'Ax',
  shipTo_lastName: 'candia',
  shipTo_email: 'opcional@gmail.com',
  shipTo_phone: '1123456789',
  shipFrom_province: 'Catamarca',
  shipFrom_addressStreet: 'Catamarca',
  shipFrom_addressNumber: '4424',
  shipFrom_city: 'Buenos Aires',
  shipFrom_country: 'Argentina',
  startSpecialInstructions: 'tocar timbre',
  shipTo_addressStreet: 'Guemes',
  shipTo_addressNumber: '4424',
  shipTo_city: 'Buenos Aires',
  shipTo_province: 'Baires',
  shipTo_country: 'Argentina',
  endSpecialInstructions: 'tocar timbre',
  packageWidth: 2,
  packageLarge: 2,
  packageHeight: 2,
  packageWeight: 1,
  shippingMethod: 'MOTO',
  digitalSignature: false,
  currency: 'ARS',
  promocode: 'INFINITRM' }));
req.end();
```

```ruby
require 'uri'
require 'net/http'

url = URI("https://api.ando.la/v1/shipment/quote")

http = Net::HTTP.new(url.host, url.port)

request = Net::HTTP::Post.new(url)
request["Content-Type"] = 'application/json'
request["Authorization"] = 'Bearer M1ia9-OmZ-h2orVTv_0AS2KR8wyecBnG4LUxk4YNueOch95QA0l01bhVDj7dH_ydTA8gBI-xdgTcM7TqT-72K5-owr-Obe_LoUfxjDMZeT9YAn-CMkP95pr9XjBoKCqv66kYRF-GN8nYi7mTyyEqgeAzkVWqPyeFCZb-x8K_QH5vfrqMWVpWkDOl5Ii9C0-qCWuOfp_4rCIFYjjwylU3WGfL7D9a9Qd5p8Zw33AxzHNydE3BVdaMb9UVKHiN-KgYeRNJ0zstVgplUKaepDl0bLAnbMKLCFgmB3QsG_RRQ9k'
request.body = "{  \"sender_userID\":306,\r\n\t\"shipTo_firstName\":\"Ax\",\r\n\t\"shipTo_lastName\":\"candia\",\r\n    \"shipTo_email\":\"opcional@gmail.com\", \r\n    \"shipTo_phone\":\"1123456789\",\r\n   \"shipFrom_province\":\"Catamarca\",\r\n   \"shipFrom_addressStreet\":\"Catamarca\",\r\n   \"shipFrom_addressNumber\":\"4424\", \r\n   \"shipFrom_city\":\"Buenos Aires\",\r\n   \"shipFrom_country\":\"Argentina\",\r\n   \"startSpecialInstructions\":\"tocar timbre\",\r\n   \"shipTo_addressStreet\":\"Guemes\",\r\n   \"shipTo_addressNumber\":\"4424\", \r\n   \"shipTo_city\":\"Buenos Aires\",\r\n   \"shipTo_province\":\"Baires\",\r\n   \"shipTo_country\":\"Argentina\",\r\n   \"endSpecialInstructions\":\"tocar timbre\",\r\n   \"packageWidth\":2,\r\n   \"packageLarge\":2,\r\n   \"packageHeight\":2,\r\n   \"packageWeight\":1,\r\n   \"shippingMethod\":\"MOTO\",\r\n   \"digitalSignature\":false,\r\n   \"currency\":\"ARS\",\r\n   \"promocode\":\"INFINITRM\" \r\n}"

response = http.request(request)
puts response.read_body
```

```python
import requests

url = "https://api.ando.la/v1/shipment/quote"

payload = "{  \"sender_userID\":306,\r\n\t\"shipTo_firstName\":\"Ax\",\r\n\t\"shipTo_lastName\":\"candia\",\r\n    \"shipTo_email\":\"opcional@gmail.com\", \r\n    \"shipTo_phone\":\"1123456789\",\r\n   \"shipFrom_province\":\"Catamarca\",\r\n   \"shipFrom_addressStreet\":\"Catamarca\",\r\n   \"shipFrom_addressNumber\":\"4424\", \r\n   \"shipFrom_city\":\"Buenos Aires\",\r\n   \"shipFrom_country\":\"Argentina\",\r\n   \"startSpecialInstructions\":\"tocar timbre\",\r\n   \"shipTo_addressStreet\":\"Guemes\",\r\n   \"shipTo_addressNumber\":\"4424\", \r\n   \"shipTo_city\":\"Buenos Aires\",\r\n   \"shipTo_province\":\"Baires\",\r\n   \"shipTo_country\":\"Argentina\",\r\n   \"endSpecialInstructions\":\"tocar timbre\",\r\n   \"packageWidth\":2,\r\n   \"packageLarge\":2,\r\n   \"packageHeight\":2,\r\n   \"packageWeight\":1,\r\n   \"shippingMethod\":\"MOTO\",\r\n   \"digitalSignature\":false,\r\n   \"currency\":\"ARS\",\r\n   \"promocode\":\"INFINITRM\" \r\n}"
headers = {
    'Content-Type': "application/json",
    'Authorization': "Bearer M1ia9-OmZ-h2orVTv_0AS2KR8wyecBnG4LUxk4YNueOch95QA0l01bhVDj7dH_ydTA8gBI-xdgTcM7TqT-72K5-owr-Obe_LoUfxjDMZeT9YAn-CMkP95pr9XjBoKCqv66kYRF-GN8nYi7mTyyEqgeAzkVWqPyeFCZb-x8K_QH5vfrqMWVpWkDOl5Ii9C0-qCWuOfp_4rCIFYjjwylU3WGfL7D9a9Qd5p8Zw33AxzHNydE3BVdaMb9UVKHiN-KgYeRNJ0zstVgplUKaepDl0bLAnbMKLCFgmB3QsG_RRQ9k"
    }

response = requests.request("POST", url, data=payload, headers=headers)

print(response.text)
```

```php
<?php

$curl = curl_init();

curl_setopt_array($curl, array(
  CURLOPT_URL => "https://api.ando.la/v1/shipment/quote",
  CURLOPT_RETURNTRANSFER => true,
  CURLOPT_ENCODING => "",
  CURLOPT_MAXREDIRS => 10,
  CURLOPT_TIMEOUT => 30,
  CURLOPT_HTTP_VERSION => CURL_HTTP_VERSION_1_1,
  CURLOPT_CUSTOMREQUEST => "POST",
  CURLOPT_POSTFIELDS => "{  \"sender_userID\":306,\r\n\t\"shipTo_firstName\":\"Ax\",\r\n\t\"shipTo_lastName\":\"candia\",\r\n    \"shipTo_email\":\"opcional@gmail.com\", \r\n    \"shipTo_phone\":\"1123456789\",\r\n   \"shipFrom_province\":\"Catamarca\",\r\n   \"shipFrom_addressStreet\":\"Catamarca\",\r\n   \"shipFrom_addressNumber\":\"4424\", \r\n   \"shipFrom_city\":\"Buenos Aires\",\r\n   \"shipFrom_country\":\"Argentina\",\r\n   \"startSpecialInstructions\":\"tocar timbre\",\r\n   \"shipTo_addressStreet\":\"Guemes\",\r\n   \"shipTo_addressNumber\":\"4424\", \r\n   \"shipTo_city\":\"Buenos Aires\",\r\n   \"shipTo_province\":\"Baires\",\r\n   \"shipTo_country\":\"Argentina\",\r\n   \"endSpecialInstructions\":\"tocar timbre\",\r\n   \"packageWidth\":2,\r\n   \"packageLarge\":2,\r\n   \"packageHeight\":2,\r\n   \"packageWeight\":1,\r\n   \"shippingMethod\":\"MOTO\",\r\n   \"digitalSignature\":false,\r\n   \"currency\":\"ARS\",\r\n   \"promocode\":\"INFINITRM\" \r\n}",
  CURLOPT_HTTPHEADER => array(
    "Authorization: Bearer M1ia9-OmZ-h2orVTv_0AS2KR8wyecBnG4LUxk4YNueOch95QA0l01bhVDj7dH_ydTA8gBI-xdgTcM7TqT-72K5-owr-Obe_LoUfxjDMZeT9YAn-CMkP95pr9XjBoKCqv66kYRF-GN8nYi7mTyyEqgeAzkVWqPyeFCZb-x8K_QH5vfrqMWVpWkDOl5Ii9C0-qCWuOfp_4rCIFYjjwylU3WGfL7D9a9Qd5p8Zw33AxzHNydE3BVdaMb9UVKHiN-KgYeRNJ0zstVgplUKaepDl0bLAnbMKLCFgmB3QsG_RRQ9k",
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

	url := "https://api.ando.la/v1/shipment/quote"

	payload := strings.NewReader("{  \"sender_userID\":306,\r\n\t\"shipTo_firstName\":\"Ax\",\r\n\t\"shipTo_lastName\":\"candia\",\r\n    \"shipTo_email\":\"opcional@gmail.com\", \r\n    \"shipTo_phone\":\"1123456789\",\r\n   \"shipFrom_province\":\"Catamarca\",\r\n   \"shipFrom_addressStreet\":\"Catamarca\",\r\n   \"shipFrom_addressNumber\":\"4424\", \r\n   \"shipFrom_city\":\"Buenos Aires\",\r\n   \"shipFrom_country\":\"Argentina\",\r\n   \"startSpecialInstructions\":\"tocar timbre\",\r\n   \"shipTo_addressStreet\":\"Guemes\",\r\n   \"shipTo_addressNumber\":\"4424\", \r\n   \"shipTo_city\":\"Buenos Aires\",\r\n   \"shipTo_province\":\"Baires\",\r\n   \"shipTo_country\":\"Argentina\",\r\n   \"endSpecialInstructions\":\"tocar timbre\",\r\n   \"packageWidth\":2,\r\n   \"packageLarge\":2,\r\n   \"packageHeight\":2,\r\n   \"packageWeight\":1,\r\n   \"shippingMethod\":\"MOTO\",\r\n   \"digitalSignature\":false,\r\n   \"currency\":\"ARS\",\r\n   \"promocode\":\"INFINITRM\" \r\n}")

	req, _ := http.NewRequest("POST", url, payload)

	req.Header.Add("Content-Type", "application/json")
	req.Header.Add("Authorization", "Bearer M1ia9-OmZ-h2orVTv_0AS2KR8wyecBnG4LUxk4YNueOch95QA0l01bhVDj7dH_ydTA8gBI-xdgTcM7TqT-72K5-owr-Obe_LoUfxjDMZeT9YAn-CMkP95pr9XjBoKCqv66kYRF-GN8nYi7mTyyEqgeAzkVWqPyeFCZb-x8K_QH5vfrqMWVpWkDOl5Ii9C0-qCWuOfp_4rCIFYjjwylU3WGfL7D9a9Qd5p8Zw33AxzHNydE3BVdaMb9UVKHiN-KgYeRNJ0zstVgplUKaepDl0bLAnbMKLCFgmB3QsG_RRQ9k")

	res, _ := http.DefaultClient.Do(req)

	defer res.Body.Close()
	body, _ := ioutil.ReadAll(res.Body)

	fmt.Println(res)
	fmt.Println(string(body))

}
```

```json
{  
  "sender_userID":306,
  "shipTo_firstName":"Ax",
  "shipTo_lastName":"candia",
  "shipTo_email":"opcional@gmail.com",
  "shipTo_phone":"1123456789",
  "shipFrom_province":"Catamarca",
  "shipFrom_addressStreet":"Catamarca",
  "shipFrom_addressNumber":"4424",
  "shipFrom_city":"Buenos Aires",
  "shipFrom_country":"Argentina",
  "startSpecialInstructions":"tocar timbre",
  "shipTo_addressStreet":"Guemes",
  "shipTo_addressNumber":"4424",
  "shipTo_city":"Buenos Aires",
  "shipTo_province":"Baires",
  "shipTo_country":"Argentina",
  "endSpecialInstructions":"tocar timbre",
  "packageWidth":2,
  "packageLarge":2,
  "packageHeight":2,
  "packageWeight":1,
  "shippingMethod":"MOTO",
  "digitalSignature":false,
  "currency":"ARS",
  "promocode":"INFINITRM"
}

```

The quote will return a price and QuoteID that shall be used to confirm the shipment order from the 'New Shipment' endpoint.

### HTTP Request

`POST https://api.ando.la/v1/shipment/quote`

Header | Content
--------- | -----------
Authorization | Bearer 4b73b11dc60ee75959eca2c117614e9741dfc99a
Content-type | application/json

### BODY Parameters

Parameter | Description
--------- | -----------
sender_userID | ID of the user sending the package.
shipFrom_addressStreet | Street Address of the sender of the package.
shipFrom_addressNumber | Street Number of the sender of the package.
shipFrom_city | City of the sender of the package.
shipFrom_province | Province of the sender of the package.
shipFrom_country | Country of the sender of the package.
startSpecialInstructions | Special instructions for the rider when picking up the package.
shipTo_firstName | First Name of the receiver of the package.
shipTo_lastName | Last Name of the receiver of the package.
shipTo_email | Email of the receiver of the package.
shipTo_phone | Phone number of the receiver of the package.
shipTo_addressStreet | Street Address of the receiver of the package.
shipTo_addressNumber | Street Number of the receiver of the package.
shipTo_city | City of the receiver of the package.
shipTo_province | Province of the receiver of the package.
shipTo_country | Country of the receiver of the package.
endSpecialInstructions | Special instructions for the rider when delivering the package.
packageWidth | Integer (in cm).
packageLarge | Integer (in cm).
packageHeight | Integer (in cm).
packageWeight | Integer (in grams).
shippingMethod | Shipping Method can be `MOTO` or `BICICLETA`
digitalSignature | Boolean (`true` or `false`), indicates if a digital signature is required by the receiver.
currency | Currency of the price of this shipment.
promocode | Promocode used for this shipment.

## New Shipment

```shell
curl --request POST \
  --url 'https://api.ando.la/v1/shipment/new' \
  --header 'Authorization: Bearer M1ia9-OmZ-h2orVTv_0AS2KR8wyecBnG4LUxk4YNueOch95QA0l01bhVDj7dH_ydTA8gBI-xdgTcM7TqT-72K5-owr-Obe_LoUfxjDMZeT9YAn-CMkP95pr9XjBoKCqv66kYRF-GN8nYi7mTyyEqgeAzkVWqPyeFCZb-x8K_QH5vfrqMWVpWkDOl5Ii9C0-qCWuOfp_4rCIFYjjwylU3WGfL7D9a9Qd5p8Zw33AxzHNydE3BVdaMb9UVKHiN-KgYeRNJ0zstVgplUKaepDl0bLAnbMKLCFgmB3QsG_RRQ9k' \
  --header 'Content-Type: application/json' \
  --data '{
  "quoteID":"6517"  ,
  "priceId":"8601" ,
  "payee": "receptor",  
  "discountId":"22"
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
    "shipment",
    "new"
  ],
  "headers": {
    "Content-Type": "application/json",
    "Authorization": "Bearer M1ia9-OmZ-h2orVTv_0AS2KR8wyecBnG4LUxk4YNueOch95QA0l01bhVDj7dH_ydTA8gBI-xdgTcM7TqT-72K5-owr-Obe_LoUfxjDMZeT9YAn-CMkP95pr9XjBoKCqv66kYRF-GN8nYi7mTyyEqgeAzkVWqPyeFCZb-x8K_QH5vfrqMWVpWkDOl5Ii9C0-qCWuOfp_4rCIFYjjwylU3WGfL7D9a9Qd5p8Zw33AxzHNydE3BVdaMb9UVKHiN-KgYeRNJ0zstVgplUKaepDl0bLAnbMKLCFgmB3QsG_RRQ9k"
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

req.write(JSON.stringify({ quoteID: '6517',
  priceId: '8601',
  payee: 'receptor',
  discountId: '22' }));
req.end();
```

```ruby
require 'uri'
require 'net/http'

url = URI("https://api.ando.la/v1/shipment/new")

http = Net::HTTP.new(url.host, url.port)

request = Net::HTTP::Post.new(url)
request["Content-Type"] = 'application/json'
request["Authorization"] = 'Bearer M1ia9-OmZ-h2orVTv_0AS2KR8wyecBnG4LUxk4YNueOch95QA0l01bhVDj7dH_ydTA8gBI-xdgTcM7TqT-72K5-owr-Obe_LoUfxjDMZeT9YAn-CMkP95pr9XjBoKCqv66kYRF-GN8nYi7mTyyEqgeAzkVWqPyeFCZb-x8K_QH5vfrqMWVpWkDOl5Ii9C0-qCWuOfp_4rCIFYjjwylU3WGfL7D9a9Qd5p8Zw33AxzHNydE3BVdaMb9UVKHiN-KgYeRNJ0zstVgplUKaepDl0bLAnbMKLCFgmB3QsG_RRQ9k'
request.body = "{\r\n  \"quoteID\":\"6517\"  ,\r\n  \"priceId\":\"8601\" ,\r\n  \"payee\": \"receptor\",  \r\n  \"discountId\":\"22\"\r\n}"

response = http.request(request)
puts response.read_body
```

```python
import requests

url = "https://api.ando.la/v1/shipment/new"

payload = "{\r\n  \"quoteID\":\"6517\"  ,\r\n  \"priceId\":\"8601\" ,\r\n  \"payee\": \"receptor\",  \r\n  \"discountId\":\"22\"\r\n}"
headers = {
    'Content-Type': "application/json",
    'Authorization': "Bearer M1ia9-OmZ-h2orVTv_0AS2KR8wyecBnG4LUxk4YNueOch95QA0l01bhVDj7dH_ydTA8gBI-xdgTcM7TqT-72K5-owr-Obe_LoUfxjDMZeT9YAn-CMkP95pr9XjBoKCqv66kYRF-GN8nYi7mTyyEqgeAzkVWqPyeFCZb-x8K_QH5vfrqMWVpWkDOl5Ii9C0-qCWuOfp_4rCIFYjjwylU3WGfL7D9a9Qd5p8Zw33AxzHNydE3BVdaMb9UVKHiN-KgYeRNJ0zstVgplUKaepDl0bLAnbMKLCFgmB3QsG_RRQ9k"
    }

response = requests.request("POST", url, data=payload, headers=headers)

print(response.text)
```

```php
<?php

$curl = curl_init();

curl_setopt_array($curl, array(
  CURLOPT_URL => "https://api.ando.la/v1/shipment/new",
  CURLOPT_RETURNTRANSFER => true,
  CURLOPT_ENCODING => "",
  CURLOPT_MAXREDIRS => 10,
  CURLOPT_TIMEOUT => 30,
  CURLOPT_HTTP_VERSION => CURL_HTTP_VERSION_1_1,
  CURLOPT_CUSTOMREQUEST => "POST",
  CURLOPT_POSTFIELDS => "{\r\n  \"quoteID\":\"6517\"  ,\r\n  \"priceId\":\"8601\" ,\r\n  \"payee\": \"receptor\",  \r\n  \"discountId\":\"22\"\r\n}",
  CURLOPT_HTTPHEADER => array(
    "Authorization: Bearer M1ia9-OmZ-h2orVTv_0AS2KR8wyecBnG4LUxk4YNueOch95QA0l01bhVDj7dH_ydTA8gBI-xdgTcM7TqT-72K5-owr-Obe_LoUfxjDMZeT9YAn-CMkP95pr9XjBoKCqv66kYRF-GN8nYi7mTyyEqgeAzkVWqPyeFCZb-x8K_QH5vfrqMWVpWkDOl5Ii9C0-qCWuOfp_4rCIFYjjwylU3WGfL7D9a9Qd5p8Zw33AxzHNydE3BVdaMb9UVKHiN-KgYeRNJ0zstVgplUKaepDl0bLAnbMKLCFgmB3QsG_RRQ9k",
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

	url := "https://api.ando.la/v1/shipment/new"

	payload := strings.NewReader("{\r\n  \"quoteID\":\"6517\"  ,\r\n  \"priceId\":\"8601\" ,\r\n  \"payee\": \"receptor\",  \r\n  \"discountId\":\"22\"\r\n}")

	req, _ := http.NewRequest("POST", url, payload)

	req.Header.Add("Content-Type", "application/json")
	req.Header.Add("Authorization", "Bearer M1ia9-OmZ-h2orVTv_0AS2KR8wyecBnG4LUxk4YNueOch95QA0l01bhVDj7dH_ydTA8gBI-xdgTcM7TqT-72K5-owr-Obe_LoUfxjDMZeT9YAn-CMkP95pr9XjBoKCqv66kYRF-GN8nYi7mTyyEqgeAzkVWqPyeFCZb-x8K_QH5vfrqMWVpWkDOl5Ii9C0-qCWuOfp_4rCIFYjjwylU3WGfL7D9a9Qd5p8Zw33AxzHNydE3BVdaMb9UVKHiN-KgYeRNJ0zstVgplUKaepDl0bLAnbMKLCFgmB3QsG_RRQ9k")

	res, _ := http.DefaultClient.Do(req)

	defer res.Body.Close()
	body, _ := ioutil.ReadAll(res.Body)

	fmt.Println(res)
	fmt.Println(string(body))

}
```

```json
{
  "quoteID":"6517"  ,
  "priceId":"8601" ,
  "payee": "receptor",  
  "discountId":"22"
}
```
In order to start a new shipment, a quote shall be required before.

### HTTP Request

`POST https://api.ando.la/v1/shipment/new`

Header | Content
--------- | -----------
Authorization | Bearer 4b73b11dc60ee75959eca2c117614e9741dfc99a
Content-type | application/json

### BODY Parameters

Parameter | Description
--------- | -----------
quoteID | Quote ID returned from the QUOTE Endpoint.
priceId | PriceID also returned from the QUOTE Endpoint.
payee | Who pays for the shipment. Possible values are `receptor` or `sender`.
discountId | ID of the PROMOCODE used.

## Track a Shipment

```shell
curl --request GET \
  --url 'https://api.ando.la/v1/shipment?quoteID=6559' \
  --header 'Authorization: Bearer IKd0thOh1XZEYiR6Iqslxf_bZkwZn9ofz7uyFNxs4pasTy9Wtxh-vOYZTRrsfuC4ZOiFZYdUdVwOAfBGjjRyV-St5gS8pVCbzhhVgUnTP6NcpBY7mi1cPFmRtdVStrvCTTb03Ciz3Jj13ohKWdvaf_VCvfQcQwDExBHqQa8EbnZ92cwegLGXd22w2ZiaEQ6maNdvgdEAFwmddo2Dzf4zBPxM0uWNhvg-XLWzwnFOZJZMxWk_mKNVaeTaMz9ClU9vrSg1yy834tx-97VzzEq9QMUt2LdMqv2bSxxHxZv0Qx0' \
  --header 'Content-Type: application/json'
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
    "shipment"
  ],
  "headers": {
    "Content-Type": "application/json",
    "Authorization": "Bearer IKd0thOh1XZEYiR6Iqslxf_bZkwZn9ofz7uyFNxs4pasTy9Wtxh-vOYZTRrsfuC4ZOiFZYdUdVwOAfBGjjRyV-St5gS8pVCbzhhVgUnTP6NcpBY7mi1cPFmRtdVStrvCTTb03Ciz3Jj13ohKWdvaf_VCvfQcQwDExBHqQa8EbnZ92cwegLGXd22w2ZiaEQ6maNdvgdEAFwmddo2Dzf4zBPxM0uWNhvg-XLWzwnFOZJZMxWk_mKNVaeTaMz9ClU9vrSg1yy834tx-97VzzEq9QMUt2LdMqv2bSxxHxZv0Qx0"
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

url = URI("https://api.ando.la/v1/shipment?quoteID=6559")

http = Net::HTTP.new(url.host, url.port)

request = Net::HTTP::Get.new(url)
request["Content-Type"] = 'application/json'
request["Authorization"] = 'Bearer IKd0thOh1XZEYiR6Iqslxf_bZkwZn9ofz7uyFNxs4pasTy9Wtxh-vOYZTRrsfuC4ZOiFZYdUdVwOAfBGjjRyV-St5gS8pVCbzhhVgUnTP6NcpBY7mi1cPFmRtdVStrvCTTb03Ciz3Jj13ohKWdvaf_VCvfQcQwDExBHqQa8EbnZ92cwegLGXd22w2ZiaEQ6maNdvgdEAFwmddo2Dzf4zBPxM0uWNhvg-XLWzwnFOZJZMxWk_mKNVaeTaMz9ClU9vrSg1yy834tx-97VzzEq9QMUt2LdMqv2bSxxHxZv0Qx0'

response = http.request(request)
puts response.read_body
```

```python
import requests

url = "https://api.ando.la/v1/shipment"

querystring = {"quoteID":"6559"}

headers = {
    'Content-Type': "application/json",
    'Authorization': "Bearer IKd0thOh1XZEYiR6Iqslxf_bZkwZn9ofz7uyFNxs4pasTy9Wtxh-vOYZTRrsfuC4ZOiFZYdUdVwOAfBGjjRyV-St5gS8pVCbzhhVgUnTP6NcpBY7mi1cPFmRtdVStrvCTTb03Ciz3Jj13ohKWdvaf_VCvfQcQwDExBHqQa8EbnZ92cwegLGXd22w2ZiaEQ6maNdvgdEAFwmddo2Dzf4zBPxM0uWNhvg-XLWzwnFOZJZMxWk_mKNVaeTaMz9ClU9vrSg1yy834tx-97VzzEq9QMUt2LdMqv2bSxxHxZv0Qx0"
    }

response = requests.request("GET", url, headers=headers, params=querystring)

print(response.text)
```

```php
<?php

$curl = curl_init();

curl_setopt_array($curl, array(
  CURLOPT_URL => "https://api.ando.la/v1/shipment?quoteID=6559",
  CURLOPT_RETURNTRANSFER => true,
  CURLOPT_ENCODING => "",
  CURLOPT_MAXREDIRS => 10,
  CURLOPT_TIMEOUT => 30,
  CURLOPT_HTTP_VERSION => CURL_HTTP_VERSION_1_1,
  CURLOPT_CUSTOMREQUEST => "GET",
  CURLOPT_HTTPHEADER => array(
    "Authorization: Bearer IKd0thOh1XZEYiR6Iqslxf_bZkwZn9ofz7uyFNxs4pasTy9Wtxh-vOYZTRrsfuC4ZOiFZYdUdVwOAfBGjjRyV-St5gS8pVCbzhhVgUnTP6NcpBY7mi1cPFmRtdVStrvCTTb03Ciz3Jj13ohKWdvaf_VCvfQcQwDExBHqQa8EbnZ92cwegLGXd22w2ZiaEQ6maNdvgdEAFwmddo2Dzf4zBPxM0uWNhvg-XLWzwnFOZJZMxWk_mKNVaeTaMz9ClU9vrSg1yy834tx-97VzzEq9QMUt2LdMqv2bSxxHxZv0Qx0",
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

	url := "https://api.ando.la/v1/shipment?quoteID=6559"

	req, _ := http.NewRequest("GET", url, nil)

	req.Header.Add("Content-Type", "application/json")
	req.Header.Add("Authorization", "Bearer IKd0thOh1XZEYiR6Iqslxf_bZkwZn9ofz7uyFNxs4pasTy9Wtxh-vOYZTRrsfuC4ZOiFZYdUdVwOAfBGjjRyV-St5gS8pVCbzhhVgUnTP6NcpBY7mi1cPFmRtdVStrvCTTb03Ciz3Jj13ohKWdvaf_VCvfQcQwDExBHqQa8EbnZ92cwegLGXd22w2ZiaEQ6maNdvgdEAFwmddo2Dzf4zBPxM0uWNhvg-XLWzwnFOZJZMxWk_mKNVaeTaMz9ClU9vrSg1yy834tx-97VzzEq9QMUt2LdMqv2bSxxHxZv0Qx0")

	res, _ := http.DefaultClient.Do(req)

	defer res.Body.Close()
	body, _ := ioutil.ReadAll(res.Body)

	fmt.Println(res)
	fmt.Println(string(body))

}
```

### HTTP Request

`GET https://api.ando.la/v1/shipment?trackingID=6559`

Header | Content
--------- | -----------
Authorization | Bearer 4b73b11dc60ee75959eca2c117614e9741dfc99a
Content-type | application/json

### URL Parameters

Parameter | Description
--------- | -----------
trackingID | ID returned after the shipment order is confirmed from the 'New Shipment' endpoint.

## Cancel a Shipment

```shell
curl --request POST \
  --url 'https://api.ando.la/v1/shipment/cancel' \
  --header 'Authorization: Bearer qmYU2SwQG_-9Zr3lM8vKk8IPaBLwyM1p4fDrnNlQpaoJguwXODMgM9_cHq_dJO29d4CQT_DcxiaVfRuzKHeCFo4KnSp37oxy33ZG0q9DevEYoLbVIeABnUF4pQBMsRVovfNCWIePvUEjcK5_EkJ7HDA8pJLocugxpYVPv_Bfm8vfUIYcXy2BuXLAMeLvLyQ4lVOJKUagrnisE12AaUuSRWaMv-T0l5ikQ-tspeqxEtyyTFRqM5YzPUNTxQwNggHrn2fPivY61yYOZwgRAa7IfFUmIbQ49BcdE-LBwQrnuc4' \
  --header 'Content-Type: application/json' \
  --data '{
  "trackingID":"2747"  ,
  "userID":"306"  
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
    "shipment",
    "cancel"
  ],
  "headers": {
    "Content-Type": "application/json",
    "Authorization": "Bearer qmYU2SwQG_-9Zr3lM8vKk8IPaBLwyM1p4fDrnNlQpaoJguwXODMgM9_cHq_dJO29d4CQT_DcxiaVfRuzKHeCFo4KnSp37oxy33ZG0q9DevEYoLbVIeABnUF4pQBMsRVovfNCWIePvUEjcK5_EkJ7HDA8pJLocugxpYVPv_Bfm8vfUIYcXy2BuXLAMeLvLyQ4lVOJKUagrnisE12AaUuSRWaMv-T0l5ikQ-tspeqxEtyyTFRqM5YzPUNTxQwNggHrn2fPivY61yYOZwgRAa7IfFUmIbQ49BcdE-LBwQrnuc4"
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

req.write(JSON.stringify({ trackingID: '2747', userID: '306' }));
req.end();
```

```ruby
require 'uri'
require 'net/http'

url = URI("https://api.ando.la/v1/shipment/cancel")

http = Net::HTTP.new(url.host, url.port)

request = Net::HTTP::Post.new(url)
request["Content-Type"] = 'application/json'
request["Authorization"] = 'Bearer qmYU2SwQG_-9Zr3lM8vKk8IPaBLwyM1p4fDrnNlQpaoJguwXODMgM9_cHq_dJO29d4CQT_DcxiaVfRuzKHeCFo4KnSp37oxy33ZG0q9DevEYoLbVIeABnUF4pQBMsRVovfNCWIePvUEjcK5_EkJ7HDA8pJLocugxpYVPv_Bfm8vfUIYcXy2BuXLAMeLvLyQ4lVOJKUagrnisE12AaUuSRWaMv-T0l5ikQ-tspeqxEtyyTFRqM5YzPUNTxQwNggHrn2fPivY61yYOZwgRAa7IfFUmIbQ49BcdE-LBwQrnuc4'
request.body = "{\r\n  \"trackingID\":\"2747\"  ,\r\n  \"userID\":\"306\"  \r\n}"

response = http.request(request)
puts response.read_body
```

```python
import requests

url = "https://api.ando.la/v1/shipment/cancel"

payload = "{\r\n  \"trackingID\":\"2747\"  ,\r\n  \"userID\":\"306\"  \r\n}"
headers = {
    'Content-Type': "application/json",
    'Authorization': "Bearer qmYU2SwQG_-9Zr3lM8vKk8IPaBLwyM1p4fDrnNlQpaoJguwXODMgM9_cHq_dJO29d4CQT_DcxiaVfRuzKHeCFo4KnSp37oxy33ZG0q9DevEYoLbVIeABnUF4pQBMsRVovfNCWIePvUEjcK5_EkJ7HDA8pJLocugxpYVPv_Bfm8vfUIYcXy2BuXLAMeLvLyQ4lVOJKUagrnisE12AaUuSRWaMv-T0l5ikQ-tspeqxEtyyTFRqM5YzPUNTxQwNggHrn2fPivY61yYOZwgRAa7IfFUmIbQ49BcdE-LBwQrnuc4"
    }

response = requests.request("POST", url, data=payload, headers=headers)

print(response.text)
```

```php
<?php

$curl = curl_init();

curl_setopt_array($curl, array(
  CURLOPT_URL => "https://api.ando.la/v1/shipment/cancel",
  CURLOPT_RETURNTRANSFER => true,
  CURLOPT_ENCODING => "",
  CURLOPT_MAXREDIRS => 10,
  CURLOPT_TIMEOUT => 30,
  CURLOPT_HTTP_VERSION => CURL_HTTP_VERSION_1_1,
  CURLOPT_CUSTOMREQUEST => "POST",
  CURLOPT_POSTFIELDS => "{\r\n  \"trackingID\":\"2747\"  ,\r\n  \"userID\":\"306\"  \r\n}",
  CURLOPT_HTTPHEADER => array(
    "Authorization: Bearer qmYU2SwQG_-9Zr3lM8vKk8IPaBLwyM1p4fDrnNlQpaoJguwXODMgM9_cHq_dJO29d4CQT_DcxiaVfRuzKHeCFo4KnSp37oxy33ZG0q9DevEYoLbVIeABnUF4pQBMsRVovfNCWIePvUEjcK5_EkJ7HDA8pJLocugxpYVPv_Bfm8vfUIYcXy2BuXLAMeLvLyQ4lVOJKUagrnisE12AaUuSRWaMv-T0l5ikQ-tspeqxEtyyTFRqM5YzPUNTxQwNggHrn2fPivY61yYOZwgRAa7IfFUmIbQ49BcdE-LBwQrnuc4",
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

	url := "https://api.ando.la/v1/shipment/cancel"

	payload := strings.NewReader("{\r\n  \"trackingID\":\"2747\"  ,\r\n  \"userID\":\"306\"  \r\n}")

	req, _ := http.NewRequest("POST", url, payload)

	req.Header.Add("Content-Type", "application/json")
	req.Header.Add("Authorization", "Bearer qmYU2SwQG_-9Zr3lM8vKk8IPaBLwyM1p4fDrnNlQpaoJguwXODMgM9_cHq_dJO29d4CQT_DcxiaVfRuzKHeCFo4KnSp37oxy33ZG0q9DevEYoLbVIeABnUF4pQBMsRVovfNCWIePvUEjcK5_EkJ7HDA8pJLocugxpYVPv_Bfm8vfUIYcXy2BuXLAMeLvLyQ4lVOJKUagrnisE12AaUuSRWaMv-T0l5ikQ-tspeqxEtyyTFRqM5YzPUNTxQwNggHrn2fPivY61yYOZwgRAa7IfFUmIbQ49BcdE-LBwQrnuc4")

	res, _ := http.DefaultClient.Do(req)

	defer res.Body.Close()
	body, _ := ioutil.ReadAll(res.Body)

	fmt.Println(res)
	fmt.Println(string(body))

}
```

### HTTP Request

`POST https://api.ando.la/v1/shipment/cancel`

Header | Content
--------- | -----------
Authorization | Bearer 4b73b11dc60ee75959eca2c117614e9741dfc99a
Content-type | application/json

### BODY Parameters

Parameter | Description
--------- | -----------
trackingID | `trackingID` Provided after the confirmation of the new shipment.
userID | `userID` of the sender of the package.
