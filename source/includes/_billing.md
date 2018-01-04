#Billing

## Get All Cards

```shell
curl --request GET \
  --url 'https://api.ando.la/v1/user/paymentMethods?userID=306' \
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
    "user",
    "paymentMethods"
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

url = URI("https://api.ando.la/v1/user/paymentMethods?userID=306")

http = Net::HTTP.new(url.host, url.port)

request = Net::HTTP::Get.new(url)
request["Content-Type"] = 'application/json'
request["Authorization"] = 'Bearer qmYU2SwQG_-9Zr3lM8vKk8IPaBLwyM1p4fDrnNlQpaoJguwXODMgM9_cHq_dJO29d4CQT_DcxiaVfRuzKHeCFo4KnSp37oxy33ZG0q9DevEYoLbVIeABnUF4pQBMsRVovfNCWIePvUEjcK5_EkJ7HDA8pJLocugxpYVPv_Bfm8vfUIYcXy2BuXLAMeLvLyQ4lVOJKUagrnisE12AaUuSRWaMv-T0l5ikQ-tspeqxEtyyTFRqM5YzPUNTxQwNggHrn2fPivY61yYOZwgRAa7IfFUmIbQ49BcdE-LBwQrnuc4'

response = http.request(request)
puts response.read_body
```

```python
import requests

url = "https://api.ando.la/v1/user/paymentMethods"

querystring = {"userID":"306"}

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
  CURLOPT_URL => "https://api.ando.la/v1/user/paymentMethods?userID=306",
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

	url := "https://api.ando.la/v1/user/paymentMethods?userID=306"

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

`GET https://api.ando.la/v1/user/paymentMethods?userID=306`

Header | Content
--------- | -----------
Authorization | Bearer 4b73b11dc60ee75959eca2c117614e9741dfc99a
Content-type | application/json

### URL Parameters

Parameter | Description
--------- | -----------
userID | UserID whose cards will be retrieved.


## Add a Card

```shell
curl --request POST \
  --url 'https://api.ando.la/v1/user/paymentMethods/add' \
  --header 'Authorization: Bearer kBxNJK2qPSDaq4AvArlta7I4J8Rl3cdY3Fl2CdeJ_aNFCWJS-ZZs7zUJ_5fX5JWQiaD0eOC4-fXJTZ4Li59jw7_A7IRFwIAvjkxXRl5Umwhtu_o8xY9EX5m5rj25A_GegYwKoEzqjAT2fHYr8YZtTstClAw51MSI-7VhhCejbcTLdw6w8GHGM9sbILwCfFjrx1XJ0C0YmR1wHcL6ghmRm50OGdHa3ZVlAJ7LaVdKJfq5tP5IHwMNKzJeQVBZ4Vf6PZ_HL7YPSbJ8zyO5jqf-CamfMYh8mvS-YMTRC_Un3Zk' \
  --header 'Content-Type: application/json' \
  --data '{    "cardNumber": 4540730016147846,
      "securityCode": "796",
      "expiration_month":10,
      "expiration_year": 2021,  
      "cardholder":"axel candia",
      "PersonalID_type":"DNI",
      "PersonalID_number":39908763,
      "cardType":"visa",
      "email":"nahuelcandiaasdasdasd@gmail.com"
}
 '
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
    "user",
    "paymentMethods",
    "add"
  ],
  "headers": {
    "Content-Type": "application/json",
    "Authorization": "Bearer kBxNJK2qPSDaq4AvArlta7I4J8Rl3cdY3Fl2CdeJ_aNFCWJS-ZZs7zUJ_5fX5JWQiaD0eOC4-fXJTZ4Li59jw7_A7IRFwIAvjkxXRl5Umwhtu_o8xY9EX5m5rj25A_GegYwKoEzqjAT2fHYr8YZtTstClAw51MSI-7VhhCejbcTLdw6w8GHGM9sbILwCfFjrx1XJ0C0YmR1wHcL6ghmRm50OGdHa3ZVlAJ7LaVdKJfq5tP5IHwMNKzJeQVBZ4Vf6PZ_HL7YPSbJ8zyO5jqf-CamfMYh8mvS-YMTRC_Un3Zk"
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

req.write(JSON.stringify({ cardNumber: 4540730016147846,
  securityCode: '796',
  expiration_month: 10,
  expiration_year: 2021,
  cardholder: 'axel candia',
  PersonalID_type: 'DNI',
  PersonalID_number: 39908763,
  cardType: 'visa',
  email: 'nahuelcandiaasdasdasd@gmail.com' }));
req.end();
```

