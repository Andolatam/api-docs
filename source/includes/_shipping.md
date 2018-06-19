#Shipping

## Get Shipping History

```shell
curl --request GET \
  --url 'https://api.ando.la/v1/shipment/history' \
  --header 'Authorization: Bearer D93fM7thTTVrTYmqpDMT2o5ReUxL6FeOM1hoZtOcgYaS8ds1d9qjWOoOn_mUFh7RBr5DuJG36AOLHf6Eqx5IqDcyfjcVkWHw5QO8ZflZjn8B8fbabRfiEujX7tWY-0jZnO9zhQqrMuPoTuvAaGerh_SASgQRlXI6y4LNF2Pyu8Z9iO4slihAawVM5R356C83TbDPpxqPyHhksTFQTBqELtjB8bCxDcQDkfSf4AkTpFDpFL8OTP0-OKZ9AYPoNfbUnr02dDW3SbBcFqPVLgPbkYiuUJojaO4XYGbSY7QwUa4' \
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
    "Authorization": "Bearer D93fM7thTTVrTYmqpDMT2o5ReUxL6FeOM1hoZtOcgYaS8ds1d9qjWOoOn_mUFh7RBr5DuJG36AOLHf6Eqx5IqDcyfjcVkWHw5QO8ZflZjn8B8fbabRfiEujX7tWY-0jZnO9zhQqrMuPoTuvAaGerh_SASgQRlXI6y4LNF2Pyu8Z9iO4slihAawVM5R356C83TbDPpxqPyHhksTFQTBqELtjB8bCxDcQDkfSf4AkTpFDpFL8OTP0-OKZ9AYPoNfbUnr02dDW3SbBcFqPVLgPbkYiuUJojaO4XYGbSY7QwUa4"
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

url = URI("https://api.ando.la/v1/shipment/history")

http = Net::HTTP.new(url.host, url.port)

request = Net::HTTP::Get.new(url)
request["Content-Type"] = 'application/json'
request["Authorization"] = 'Bearer D93fM7thTTVrTYmqpDMT2o5ReUxL6FeOM1hoZtOcgYaS8ds1d9qjWOoOn_mUFh7RBr5DuJG36AOLHf6Eqx5IqDcyfjcVkWHw5QO8ZflZjn8B8fbabRfiEujX7tWY-0jZnO9zhQqrMuPoTuvAaGerh_SASgQRlXI6y4LNF2Pyu8Z9iO4slihAawVM5R356C83TbDPpxqPyHhksTFQTBqELtjB8bCxDcQDkfSf4AkTpFDpFL8OTP0-OKZ9AYPoNfbUnr02dDW3SbBcFqPVLgPbkYiuUJojaO4XYGbSY7QwUa4'

response = http.request(request)
puts response.read_body
```

```python
import requests

url = "https://api.ando.la/v1/shipment/history"

headers = {
    'Content-Type': "application/json",
    'Authorization': "Bearer D93fM7thTTVrTYmqpDMT2o5ReUxL6FeOM1hoZtOcgYaS8ds1d9qjWOoOn_mUFh7RBr5DuJG36AOLHf6Eqx5IqDcyfjcVkWHw5QO8ZflZjn8B8fbabRfiEujX7tWY-0jZnO9zhQqrMuPoTuvAaGerh_SASgQRlXI6y4LNF2Pyu8Z9iO4slihAawVM5R356C83TbDPpxqPyHhksTFQTBqELtjB8bCxDcQDkfSf4AkTpFDpFL8OTP0-OKZ9AYPoNfbUnr02dDW3SbBcFqPVLgPbkYiuUJojaO4XYGbSY7QwUa4"
    }

response = requests.request("GET", url, headers=headers)

print(response.text)
```

