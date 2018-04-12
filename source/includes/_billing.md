#Billing

## Get All Cards

```shell
curl --request GET \
  --url 'https://api.ando.la/v1/user/paymentMethods' \
  --header 'Authorization: Bearer TxuLf62rVjOrNPiGfqSkrccTkLJFHVAmafOjsZd_n8N-LgpcCe47gS-6hfN2iEcstgz_S63B3lYdbQvlD8uRYNQHEuez3dQisNp3gVlwHh27pDtCX2-d4bKnDo20_VRVO9V2PX-6xkA6YH3aSHp1SKOeQ-lYMdt-Y-NvIuRhHzrNrSZTN_qPVrEq3-hiTlgXk670chAAoeVufK8mKIYcljgAMZRPxSDZ0J0vaci8aPd0PG8N-sNPe5vq_y5DEIqVOjSHL7H4ubyzpkl2-JxIyO5B7ldDIse_jmxjWXmScmw' \
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
    "Authorization": "Bearer TxuLf62rVjOrNPiGfqSkrccTkLJFHVAmafOjsZd_n8N-LgpcCe47gS-6hfN2iEcstgz_S63B3lYdbQvlD8uRYNQHEuez3dQisNp3gVlwHh27pDtCX2-d4bKnDo20_VRVO9V2PX-6xkA6YH3aSHp1SKOeQ-lYMdt-Y-NvIuRhHzrNrSZTN_qPVrEq3-hiTlgXk670chAAoeVufK8mKIYcljgAMZRPxSDZ0J0vaci8aPd0PG8N-sNPe5vq_y5DEIqVOjSHL7H4ubyzpkl2-JxIyO5B7ldDIse_jmxjWXmScmw"
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

url = URI("https://api.ando.la/v1/user/paymentMethods")

http = Net::HTTP.new(url.host, url.port)

request = Net::HTTP::Get.new(url)
request["Content-Type"] = 'application/json'
request["Authorization"] = 'Bearer TxuLf62rVjOrNPiGfqSkrccTkLJFHVAmafOjsZd_n8N-LgpcCe47gS-6hfN2iEcstgz_S63B3lYdbQvlD8uRYNQHEuez3dQisNp3gVlwHh27pDtCX2-d4bKnDo20_VRVO9V2PX-6xkA6YH3aSHp1SKOeQ-lYMdt-Y-NvIuRhHzrNrSZTN_qPVrEq3-hiTlgXk670chAAoeVufK8mKIYcljgAMZRPxSDZ0J0vaci8aPd0PG8N-sNPe5vq_y5DEIqVOjSHL7H4ubyzpkl2-JxIyO5B7ldDIse_jmxjWXmScmw'

response = http.request(request)
puts response.read_body
```

```python
import requests

url = "https://api.ando.la/v1/user/paymentMethods"

headers = {
    'Content-Type': "application/json",
    'Authorization': "Bearer TxuLf62rVjOrNPiGfqSkrccTkLJFHVAmafOjsZd_n8N-LgpcCe47gS-6hfN2iEcstgz_S63B3lYdbQvlD8uRYNQHEuez3dQisNp3gVlwHh27pDtCX2-d4bKnDo20_VRVO9V2PX-6xkA6YH3aSHp1SKOeQ-lYMdt-Y-NvIuRhHzrNrSZTN_qPVrEq3-hiTlgXk670chAAoeVufK8mKIYcljgAMZRPxSDZ0J0vaci8aPd0PG8N-sNPe5vq_y5DEIqVOjSHL7H4ubyzpkl2-JxIyO5B7ldDIse_jmxjWXmScmw"
    }

response = requests.request("GET", url, headers=headers)

print(response.text)
```