```ruby
require 'uri'
require 'net/http'

url = URI("https://api.ando.la/v1/user/paymentMethods/add")

http = Net::HTTP.new(url.host, url.port)

request = Net::HTTP::Post.new(url)
request["Content-Type"] = 'application/json'
request["Authorization"] = 'Bearer kBxNJK2qPSDaq4AvArlta7I4J8Rl3cdY3Fl2CdeJ_aNFCWJS-ZZs7zUJ_5fX5JWQiaD0eOC4-fXJTZ4Li59jw7_A7IRFwIAvjkxXRl5Umwhtu_o8xY9EX5m5rj25A_GegYwKoEzqjAT2fHYr8YZtTstClAw51MSI-7VhhCejbcTLdw6w8GHGM9sbILwCfFjrx1XJ0C0YmR1wHcL6ghmRm50OGdHa3ZVlAJ7LaVdKJfq5tP5IHwMNKzJeQVBZ4Vf6PZ_HL7YPSbJ8zyO5jqf-CamfMYh8mvS-YMTRC_Un3Zk'
request.body = "{    \"cardNumber\": 4540730016147846, \n      \"securityCode\": \"796\", \n      \"expiration_month\":10,\n      \"expiration_year\": 2021,  \n      \"cardholder\":\"axel candia\",\n      \"PersonalID_type\":\"DNI\",\n      \"PersonalID_number\":39908763,\n      \"cardType\":\"visa\",\n      \"email\":\"nahuelcandiaasdasdasd@gmail.com\"\n}\n "

response = http.request(request)
puts response.read_body
```

```python
import requests

url = "https://api.ando.la/v1/user/paymentMethods/add"

payload = "{    \"cardNumber\": 4540730016147846, \n      \"securityCode\": \"796\", \n      \"expiration_month\":10,\n      \"expiration_year\": 2021,  \n      \"cardholder\":\"axel candia\",\n      \"PersonalID_type\":\"DNI\",\n      \"PersonalID_number\":39908763,\n      \"cardType\":\"visa\",\n      \"email\":\"nahuelcandiaasdasdasd@gmail.com\"\n}\n "
headers = {
    'Content-Type': "application/json",
    'Authorization': "Bearer kBxNJK2qPSDaq4AvArlta7I4J8Rl3cdY3Fl2CdeJ_aNFCWJS-ZZs7zUJ_5fX5JWQiaD0eOC4-fXJTZ4Li59jw7_A7IRFwIAvjkxXRl5Umwhtu_o8xY9EX5m5rj25A_GegYwKoEzqjAT2fHYr8YZtTstClAw51MSI-7VhhCejbcTLdw6w8GHGM9sbILwCfFjrx1XJ0C0YmR1wHcL6ghmRm50OGdHa3ZVlAJ7LaVdKJfq5tP5IHwMNKzJeQVBZ4Vf6PZ_HL7YPSbJ8zyO5jqf-CamfMYh8mvS-YMTRC_Un3Zk"
    }

response = requests.request("POST", url, data=payload, headers=headers)

print(response.text)
```