```php
<?php

$curl = curl_init();

curl_setopt_array($curl, array(
  CURLOPT_URL => "https://api.ando.la/v1/shipment/history",
  CURLOPT_RETURNTRANSFER => true,
  CURLOPT_ENCODING => "",
  CURLOPT_MAXREDIRS => 10,
  CURLOPT_TIMEOUT => 30,
  CURLOPT_HTTP_VERSION => CURL_HTTP_VERSION_1_1,
  CURLOPT_CUSTOMREQUEST => "GET",
  CURLOPT_HTTPHEADER => array(
    "Authorization: Bearer D93fM7thTTVrTYmqpDMT2o5ReUxL6FeOM1hoZtOcgYaS8ds1d9qjWOoOn_mUFh7RBr5DuJG36AOLHf6Eqx5IqDcyfjcVkWHw5QO8ZflZjn8B8fbabRfiEujX7tWY-0jZnO9zhQqrMuPoTuvAaGerh_SASgQRlXI6y4LNF2Pyu8Z9iO4slihAawVM5R356C83TbDPpxqPyHhksTFQTBqELtjB8bCxDcQDkfSf4AkTpFDpFL8OTP0-OKZ9AYPoNfbUnr02dDW3SbBcFqPVLgPbkYiuUJojaO4XYGbSY7QwUa4",
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

	url := "https://api.ando.la/v1/shipment/history"

	req, _ := http.NewRequest("GET", url, nil)

	req.Header.Add("Content-Type", "application/json")
	req.Header.Add("Authorization", "Bearer D93fM7thTTVrTYmqpDMT2o5ReUxL6FeOM1hoZtOcgYaS8ds1d9qjWOoOn_mUFh7RBr5DuJG36AOLHf6Eqx5IqDcyfjcVkWHw5QO8ZflZjn8B8fbabRfiEujX7tWY-0jZnO9zhQqrMuPoTuvAaGerh_SASgQRlXI6y4LNF2Pyu8Z9iO4slihAawVM5R356C83TbDPpxqPyHhksTFQTBqELtjB8bCxDcQDkfSf4AkTpFDpFL8OTP0-OKZ9AYPoNfbUnr02dDW3SbBcFqPVLgPbkYiuUJojaO4XYGbSY7QwUa4")

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
  "trackingID":12345,
    "externalReference":12345,
    "shipFrom": {
      "email":"user@email.com",
      "name":"name",
      "surname":"surname", 
      "userID":1,
      "phone":"phone",
      "address":"address",   
      "calification":5,
      "identificationNumber":12345678, 
      "profilePicture":"profile_picture_url",
      "companyId":123456,
      "company":"company_name",
      "address":"company_address",
      "instructions":"instructions" 
    },
    "shipTo": {
      "email":"email@email.com",
      "name":"name",
      "surname":"surname", 
      "userID":"userID",
      "phone":"phone",
      "address":"address",   
      "calification":5,
      "identificationNumber":12345678, 
      "profilePicture":"profile_picture_url",
      "companyId":123456,
      "company":"company_name",
      "address":"company_address",
      "instructions":"instructions"  
    }, 
    "carrier":{ 
      "transport":"bike", 
      "name":"transportist_name",
      "surname":"transportist_surname",
      "phone": "transportist_phone",
      "email": "tranportist_email",
      "profilePicture":"profile_picture_url",
      "status":"sent",
      "startDate":"startDate", 
      "packageType":"packageType",  
      "paid":true, 
      "price":10000,
      "encripted": "sign",  
      "delivered_ToCarrier":true,  
      "cancelled": false
}
```
The users can get useful information to view the tracking and current status of their shipments. In order to begin a new shipment history a Bearer Token is needed from Login endpoint. 

### HTTP Request

`GET https://api.ando.la/v1/shipment/history`

Header | Content
--------- | -----------
Authorization | Bearer 4b73b11dc60ee75959eca2c117614e9741dfc99a
Content-type | application/json

## Get Shipping Quote