```php
<?php

$curl = curl_init();

curl_setopt_array($curl, array(
  CURLOPT_URL => "https://api.ando.la/v1/user/paymentMethods",
  CURLOPT_RETURNTRANSFER => true,
  CURLOPT_ENCODING => "",
  CURLOPT_MAXREDIRS => 10,
  CURLOPT_TIMEOUT => 30,
  CURLOPT_HTTP_VERSION => CURL_HTTP_VERSION_1_1,
  CURLOPT_CUSTOMREQUEST => "GET",
  CURLOPT_HTTPHEADER => array(
    "Authorization: Bearer TxuLf62rVjOrNPiGfqSkrccTkLJFHVAmafOjsZd_n8N-LgpcCe47gS-6hfN2iEcstgz_S63B3lYdbQvlD8uRYNQHEuez3dQisNp3gVlwHh27pDtCX2-d4bKnDo20_VRVO9V2PX-6xkA6YH3aSHp1SKOeQ-lYMdt-Y-NvIuRhHzrNrSZTN_qPVrEq3-hiTlgXk670chAAoeVufK8mKIYcljgAMZRPxSDZ0J0vaci8aPd0PG8N-sNPe5vq_y5DEIqVOjSHL7H4ubyzpkl2-JxIyO5B7ldDIse_jmxjWXmScmw",
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

	url := "https://api.ando.la/v1/user/paymentMethods"

	req, _ := http.NewRequest("GET", url, nil)

	req.Header.Add("Content-Type", "application/json")
	req.Header.Add("Authorization", "Bearer TxuLf62rVjOrNPiGfqSkrccTkLJFHVAmafOjsZd_n8N-LgpcCe47gS-6hfN2iEcstgz_S63B3lYdbQvlD8uRYNQHEuez3dQisNp3gVlwHh27pDtCX2-d4bKnDo20_VRVO9V2PX-6xkA6YH3aSHp1SKOeQ-lYMdt-Y-NvIuRhHzrNrSZTN_qPVrEq3-hiTlgXk670chAAoeVufK8mKIYcljgAMZRPxSDZ0J0vaci8aPd0PG8N-sNPe5vq_y5DEIqVOjSHL7H4ubyzpkl2-JxIyO5B7ldDIse_jmxjWXmScmw")

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
    "status": 200,
    "message": [
        [{"An Object with information about your cards"}]
    ]
}
```

The users can get information of their credit cards. If exist, will return a JSON file with information about cards, else will return an error.

### HTTP Request

`GET https://api.ando.la/v1/user/paymentMethods`

Header | Content
--------- | -----------
Authorization | Bearer 4b73b11dc60ee75959eca2c117614e9741dfc99a
Content-type | application/json


## Add a Card

```shell
curl --request POST \
  --url 'https://api.ando.la/v1/user/paymentMethods/add' \
  --header 'Authorization: Bearer RmZkF_zqU0zSiJkZxwigcZ_68bYzr3gnXfopPZ7Lf6xZYA7cknhMcq9E4hpD9jtQ1noL9rePoMtZ0Yyod0LWSQZNayhfoU_K_kgbTahp8SsAl_yYAY2YeM4Eb7xKwV4963WFLm7JAU_eQdEmAjvK1iJrt0b9wH11K4VcINjGYO_xopL8-jLchKF3UcC5GkkzLBmUYpMPuqi60Z3SDixg-pzI_UMaR4vznre9a6tMdzdTfnaCtk3lg7qr-77cDie6fjBYIftgZXdfNH22uuJ4oCY-GCnz_1swIUKiofL6JD0' \
  --header 'Content-Type: application/json' \
  --data '{    "cardNumber": 4540000000000000,
      "securityCode": "111",
      "expiration_month":10,
      "expiration_year": 2021,  
      "cardholder":"John Doe",
      "PersonalID_type":"DNI",
      "PersonalID_number":39000000,
      "cardType":"VISA"
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
    "Authorization": "Bearer RmZkF_zqU0zSiJkZxwigcZ_68bYzr3gnXfopPZ7Lf6xZYA7cknhMcq9E4hpD9jtQ1noL9rePoMtZ0Yyod0LWSQZNayhfoU_K_kgbTahp8SsAl_yYAY2YeM4Eb7xKwV4963WFLm7JAU_eQdEmAjvK1iJrt0b9wH11K4VcINjGYO_xopL8-jLchKF3UcC5GkkzLBmUYpMPuqi60Z3SDixg-pzI_UMaR4vznre9a6tMdzdTfnaCtk3lg7qr-77cDie6fjBYIftgZXdfNH22uuJ4oCY-GCnz_1swIUKiofL6JD0"
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

req.write(JSON.stringify({ cardNumber: 4540000000000000,
  securityCode: '111',
  expiration_month: 10,
  expiration_year: 2021,
  cardholder: 'John Doe',
  PersonalID_type: 'DNI',
  PersonalID_number: 39000000,
  cardType: 'VISA' }));
req.end();
```