```php
<?php

$curl = curl_init();

curl_setopt_array($curl, array(
  CURLOPT_URL => "https://api.ando.la/v1/user/paymentMethods/add",
  CURLOPT_RETURNTRANSFER => true,
  CURLOPT_ENCODING => "",
  CURLOPT_MAXREDIRS => 10,
  CURLOPT_TIMEOUT => 30,
  CURLOPT_HTTP_VERSION => CURL_HTTP_VERSION_1_1,
  CURLOPT_CUSTOMREQUEST => "POST",
  CURLOPT_POSTFIELDS => "{    \"cardNumber\": 4540730016147846, \n      \"securityCode\": \"796\", \n      \"expiration_month\":10,\n      \"expiration_year\": 2021,  \n      \"cardholder\":\"axel candia\",\n      \"PersonalID_type\":\"DNI\",\n      \"PersonalID_number\":39908763,\n      \"cardType\":\"visa\",\n      \"email\":\"nahuelcandiaasdasdasd@gmail.com\"\n}\n ",
  CURLOPT_HTTPHEADER => array(
    "Authorization: Bearer kBxNJK2qPSDaq4AvArlta7I4J8Rl3cdY3Fl2CdeJ_aNFCWJS-ZZs7zUJ_5fX5JWQiaD0eOC4-fXJTZ4Li59jw7_A7IRFwIAvjkxXRl5Umwhtu_o8xY9EX5m5rj25A_GegYwKoEzqjAT2fHYr8YZtTstClAw51MSI-7VhhCejbcTLdw6w8GHGM9sbILwCfFjrx1XJ0C0YmR1wHcL6ghmRm50OGdHa3ZVlAJ7LaVdKJfq5tP5IHwMNKzJeQVBZ4Vf6PZ_HL7YPSbJ8zyO5jqf-CamfMYh8mvS-YMTRC_Un3Zk",
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

	url := "https://api.ando.la/v1/user/paymentMethods/add"

	payload := strings.NewReader("{    \"cardNumber\": 4540730016147846, \n      \"securityCode\": \"796\", \n      \"expiration_month\":10,\n      \"expiration_year\": 2021,  \n      \"cardholder\":\"axel candia\",\n      \"PersonalID_type\":\"DNI\",\n      \"PersonalID_number\":39908763,\n      \"cardType\":\"visa\",\n      \"email\":\"nahuelcandiaasdasdasd@gmail.com\"\n}\n ")

	req, _ := http.NewRequest("POST", url, payload)

	req.Header.Add("Content-Type", "application/json")
	req.Header.Add("Authorization", "Bearer kBxNJK2qPSDaq4AvArlta7I4J8Rl3cdY3Fl2CdeJ_aNFCWJS-ZZs7zUJ_5fX5JWQiaD0eOC4-fXJTZ4Li59jw7_A7IRFwIAvjkxXRl5Umwhtu_o8xY9EX5m5rj25A_GegYwKoEzqjAT2fHYr8YZtTstClAw51MSI-7VhhCejbcTLdw6w8GHGM9sbILwCfFjrx1XJ0C0YmR1wHcL6ghmRm50OGdHa3ZVlAJ7LaVdKJfq5tP5IHwMNKzJeQVBZ4Vf6PZ_HL7YPSbJ8zyO5jqf-CamfMYh8mvS-YMTRC_Un3Zk")

	res, _ := http.DefaultClient.Do(req)

	defer res.Body.Close()
	body, _ := ioutil.ReadAll(res.Body)

	fmt.Println(res)
	fmt.Println(string(body))

}
```

```json
{
  "cardNumber": 4540730016147846,
  "securityCode": "796",
  "expiration_month":10,
  "expiration_year": 2021,  
  "cardholder":"axel candia",
  "PersonalID_type":"DNI",
  "PersonalID_number":39908763,
  "cardType":"visa",
  "email":"nahuelcandiaasdasdasd@gmail.com"
}
```
### HTTP Request

`POST https://api.ando.la/v1/user/paymentMethods/add`

Header | Content
--------- | -----------
Authorization | Bearer 4b73b11dc60ee75959eca2c117614e9741dfc99a
Content-type | application/json

### BODY Parameters

Parameter | Description
--------- | -----------
cardNumber | Card number of the customer.
securityCode | CVV
expiration_month | Expiration month of the card.
expiration_year | Expiration year of the card.
cardholder | Full Name of the cardholder.
PersonalID_type | Type of Personal ID, can be `DNI`, `CUIT`, `Passport`.
PersonalID_number | Personal ID number.
cardType | Type of the card can be `VISA`, `Mastercard`, etc.
email | Email of the customer.

## Delete a Card

```shell
curl --request DELETE \
  --url 'https://api.ando.la/v1/user/paymentMethods/remove' \
  --header 'Authorization: Bearer qmYU2SwQG_-9Zr3lM8vKk8IPaBLwyM1p4fDrnNlQpaoJguwXODMgM9_cHq_dJO29d4CQT_DcxiaVfRuzKHeCFo4KnSp37oxy33ZG0q9DevEYoLbVIeABnUF4pQBMsRVovfNCWIePvUEjcK5_EkJ7HDA8pJLocugxpYVPv_Bfm8vfUIYcXy2BuXLAMeLvLyQ4lVOJKUagrnisE12AaUuSRWaMv-T0l5ikQ-tspeqxEtyyTFRqM5YzPUNTxQwNggHrn2fPivY61yYOZwgRAa7IfFUmIbQ49BcdE-LBwQrnuc4' \
  --header 'Content-Type: application/json' \
  --data '{
  "userID":306,
  "cardId":12
}'
```

```javascript
var http = require("http");

var options = {
  "method": "DELETE",
  "hostname": [
    "https://api.ando.la"
  ],
  "path": [
    "v1",
    "user",
    "paymentMethods",
    "remove"
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

req.write(JSON.stringify({ userID: 306, cardId: 12 }));
req.end();
```