```shell
curl --request POST \
  --url 'https://api.ando.la/v1/shipment/quote' \
  --header 'Authorization: Bearer TxuLf62rVjOrNPiGfqSkrccTkLJFHVAmafOjsZd_n8N-LgpcCe47gS-6hfN2iEcstgz_S63B3lYdbQvlD8uRYNQHEuez3dQisNp3gVlwHh27pDtCX2-d4bKnDo20_VRVO9V2PX-6xkA6YH3aSHp1SKOeQ-lYMdt-Y-NvIuRhHzrNrSZTN_qPVrEq3-hiTlgXk670chAAoeVufK8mKIYcljgAMZRPxSDZ0J0vaci8aPd0PG8N-sNPe5vq_y5DEIqVOjSHL7H4ubyzpkl2-JxIyO5B7ldDIse_jmxjWXmScmw' \
  --header 'Content-Type: application/json' \
  --data '{  
	"shipFrom_province":"Buenos Aires",
	"shipFrom_addressStreet":"El Salvador",
	"shipFrom_addressNumber":"5218",
	"shipFrom_city":"Buenos Aires",
	"shipFrom_country":"Argentina",
	"shipTo_firstName":"Name",
	"shipTo_lastName":"LastName",
	"shipTo_phone":"000000000",
	"shipTo_addressStreet":"Guemes",
	"shipTo_addressNumber":"4424",
	"shipTo_city":"Buenos Aires",
	"shipTo_country":"Argentina",
	"shipTo_instructions":"Something.",
	"packageWidth":2,
	"packageLarge":2,
	"packageHeight":2,
	"packageWeight":1
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

req.write(JSON.stringify({ shipFrom_province: 'Buenos Aires',
  shipFrom_addressStreet: 'El Salvador',
  shipFrom_addressNumber: '5218',
  shipFrom_city: 'Buenos Aires',
  shipFrom_country: 'Argentina',
  shipTo_firstName: 'Name',
  shipTo_lastName: 'LastName',
  shipTo_phone: '000000000',
  shipTo_addressStreet: 'Guemes',
  shipTo_addressNumber: '4424',
  shipTo_city: 'Buenos Aires',
  shipTo_country: 'Argentina',
  shipTo_instructions: 'Something.',
  packageWidth: 2,
  packageLarge: 2,
  packageHeight: 2,
  packageWeight: 1
 }));
req.end();
```

```ruby
require 'uri'
require 'net/http'

url = URI("https://api.ando.la/v1/shipment/quote")

http = Net::HTTP.new(url.host, url.port)

request = Net::HTTP::Post.new(url)
request["Content-Type"] = 'application/json'
request["Authorization"] = 'Bearer TxuLf62rVjOrNPiGfqSkrccTkLJFHVAmafOjsZd_n8N-LgpcCe47gS-6hfN2iEcstgz_S63B3lYdbQvlD8uRYNQHEuez3dQisNp3gVlwHh27pDtCX2-d4bKnDo20_VRVO9V2PX-6xkA6YH3aSHp1SKOeQ-lYMdt-Y-NvIuRhHzrNrSZTN_qPVrEq3-hiTlgXk670chAAoeVufK8mKIYcljgAMZRPxSDZ0J0vaci8aPd0PG8N-sNPe5vq_y5DEIqVOjSHL7H4ubyzpkl2-JxIyO5B7ldDIse_jmxjWXmScmw'
request.body = "{  \r\n\t\"shipFrom_province\":\"Buenos Aires\",\r\n\t\"shipFrom_addressStreet\":\"El Salvador\",\r\n\t\"shipFrom_addressNumber\":\"5218\", \r\n\t\"shipFrom_city\":\"Buenos Aires\",\r\n\t\"shipFrom_country\":\"Argentina\",\r\n\t\"shipTo_firstName\":\"Name\",\r\n\t\"shipTo_lastName\":\"LastName\",\r\n\t\"shipTo_phone\":\"000000000\",\r\n\t\"shipTo_addressStreet\":\"Guemes\",\r\n\t\"shipTo_addressNumber\":\"4424\", \r\n\t\"shipTo_city\":\"Buenos Aires\",\r\n\t\"shipTo_country\":\"Argentina\",\r\n\t\"shipTo_instructions\":\"Something.\",\r\n\t\"packageWidth\":2,\r\n\t\"packageLarge\":2,\r\n\t\"packageHeight\":2,\r\n\t\"packageWeight\":1}"

response = http.request(request)
puts response.read_body
```