```ruby
require 'uri'
require 'net/http'

url = URI("https://api.ando.la/v1/user/paymentMethods/add")

http = Net::HTTP.new(url.host, url.port)

request = Net::HTTP::Post.new(url)
request["Content-Type"] = 'application/json'
request["Authorization"] = 'Bearer RmZkF_zqU0zSiJkZxwigcZ_68bYzr3gnXfopPZ7Lf6xZYA7cknhMcq9E4hpD9jtQ1noL9rePoMtZ0Yyod0LWSQZNayhfoU_K_kgbTahp8SsAl_yYAY2YeM4Eb7xKwV4963WFLm7JAU_eQdEmAjvK1iJrt0b9wH11K4VcINjGYO_xopL8-jLchKF3UcC5GkkzLBmUYpMPuqi60Z3SDixg-pzI_UMaR4vznre9a6tMdzdTfnaCtk3lg7qr-77cDie6fjBYIftgZXdfNH22uuJ4oCY-GCnz_1swIUKiofL6JD0'
request.body = "{    \"cardNumber\": 4540000000000000, \n      \"securityCode\": \"111\", \n      \"expiration_month\":10,\n      \"expiration_year\": 2021,  \n      \"cardholder\":\"John Doe\",\n      \"PersonalID_type\":\"DNI\",\n      \"PersonalID_number\":39000000,\n      \"cardType\":\"VISA\"\n}\n "

response = http.request(request)
puts response.read_body
```

```python
import requests

url = "https://api.ando.la/v1/user/paymentMethods/add"

payload = "{    \"cardNumber\": 4540000000000000, \n      \"securityCode\": \"111\", \n      \"expiration_month\":10,\n      \"expiration_year\": 2021,  \n      \"cardholder\":\"John Doe\",\n      \"PersonalID_type\":\"DNI\",\n      \"PersonalID_number\":39000000,\n      \"cardType\":\"VISA\"\n}\n "
headers = {
    'Content-Type': "application/json",
    'Authorization': "Bearer RmZkF_zqU0zSiJkZxwigcZ_68bYzr3gnXfopPZ7Lf6xZYA7cknhMcq9E4hpD9jtQ1noL9rePoMtZ0Yyod0LWSQZNayhfoU_K_kgbTahp8SsAl_yYAY2YeM4Eb7xKwV4963WFLm7JAU_eQdEmAjvK1iJrt0b9wH11K4VcINjGYO_xopL8-jLchKF3UcC5GkkzLBmUYpMPuqi60Z3SDixg-pzI_UMaR4vznre9a6tMdzdTfnaCtk3lg7qr-77cDie6fjBYIftgZXdfNH22uuJ4oCY-GCnz_1swIUKiofL6JD0"
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
  CURLOPT_POSTFIELDS => "{    \"cardNumber\": 4540000000000000, \n      \"securityCode\": \"111\", \n      \"expiration_month\":10,\n      \"expiration_year\": 2021,  \n      \"cardholder\":\"John Doe\",\n      \"PersonalID_type\":\"DNI\",\n      \"PersonalID_number\":39000000,\n      \"cardType\":\"VISA\"\n}\n ",
  CURLOPT_HTTPHEADER => array(
    "Authorization: Bearer RmZkF_zqU0zSiJkZxwigcZ_68bYzr3gnXfopPZ7Lf6xZYA7cknhMcq9E4hpD9jtQ1noL9rePoMtZ0Yyod0LWSQZNayhfoU_K_kgbTahp8SsAl_yYAY2YeM4Eb7xKwV4963WFLm7JAU_eQdEmAjvK1iJrt0b9wH11K4VcINjGYO_xopL8-jLchKF3UcC5GkkzLBmUYpMPuqi60Z3SDixg-pzI_UMaR4vznre9a6tMdzdTfnaCtk3lg7qr-77cDie6fjBYIftgZXdfNH22uuJ4oCY-GCnz_1swIUKiofL6JD0",
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

	payload := strings.NewReader("{    \"cardNumber\": 4540000000000000, \n      \"securityCode\": \"111\", \n      \"expiration_month\":10,\n      \"expiration_year\": 2021,  \n      \"cardholder\":\"John Doe\",\n      \"PersonalID_type\":\"DNI\",\n      \"PersonalID_number\":39000000,\n      \"cardType\":\"VISA\"\n}\n ")

	req, _ := http.NewRequest("POST", url, payload)

	req.Header.Add("Content-Type", "application/json")
	req.Header.Add("Authorization", "Bearer RmZkF_zqU0zSiJkZxwigcZ_68bYzr3gnXfopPZ7Lf6xZYA7cknhMcq9E4hpD9jtQ1noL9rePoMtZ0Yyod0LWSQZNayhfoU_K_kgbTahp8SsAl_yYAY2YeM4Eb7xKwV4963WFLm7JAU_eQdEmAjvK1iJrt0b9wH11K4VcINjGYO_xopL8-jLchKF3UcC5GkkzLBmUYpMPuqi60Z3SDixg-pzI_UMaR4vznre9a6tMdzdTfnaCtk3lg7qr-77cDie6fjBYIftgZXdfNH22uuJ4oCY-GCnz_1swIUKiofL6JD0")

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
  "cardNumber": 4540000000000000,
  "securityCode": "111",
  "expiration_month":10,
  "expiration_year": 2021,  
  "cardholder":"John Doe",
  "PersonalID_type":"DNI",
  "PersonalID_number":39000000,
  "cardType":"VISA"
}
```
The users can add a credit card to their accounts. If it's valid, will return a JSON file with information about user's card, else will return an error.
 

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