```ruby
require 'uri'
require 'net/http'

url = URI("https://api.ando.la/v1/user/paymentMethods/remove")

http = Net::HTTP.new(url.host, url.port)

request = Net::HTTP::Delete.new(url)
request["Content-Type"] = 'application/json'
request["Authorization"] = 'Bearer qmYU2SwQG_-9Zr3lM8vKk8IPaBLwyM1p4fDrnNlQpaoJguwXODMgM9_cHq_dJO29d4CQT_DcxiaVfRuzKHeCFo4KnSp37oxy33ZG0q9DevEYoLbVIeABnUF4pQBMsRVovfNCWIePvUEjcK5_EkJ7HDA8pJLocugxpYVPv_Bfm8vfUIYcXy2BuXLAMeLvLyQ4lVOJKUagrnisE12AaUuSRWaMv-T0l5ikQ-tspeqxEtyyTFRqM5YzPUNTxQwNggHrn2fPivY61yYOZwgRAa7IfFUmIbQ49BcdE-LBwQrnuc4'
request.body = "{\r\n  \"userID\":306,\r\n  \"cardId\":12\r\n}"

response = http.request(request)
puts response.read_body
```

```python
import requests

url = "https://api.ando.la/v1/user/paymentMethods/remove"

payload = "{\r\n  \"userID\":306,\r\n  \"cardId\":12\r\n}"
headers = {
    'Content-Type': "application/json",
    'Authorization': "Bearer qmYU2SwQG_-9Zr3lM8vKk8IPaBLwyM1p4fDrnNlQpaoJguwXODMgM9_cHq_dJO29d4CQT_DcxiaVfRuzKHeCFo4KnSp37oxy33ZG0q9DevEYoLbVIeABnUF4pQBMsRVovfNCWIePvUEjcK5_EkJ7HDA8pJLocugxpYVPv_Bfm8vfUIYcXy2BuXLAMeLvLyQ4lVOJKUagrnisE12AaUuSRWaMv-T0l5ikQ-tspeqxEtyyTFRqM5YzPUNTxQwNggHrn2fPivY61yYOZwgRAa7IfFUmIbQ49BcdE-LBwQrnuc4"
    }

response = requests.request("DELETE", url, data=payload, headers=headers)

print(response.text)
```

```php
<?php

$curl = curl_init();

curl_setopt_array($curl, array(
  CURLOPT_URL => "https://api.ando.la/v1/user/paymentMethods/remove",
  CURLOPT_RETURNTRANSFER => true,
  CURLOPT_ENCODING => "",
  CURLOPT_MAXREDIRS => 10,
  CURLOPT_TIMEOUT => 30,
  CURLOPT_HTTP_VERSION => CURL_HTTP_VERSION_1_1,
  CURLOPT_CUSTOMREQUEST => "DELETE",
  CURLOPT_POSTFIELDS => "{\r\n  \"userID\":306,\r\n  \"cardId\":12\r\n}",
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

	url := "https://api.ando.la/v1/user/paymentMethods/remove"

	payload := strings.NewReader("{\r\n  \"userID\":306,\r\n  \"cardId\":12\r\n}")

	req, _ := http.NewRequest("DELETE", url, payload)

	req.Header.Add("Content-Type", "application/json")
	req.Header.Add("Authorization", "Bearer qmYU2SwQG_-9Zr3lM8vKk8IPaBLwyM1p4fDrnNlQpaoJguwXODMgM9_cHq_dJO29d4CQT_DcxiaVfRuzKHeCFo4KnSp37oxy33ZG0q9DevEYoLbVIeABnUF4pQBMsRVovfNCWIePvUEjcK5_EkJ7HDA8pJLocugxpYVPv_Bfm8vfUIYcXy2BuXLAMeLvLyQ4lVOJKUagrnisE12AaUuSRWaMv-T0l5ikQ-tspeqxEtyyTFRqM5YzPUNTxQwNggHrn2fPivY61yYOZwgRAa7IfFUmIbQ49BcdE-LBwQrnuc4")

	res, _ := http.DefaultClient.Do(req)

	defer res.Body.Close()
	body, _ := ioutil.ReadAll(res.Body)

	fmt.Println(res)
	fmt.Println(string(body))

}
```

```json
{
  "userID":306,
  "cardId":12
}
```
### HTTP Request

`DELETE https://api.ando.la/v1/user/paymentMethods/remove`

Header | Content
--------- | -----------
Authorization | Bearer 4b73b11dc60ee75959eca2c117614e9741dfc99a
Content-type | application/json

### BODY Parameters

Parameter | Description
--------- | -----------
userID | ID of the user which card shall be deleted.
cardId | ID of the card to delete.