```python
import requests

url = "https://api.ando.la/v1/shipment/quote"

payload = "{  \r\n\t\"shipFrom_province\":\"Buenos Aires\",\r\n\t\"shipFrom_addressStreet\":\"El Salvador\",\r\n\t\"shipFrom_addressNumber\":\"5218\", \r\n\t\"shipFrom_city\":\"Buenos Aires\",\r\n\t\"shipFrom_country\":\"Argentina\",\r\n\t\"shipTo_firstName\":\"Name\",\r\n\t\"shipTo_lastName\":\"LastName\",\r\n\t\"shipTo_phone\":\"000000000\",\r\n\t\"shipTo_addressStreet\":\"Guemes\",\r\n\t\"shipTo_addressNumber\":\"4424\", \r\n\t\"shipTo_city\":\"Buenos Aires\",\r\n\t\"shipTo_country\":\"Argentina\",\r\n\t\"shipTo_instructions\":\"Something.\",\r\n\t\"packageWidth\":2,\r\n\t\"packageLarge\":2,\r\n\t\"packageHeight\":2,\r\n\t\"packageWeight\":1}"
headers = {
    'Content-Type': "application/json",
    'Authorization': "Bearer TxuLf62rVjOrNPiGfqSkrccTkLJFHVAmafOjsZd_n8N-LgpcCe47gS-6hfN2iEcstgz_S63B3lYdbQvlD8uRYNQHEuez3dQisNp3gVlwHh27pDtCX2-d4bKnDo20_VRVO9V2PX-6xkA6YH3aSHp1SKOeQ-lYMdt-Y-NvIuRhHzrNrSZTN_qPVrEq3-hiTlgXk670chAAoeVufK8mKIYcljgAMZRPxSDZ0J0vaci8aPd0PG8N-sNPe5vq_y5DEIqVOjSHL7H4ubyzpkl2-JxIyO5B7ldDIse_jmxjWXmScmw"
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
  CURLOPT_POSTFIELDS => "{  \r\n\t\"shipFrom_province\":\"Buenos Aires\",\r\n\t\"shipFrom_addressStreet\":\"El Salvador\",\r\n\t\"shipFrom_addressNumber\":\"5218\", \r\n\t\"shipFrom_city\":\"Buenos Aires\",\r\n\t\"shipFrom_country\":\"Argentina\",\r\n\t\"shipTo_firstName\":\"Name\",\r\n\t\"shipTo_lastName\":\"LastName\",\r\n\t\"shipTo_phone\":\"000000000\",\r\n\t\"shipTo_addressStreet\":\"Guemes\",\r\n\t\"shipTo_addressNumber\":\"4424\", \r\n\t\"shipTo_city\":\"Buenos Aires\",\r\n\t\"shipTo_country\":\"Argentina\",\r\n\t\"shipTo_instructions\":\"Something.\",\r\n\t\"packageWidth\":2,\r\n\t\"packageLarge\":2,\r\n\t\"packageHeight\":2,\r\n\t\"packageWeight\":1}",
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
	"strings"
	"net/http"
	"io/ioutil"
)

func main() {

	url := "https://api.ando.la/v1/shipment/quote"

	payload := strings.NewReader("{  \r\n\t\"shipFrom_province\":\"Buenos Aires\",\r\n\t\"shipFrom_addressStreet\":\"El Salvador\",\r\n\t\"shipFrom_addressNumber\":\"5218\", \r\n\t\"shipFrom_city\":\"Buenos Aires\",\r\n\t\"shipFrom_country\":\"Argentina\",\r\n\t\"shipTo_firstName\":\"Name\",\r\n\t\"shipTo_lastName\":\"LastName\", \r\n\t\"shipTo_phone\":\"000000000\",\r\n\t\"shipTo_addressStreet\":\"Guemes\",\r\n\t\"shipTo_addressNumber\":\"4424\", \r\n\t\"shipTo_city\":\"Buenos Aires\",\r\n\t\"shipTo_country\":\"Argentina\",\r\n\t\"shipTo_instructions\":\"Something.\",\r\n\t\"packageWidth\":2,\r\n\t\"packageLarge\":2,\r\n\t\"packageHeight\":2,\r\n\t\"packageWeight\":1}")

	req, _ := http.NewRequest("POST", url, payload)

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
Request Example
{
	"shipFrom_province":"Buenos Aires",
	"shipFrom_addressStreet":"El Salvador",
	"shipFrom_addressNumber":"5218",
	"shipFrom_city":"Buenos Aires",
	"shipFrom_country":"Argentina",
	"shipTo_firstName":"Name",
	"shipTo_lastName":"LastName",
	"shipTo_phone":"000000000",
	"shipTo_addressStreet":"Guemes",
	"shipTo_addressNumber":"4424",
	"shipTo_city":"Buenos Aires",
	"shipTo_country":"Argentina",
	"shipTo_instructions":"Something.",
	"packageWidth":2,
	"packageLarge":2,
	"packageHeight":2,
	"packageWeight":1
}
Response Example
{
  "quoteID": 221434,
  "price":{
    "priceId":1234,
    "transportType":"BICICLETA",
    "waitingTime":"10 mins",
    "estimatedPrice":12.50,
    "estimatedDistance":"12 km",
    "estimatedTimeToOrigin":"1 min"
  }
}
```