## Delete a Card

```shell
curl --request DELETE \
  --url 'https://api.ando.la/v1/user/paymentMethods/remove' \
  --header 'Authorization: Bearer qRtl1Tlh2659xK0YTdJc4gYTNK98tzLzLXB2sZd1giiqhGWHWwGjjQsIkkr1gZgJbnqrqt0FEf9ulVb21tLDJopeOg50lNZN0Akbn6NUQynnzSw2yL7BKhxb-qKyJNOk3Cfum3cAhQilcKJUMFTC9GS4BIjXxFQ0Nk_NvIabV7CnDHXfrWoCAxwF1eqGwmhycoMwaWUi1cWfQPc6J1EZTAMfBPeNGsqNtm7oSM98RkDXG_YJ1AozMRD04oUI1uTrCIIXRXTTcrGxFIlWAbJKlzzBTMODFQu7pFJdoegBiUg' \
  --header 'Content-Type: application/json' \
  --data '{
  "cardId":243715685
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
    "Authorization": "Bearer qRtl1Tlh2659xK0YTdJc4gYTNK98tzLzLXB2sZd1giiqhGWHWwGjjQsIkkr1gZgJbnqrqt0FEf9ulVb21tLDJopeOg50lNZN0Akbn6NUQynnzSw2yL7BKhxb-qKyJNOk3Cfum3cAhQilcKJUMFTC9GS4BIjXxFQ0Nk_NvIabV7CnDHXfrWoCAxwF1eqGwmhycoMwaWUi1cWfQPc6J1EZTAMfBPeNGsqNtm7oSM98RkDXG_YJ1AozMRD04oUI1uTrCIIXRXTTcrGxFIlWAbJKlzzBTMODFQu7pFJdoegBiUg"
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

req.write(JSON.stringify({ cardId: 243715685 }));
req.end();
```