The users can quote their shipments. The quote will return a price and QuoteID that shall be used to confirm the shipment order from the 'New Shipment' endpoint. 

### HTTP Request

`POST https://api.ando.la/v1/shipment/quote`

Header | Content
--------- | -----------
Authorization | Bearer 4b73b11dc60ee75959eca2c117614e9741dfc99a
Content-type | application/json

### BODY Parameters

Parameter | Description
--------- | -----------
shipFrom_addressStreet | Street Address of the sender of the package.
shipFrom_addressNumber | Street Number of the sender of the package.
shipFrom_city | City of the sender of the package.
shipFrom_province | Province of the sender of the package.
shipFrom_country | Country of the sender of the package.
shipTo_firstName | First Name of the receiver of the package.
shipTo_lastName | Last Name of the receiver of the package.
shipTo_email (optional) | Email of the receiver of the package.
shipTo_phone | Phone number of the receiver of the package.
shipTo_addressStreet | Street Address of the receiver of the package.
shipTo_addressNumber | Street Number of the receiver of the package.
shipTo_city | City of the receiver of the package.
shipTo_province (optional) | Province of the receiver of the package.
shipTo_country | Country of the receiver of the package.
shipTo_instructions | Special instructions for the rider when delivering the package.
packageWidth | Integer (in cm).
packageLarge | Integer (in cm).
packageHeight | Integer (in cm).
packageWeight | Integer (in grams).
sender_email (optional) | Email of the receiver of the package.
shippingMethod (optional) | Shipping Method can be `MOTO` or `BICICLETA`
digitalSignature (optional) | Boolean (`true` or `false`), indicates if a digital signature is required by the receiver.
currency (optional) | Currency of the price of this shipment.

## New Shipment

```shell
curl --request POST \
  --url 'https://api.ando.la/v1/shipment/new' \
  --header 'Authorization: Bearer TxuLf62rVjOrNPiGfqSkrccTkLJFHVAmafOjsZd_n8N-LgpcCe47gS-6hfN2iEcstgz_S63B3lYdbQvlD8uRYNQHEuez3dQisNp3gVlwHh27pDtCX2-d4bKnDo20_VRVO9V2PX-6xkA6YH3aSHp1SKOeQ-lYMdt-Y-NvIuRhHzrNrSZTN_qPVrEq3-hiTlgXk670chAAoeVufK8mKIYcljgAMZRPxSDZ0J0vaci8aPd0PG8N-sNPe5vq_y5DEIqVOjSHL7H4ubyzpkl2-JxIyO5B7ldDIse_jmxjWXmScmw' \
  --header 'Content-Type: application/json' \
  --data '{
  "quoteID":"6757"  ,
  "priceId":"6757",
  "paymentMethod": "credit_card",
  "promocode": "CODE888"
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

req.write(JSON.stringify({ quoteID: '6757', priceId:"6757", paymentMethod: "credit_card", promocode: "CODE888" }));
req.end();
```

```ruby
require 'uri'
require 'net/http'

url = URI("https://api.ando.la/v1/shipment/new")

http = Net::HTTP.new(url.host, url.port)

request = Net::HTTP::Post.new(url)
request["Content-Type"] = 'application/json'
request["Authorization"] = 'Bearer TxuLf62rVjOrNPiGfqSkrccTkLJFHVAmafOjsZd_n8N-LgpcCe47gS-6hfN2iEcstgz_S63B3lYdbQvlD8uRYNQHEuez3dQisNp3gVlwHh27pDtCX2-d4bKnDo20_VRVO9V2PX-6xkA6YH3aSHp1SKOeQ-lYMdt-Y-NvIuRhHzrNrSZTN_qPVrEq3-hiTlgXk670chAAoeVufK8mKIYcljgAMZRPxSDZ0J0vaci8aPd0PG8N-sNPe5vq_y5DEIqVOjSHL7H4ubyzpkl2-JxIyO5B7ldDIse_jmxjWXmScmw'
request.body = "{\r\n  \"quoteID\":\"6757\", \r\n  \"priceId\":\"6757\", \r\n  \"paymentMethod\":\"credit_card\" \r\n, \r\n  \"promocode\":\"CODE888\" \r\n}"

response = http.request(request)
puts response.read_body
```

```python
import requests

url = "https://api.ando.la/v1/shipment/new"

payload = "{\r\n  \"quoteID\":\"6757\"  , \r\n  \"priceId\":\"6757\", \r\n  \"paymentMethod\":\"credit_card\" \r\n, \r\n  \"promocode\":\"CODE888\" \r\n}"
headers = {
    'Content-Type': "application/json",
    'Authorization': "Bearer TxuLf62rVjOrNPiGfqSkrccTkLJFHVAmafOjsZd_n8N-LgpcCe47gS-6hfN2iEcstgz_S63B3lYdbQvlD8uRYNQHEuez3dQisNp3gVlwHh27pDtCX2-d4bKnDo20_VRVO9V2PX-6xkA6YH3aSHp1SKOeQ-lYMdt-Y-NvIuRhHzrNrSZTN_qPVrEq3-hiTlgXk670chAAoeVufK8mKIYcljgAMZRPxSDZ0J0vaci8aPd0PG8N-sNPe5vq_y5DEIqVOjSHL7H4ubyzpkl2-JxIyO5B7ldDIse_jmxjWXmScmw"
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
  CURLOPT_POSTFIELDS => "{ \"quoteID\":\"6757\"  , \r\n  \"priceId\":\"6757\", \r\n  \"paymentMethod\":\"credit_card\" \r\n, \r\n  \"promocode\":\"CODE888\" \r\n}",
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
	"strings"
	"net/http"
	"io/ioutil"
)

func main() {

	url := "https://api.ando.la/v1/shipment/new"

	payload := strings.NewReader("{\r\n  \"quoteID\":\"6757\"  , \r\n  \"priceId\":\"6757\", \r\n  \"paymentMethod\":\"credit_card\" \r\n, \r\n  \"promocode\":\"CODE888\" \r\n }")

	req, _ := http.NewRequest("POST", url, payload)

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
Request Example
{
  "quoteID":"6757"  ,
  "priceId":"6757",
  "paymentMethod": "credit_card",
  "promocode": "CODE888"
}
Response Example 
{
    "trackingID": "11111"
}
```
The users can request a new shipment. In order to start a new shipment, a quote shall be required before. 

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
priceId | Price Id returned from the QUOTE Endpoint.
paymentMethod | Payment Method used by the customer (checking_account* or credit_card)
promoCode (optional) | Promotional code given to the user


*ONLY E-COMMERCES
## Track a Shipment

```shell
curl --request GET \
  --url 'https://api.ando.la/v1/shipment?trackingID=6769' \
  --header 'Authorization: Bearer qRtl1Tlh2659xK0YTdJc4gYTNK98tzLzLXB2sZd1giiqhGWHWwGjjQsIkkr1gZgJbnqrqt0FEf9ulVb21tLDJopeOg50lNZN0Akbn6NUQynnzSw2yL7BKhxb-qKyJNOk3Cfum3cAhQilcKJUMFTC9GS4BIjXxFQ0Nk_NvIabV7CnDHXfrWoCAxwF1eqGwmhycoMwaWUi1cWfQPc6J1EZTAMfBPeNGsqNtm7oSM98RkDXG_YJ1AozMRD04oUI1uTrCIIXRXTTcrGxFIlWAbJKlzzBTMODFQu7pFJdoegBiUg' \
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

req.end();
```

```ruby
require 'uri'
require 'net/http'

url = URI("https://api.ando.la/v1/shipment?trackingID=6769")

http = Net::HTTP.new(url.host, url.port)

request = Net::HTTP::Get.new(url)
request["Content-Type"] = 'application/json'
request["Authorization"] = 'Bearer qRtl1Tlh2659xK0YTdJc4gYTNK98tzLzLXB2sZd1giiqhGWHWwGjjQsIkkr1gZgJbnqrqt0FEf9ulVb21tLDJopeOg50lNZN0Akbn6NUQynnzSw2yL7BKhxb-qKyJNOk3Cfum3cAhQilcKJUMFTC9GS4BIjXxFQ0Nk_NvIabV7CnDHXfrWoCAxwF1eqGwmhycoMwaWUi1cWfQPc6J1EZTAMfBPeNGsqNtm7oSM98RkDXG_YJ1AozMRD04oUI1uTrCIIXRXTTcrGxFIlWAbJKlzzBTMODFQu7pFJdoegBiUg'

response = http.request(request)
puts response.read_body
```