```ruby
require 'uri'
require 'net/http'

url = URI("https://api.ando.la/v1/user/paymentMethods/remove")

http = Net::HTTP.new(url.host, url.port)

request = Net::HTTP::Delete.new(url)
request["Content-Type"] = 'application/json'
request["Authorization"] = 'Bearer qRtl1Tlh2659xK0YTdJc4gYTNK98tzLzLXB2sZd1giiqhGWHWwGjjQsIkkr1gZgJbnqrqt0FEf9ulVb21tLDJopeOg50lNZN0Akbn6NUQynnzSw2yL7BKhxb-qKyJNOk3Cfum3cAhQilcKJUMFTC9GS4BIjXxFQ0Nk_NvIabV7CnDHXfrWoCAxwF1eqGwmhycoMwaWUi1cWfQPc6J1EZTAMfBPeNGsqNtm7oSM98RkDXG_YJ1AozMRD04oUI1uTrCIIXRXTTcrGxFIlWAbJKlzzBTMODFQu7pFJdoegBiUg'
request.body = "{ \r\n  \"cardId\":243715685\r\n}"

response = http.request(request)
puts response.read_body
```

```python
import requests

url = "https://api.ando.la/v1/user/paymentMethods/remove"

payload = "{ \r\n  \"cardId\":243715685\r\n}"
headers = {
    'Content-Type': "application/json",
    'Authorization': "Bearer qRtl1Tlh2659xK0YTdJc4gYTNK98tzLzLXB2sZd1giiqhGWHWwGjjQsIkkr1gZgJbnqrqt0FEf9ulVb21tLDJopeOg50lNZN0Akbn6NUQynnzSw2yL7BKhxb-qKyJNOk3Cfum3cAhQilcKJUMFTC9GS4BIjXxFQ0Nk_NvIabV7CnDHXfrWoCAxwF1eqGwmhycoMwaWUi1cWfQPc6J1EZTAMfBPeNGsqNtm7oSM98RkDXG_YJ1AozMRD04oUI1uTrCIIXRXTTcrGxFIlWAbJKlzzBTMODFQu7pFJdoegBiUg"
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
  CURLOPT_POSTFIELDS => "{ \r\n  \"cardId\":243715685\r\n}",
  CURLOPT_HTTPHEADER => array(
    "Authorization: Bearer qRtl1Tlh2659xK0YTdJc4gYTNK98tzLzLXB2sZd1giiqhGWHWwGjjQsIkkr1gZgJbnqrqt0FEf9ulVb21tLDJopeOg50lNZN0Akbn6NUQynnzSw2yL7BKhxb-qKyJNOk3Cfum3cAhQilcKJUMFTC9GS4BIjXxFQ0Nk_NvIabV7CnDHXfrWoCAxwF1eqGwmhycoMwaWUi1cWfQPc6J1EZTAMfBPeNGsqNtm7oSM98RkDXG_YJ1AozMRD04oUI1uTrCIIXRXTTcrGxFIlWAbJKlzzBTMODFQu7pFJdoegBiUg",
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

	payload := strings.NewReader("{ \r\n  \"cardId\":243715685\r\n}")

	req, _ := http.NewRequest("DELETE", url, payload)

	req.Header.Add("Content-Type", "application/json")
	req.Header.Add("Authorization", "Bearer qRtl1Tlh2659xK0YTdJc4gYTNK98tzLzLXB2sZd1giiqhGWHWwGjjQsIkkr1gZgJbnqrqt0FEf9ulVb21tLDJopeOg50lNZN0Akbn6NUQynnzSw2yL7BKhxb-qKyJNOk3Cfum3cAhQilcKJUMFTC9GS4BIjXxFQ0Nk_NvIabV7CnDHXfrWoCAxwF1eqGwmhycoMwaWUi1cWfQPc6J1EZTAMfBPeNGsqNtm7oSM98RkDXG_YJ1AozMRD04oUI1uTrCIIXRXTTcrGxFIlWAbJKlzzBTMODFQu7pFJdoegBiUg")

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
  "cardId":12345678
}
Response Example
{
    "status": 200,
    "message": "Credit Card deleted succesfully"
}
```
The users can delete an specific Credit Card. In order to delete a card, the user needs a specific cardId parameter, which is returned by a card of 'Get All Cards' Endpoint. If exist, will return a JSON file with a success message, else will return an error.


### HTTP Request

`DELETE https://api.ando.la/v1/user/paymentMethods/remove`

Header | Content
--------- | -----------
Authorization | Bearer 4b73b11dc60ee75959eca2c117614e9741dfc99a
Content-type | application/json

### BODY Parameters

Parameter | Description
--------- | -----------
cardId | ID of the card to delete.