```python
import requests

url = "https://api.ando.la/v1/shipment"

querystring = {"trackingID":"6769"}

headers = {
    'Content-Type': "application/json",
    'Authorization': "Bearer qRtl1Tlh2659xK0YTdJc4gYTNK98tzLzLXB2sZd1giiqhGWHWwGjjQsIkkr1gZgJbnqrqt0FEf9ulVb21tLDJopeOg50lNZN0Akbn6NUQynnzSw2yL7BKhxb-qKyJNOk3Cfum3cAhQilcKJUMFTC9GS4BIjXxFQ0Nk_NvIabV7CnDHXfrWoCAxwF1eqGwmhycoMwaWUi1cWfQPc6J1EZTAMfBPeNGsqNtm7oSM98RkDXG_YJ1AozMRD04oUI1uTrCIIXRXTTcrGxFIlWAbJKlzzBTMODFQu7pFJdoegBiUg"
    }

response = requests.request("GET", url, headers=headers, params=querystring)

print(response.text)
```

```php
<?php

$curl = curl_init();

curl_setopt_array($curl, array(
  CURLOPT_URL => "https://api.ando.la/v1/shipment?trackingID=6769",
  CURLOPT_RETURNTRANSFER => true,
  CURLOPT_ENCODING => "",
  CURLOPT_MAXREDIRS => 10,
  CURLOPT_TIMEOUT => 30,
  CURLOPT_HTTP_VERSION => CURL_HTTP_VERSION_1_1,
  CURLOPT_CUSTOMREQUEST => "GET",
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
	"net/http"
	"io/ioutil"
)

func main() {

	url := "https://api.ando.la/v1/shipment?trackingID=6769"

	req, _ := http.NewRequest("GET", url, nil)

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
  "trackingID":"2747"
}
Response Example
{
    "status": {
        "statusID": 19,
        "message": "CLOSED"
    }
}
```
The users can tracking a shipment status. Requires a trackingID, which was returned by 'New Shipment' endpoint. Will return a JSON with statusID and message, which will depend of shipment status itself.

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


## Shipment Status

There are 25 possible status of a shipment that users can tracking through 'Track a Shipment' endpoint.

Status Code | Message
---------- | -------
1	| Cancelled.
2 | Rejected.
3 | On Its way.
4 | Waiting for Payment.
5 | Payment Successful
6 | Payment Rejected
7 | Waiting for Rider
8 | Rider not found
9 | Traveling to Start Address
10 | The rider is at the Start Address
11 | Traveling to End Address
12 | The rider is at the End Address
13 | Package Delivered succesfully to User
14 | Package Delivered to Rider
15 | Delivered Succesfully
16 | Paid
17 | Cancelled
18 | Voided
19 | Closed
20 | Shipment Cancelled by the Rider
21 | Shipment Cancelled by the Receiver
22 | Shipment Cancelled by the Sender
23 | Waiting for Confirmation
24 | Waiting for a Second Confirmation
25 | Started 

## Cancel a Shipment

```shell
curl --request POST \
  --url 'https://api.ando.la/v1/shipment/cancel' \
  --header 'Authorization: Bearer gSJyUaU_ThBDXU_eZ0SWeuvdEK4B-Hjb-kpSFqs5ZLaw5RhA2Ibv68ubrC6_T4eu6-X6k_z6vPMN8EoyOOs1reiS3YegDPiAqwBvZZc97m1LmfGsu_e1502xR2BH0tBv5B3DseRbu187aUyznocvEUVheeVFmxjESnbAcywWT-38OaJqw5AUTOwnCm2tv8EI_xmk8S2dpqYEMOJ_djnQKrB8d-PnGiSadaV8GMn8mjraWcfculVQ25wVceVoqiOYi3KBi7i0XrjLAOgSVv_uwM5wEu7abo-p2ZsW-SsUPEE' \
  --header 'Content-Type: application/json' \
  --data '{
  "trackingID":"2747"
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
    "Authorization": "Bearer gSJyUaU_ThBDXU_eZ0SWeuvdEK4B-Hjb-kpSFqs5ZLaw5RhA2Ibv68ubrC6_T4eu6-X6k_z6vPMN8EoyOOs1reiS3YegDPiAqwBvZZc97m1LmfGsu_e1502xR2BH0tBv5B3DseRbu187aUyznocvEUVheeVFmxjESnbAcywWT-38OaJqw5AUTOwnCm2tv8EI_xmk8S2dpqYEMOJ_djnQKrB8d-PnGiSadaV8GMn8mjraWcfculVQ25wVceVoqiOYi3KBi7i0XrjLAOgSVv_uwM5wEu7abo-p2ZsW-SsUPEE"
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

req.write(JSON.stringify({ trackingID: '2747' }));
req.end();
```

```ruby
require 'uri'
require 'net/http'

url = URI("https://api.ando.la/v1/shipment/cancel")

http = Net::HTTP.new(url.host, url.port)

request = Net::HTTP::Post.new(url)
request["Content-Type"] = 'application/json'
request["Authorization"] = 'Bearer gSJyUaU_ThBDXU_eZ0SWeuvdEK4B-Hjb-kpSFqs5ZLaw5RhA2Ibv68ubrC6_T4eu6-X6k_z6vPMN8EoyOOs1reiS3YegDPiAqwBvZZc97m1LmfGsu_e1502xR2BH0tBv5B3DseRbu187aUyznocvEUVheeVFmxjESnbAcywWT-38OaJqw5AUTOwnCm2tv8EI_xmk8S2dpqYEMOJ_djnQKrB8d-PnGiSadaV8GMn8mjraWcfculVQ25wVceVoqiOYi3KBi7i0XrjLAOgSVv_uwM5wEu7abo-p2ZsW-SsUPEE'
request.body = "{\r\n  \"trackingID\":\"2747\" \r\n}"

response = http.request(request)
puts response.read_body
```

```python
import requests

url = "https://api.ando.la/v1/shipment/cancel"

payload = "{\r\n  \"trackingID\":\"2747\" \r\n}"
headers = {
    'Content-Type': "application/json",
    'Authorization': "Bearer gSJyUaU_ThBDXU_eZ0SWeuvdEK4B-Hjb-kpSFqs5ZLaw5RhA2Ibv68ubrC6_T4eu6-X6k_z6vPMN8EoyOOs1reiS3YegDPiAqwBvZZc97m1LmfGsu_e1502xR2BH0tBv5B3DseRbu187aUyznocvEUVheeVFmxjESnbAcywWT-38OaJqw5AUTOwnCm2tv8EI_xmk8S2dpqYEMOJ_djnQKrB8d-PnGiSadaV8GMn8mjraWcfculVQ25wVceVoqiOYi3KBi7i0XrjLAOgSVv_uwM5wEu7abo-p2ZsW-SsUPEE"
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
  CURLOPT_POSTFIELDS => "{\r\n  \"trackingID\":\"2747\" \r\n}",
  CURLOPT_HTTPHEADER => array(
    "Authorization: Bearer gSJyUaU_ThBDXU_eZ0SWeuvdEK4B-Hjb-kpSFqs5ZLaw5RhA2Ibv68ubrC6_T4eu6-X6k_z6vPMN8EoyOOs1reiS3YegDPiAqwBvZZc97m1LmfGsu_e1502xR2BH0tBv5B3DseRbu187aUyznocvEUVheeVFmxjESnbAcywWT-38OaJqw5AUTOwnCm2tv8EI_xmk8S2dpqYEMOJ_djnQKrB8d-PnGiSadaV8GMn8mjraWcfculVQ25wVceVoqiOYi3KBi7i0XrjLAOgSVv_uwM5wEu7abo-p2ZsW-SsUPEE",
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

	payload := strings.NewReader("{\r\n  \"trackingID\":\"2747\" \r\n}")

	req, _ := http.NewRequest("POST", url, payload)

	req.Header.Add("Content-Type", "application/json")
	req.Header.Add("Authorization", "Bearer gSJyUaU_ThBDXU_eZ0SWeuvdEK4B-Hjb-kpSFqs5ZLaw5RhA2Ibv68ubrC6_T4eu6-X6k_z6vPMN8EoyOOs1reiS3YegDPiAqwBvZZc97m1LmfGsu_e1502xR2BH0tBv5B3DseRbu187aUyznocvEUVheeVFmxjESnbAcywWT-38OaJqw5AUTOwnCm2tv8EI_xmk8S2dpqYEMOJ_djnQKrB8d-PnGiSadaV8GMn8mjraWcfculVQ25wVceVoqiOYi3KBi7i0XrjLAOgSVv_uwM5wEu7abo-p2ZsW-SsUPEE")

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
  "trackingID":"2747"
}
Response Example
{
    "status": 200,
    "message": "Delivery cancelled"
}
```
The users can delete their shipments. In order to begin a new cancellation, the trackingID is required, provided after the confirmation of a new shipment.

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
