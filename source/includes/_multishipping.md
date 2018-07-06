# MultiShipping

## New MultiShipment

```shell
curl --request POST \
  --url 'https://api.ando.la/v1/enterprise/shipments' \
  --header 'Authorization: Bearer D93fM7thTTVrTYmqpDMT2o5ReUxL6FeOM1hoZtOcgYaS8ds1d9qjWOoOn_mUFh7RBr5DuJG36AOLHf6Eqx5IqDcyfjcVkWHw5QO8ZflZjn8B8fbabRfiEujX7tWY-0jZnO9zhQqrMuPoTuvAaGerh_SASgQRlXI6y4LNF2Pyu8Z9iO4slihAawVM5R356C83TbDPpxqPyHhksTFQTBqELtjB8bCxDcQDkfSf4AkTpFDpFL8OTP0-OKZ9AYPoNfbUnr02dDW3SbBcFqPVLgPbkYiuUJojaO4XYGbSY7QwUa4' \
  --header 'Content-Type: application/json'
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
    "enterprise",
    "shipments"
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

req.write(JSON.stringify({ 
    shipTo: [
        {
            firstName: 'Ulises',
            lastName:  'Vargas',
            email:     'ulisesv@email.com',
            phone:     '123456789',
            addressStreet: 'Falsa',
            addressNumber:  '123',
            city:           'Caracas',
            country:        'Venezuela',
            province:       'Distrito Federal',
            instructions:   'Dejar en el buzón'
        },
        {
            firstName: 'Claudia',
            lastName:  'Cerda',
            email:     'claudiac@email.com',
            phone:     '123456789',
            addressStreet: 'Falsa2',
            addressNumber:  '123',
            city:           'Caracas',
            country:        'Venezuela',
            province:       'Distrito Federal',
            instructions:   'Tocar timbre'
        }
    ],
    shipFrom_city: 'Buenos Aires',
    shipFrom_country: 'Argentina',
    shipFrom_addressStreet: 'Rivadavia',
    shipFrom_addressNumber: '123',
    shipFrom_province: "CABA",
    packageWidth: 22.50,
    packageLarge: 22.50,
    packageHeight: 22.50,
    packageWeight: 1.00,
    currency: 'USD'
}));

req.end()
```

```ruby
require 'uri'
require 'net/http'

url = URI("https://api.ando.la/v1/enterprise/shipments")

http = Net::HTTP.new(url.host, url.port)

request = Net::HTTP::Post.new(url)
request["Content-Type"] = 'application/json'
request["Authorization"] = 'Bearer TxuLf62rVjOrNPiGfqSkrccTkLJFHVAmafOjsZd_n8N-LgpcCe47gS-6hfN2iEcstgz_S63B3lYdbQvlD8uRYNQHEuez3dQisNp3gVlwHh27pDtCX2-d4bKnDo20_VRVO9V2PX-6xkA6YH3aSHp1SKOeQ-lYMdt-Y-NvIuRhHzrNrSZTN_qPVrEq3-hiTlgXk670chAAoeVufK8mKIYcljgAMZRPxSDZ0J0vaci8aPd0PG8N-sNPe5vq_y5DEIqVOjSHL7H4ubyzpkl2-JxIyO5B7ldDIse_jmxjWXmScmw'
request.body = "{\r\n \"shipTo\":\r\n[
\r\n{\r\n
\"firstName\":\"Ulises\",\"lastName\":\"Vargas\",\r\n
\"email\":\"ulisesv@email.com\",\r\n
\"phone\":\"123456789\",\r\n
\"addressStreet\":\"Falsa\",\r\n
\"addressNumber\":\"123\",\r\n
\"city\":\"Caracas\",\r\n
\"country\":\"Venezuela\",\r\n
\"province\":\"Distrito Federal\",\r\n
\"instructions\":\"Dejar en el buzón\"\r\n
},\r\n{
\"firstName\":\"Claudia\",\r\n
\"lastName\":\"Cerda\",\r\n
\"email\":\"claudiac@email.com\",\r\n
\"phone\":\"123456789\",\r\n
\"addressStreet\":\"Falsa2\",\r\n
\"addressNumber\":\"123\",\r\n
\"city\":\"Caracas\",\r\n
\"country\":\"Venezuela\",\r\n
\"province\":\"Distrito Federal\",\r\n
\"instructions\":\"Tocar timbre\"\r\n
}\r\n],\r\n
\"shipFrom_city\":\"Buenos Aires\",\r\n
\"shipFrom_country\":\"Argentina\",\r\n
\"shipFrom_addressStreet\":\"Rivadavia\",\r\n
\"shipFrom_province\":\"CABA\",\r\n
\"shipFrom_addressNumber\":\"123\",\r\n
\"packageWidth\":22.50,\r\n
\"packageLarge\":22.50,\r\n
\"packageHeight\":22.50,\r\n
\"packageWeight\":1.00,\r\n
\"currency: 'USD'\"\r\n
}"

response = http.request(request)
puts response.read_body
```
```python
import requests

url = "https://api.ando.la/v1/enterprise/shipments"

payload = "{\r\n \"shipTo\":\r\n[\r\n{\r\n\"firstName\":\"Ulises\",\"lastName\":\"Vargas\",\r\n\"email\":\"ulisesv@email.com\",\r\n\"phone\":\"123456789\",\r\n\"addressStreet\":\"Falsa\",\r\n\"addressNumber\":\"123\",\r\n\"city\":\"Caracas\",\r\n\"country\":\"Venezuela\",\r\n\"province\":\"Distrito Federal\",\r\n\"instructions\":\"Dejar en el buzón\"\r\n},\r\n{\"firstName\":\"Claudia\",\r\n\"lastName\":\"Cerda\",\r\n\"email\":\"claudiac@email.com\",\r\n\"phone\":\"123456789\",\r\n\"addressStreet\":\"Falsa2\",\r\n\"addressNumber\":\"123\",\r\n\"city\":\"Caracas\",\r\n\"country\":\"Venezuela\",\r\n\"province\":\"Distrito Federal\",\r\n\"instructions\":\"Tocar timbre\"\r\n}\r\n],\r\n\"shipFrom_city\":\"Buenos Aires\",\r\n\"shipFrom_country\":\"Argentina\",\r\n\"shipFrom_addressStreet\":\"Rivadavia\",\r\n\"shipFrom_province\":\"CABA\",\r\n\"shipFrom_addressNumber\":\"123\",\r\n\"packageWidth\":22.50,\r\n\"packageLarge\":22.50,\r\n\"packageHeight\":22.50,\r\n\"packageWeight\":1.00,\r\n\"currency: 'USD'\"\r\n}"

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
  CURLOPT_URL => "https://api.ando.la/v1/enterprise/shipments",
  CURLOPT_RETURNTRANSFER => true,
  CURLOPT_ENCODING => "",
  CURLOPT_MAXREDIRS => 10,
  CURLOPT_TIMEOUT => 30,
  CURLOPT_HTTP_VERSION => CURL_HTTP_VERSION_1_1,
  CURLOPT_CUSTOMREQUEST => "POST",
  CURLOPT_POSTFIELDS => "{\r\n \"shipTo\":\r\n[\r\n{\r\n\"firstName\":\"Ulises\",\"lastName\":\"Vargas\",\r\n\"email\":\"ulisesv@email.com\",\r\n\"phone\":\"123456789\",\r\n\"addressStreet\":\"Falsa\",\r\n\"addressNumber\":\"123\",\r\n\"city\":\"Caracas\",\r\n\"country\":\"Venezuela\",\r\n\"province\":\"Distrito Federal\",\r\n\"instructions\":\"Dejar en el buzón\"\r\n},\r\n{\"firstName\":\"Claudia\",\r\n\"lastName\":\"Cerda\",\r\n\"email\":\"claudiac@email.com\",\r\n\"phone\":\"123456789\",\r\n\"addressStreet\":\"Falsa2\",\r\n\"addressNumber\":\"123\",\r\n\"city\":\"Caracas\",\r\n\"country\":\"Venezuela\",\r\n\"province\":\"Distrito Federal\",\r\n\"instructions\":\"Tocar timbre\"\r\n}\r\n],\r\n\"shipFrom_city\":\"Buenos Aires\",\r\n\"shipFrom_country\":\"Argentina\",\r\n\"shipFrom_addressStreet\":\"Rivadavia\",
  \r\n\"shipFrom_province":\"CABA\",
  \r\n\"shipFrom_addressNumber\":\"123\",\r\n\"packageWidth\":22.50,\r\n\"packageLarge\":22.50,\r\n\"packageHeight\":22.50,\r\n\"packageWeight\":1.00,\r\n\"currency: 'USD'\"\r\n}",
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

	url := "https://api.ando.la/v1/enterprise/shipments"

  payload := strings.NewReader("{\r\n \"shipTo\":\r\n[\r\n{\r\n\"firstName\":\"Ulises\",\"lastName\":\"Vargas\",\r\n\"email\":\"ulisesv@email.com\",\r\n\"phone\":\"123456789\",\r\n\"addressStreet\":\"Falsa\",\r\n\"addressNumber\":\"123\",\r\n\"city\":\"Caracas\",\r\n\"country\":\"Venezuela\",\r\n\"province\":\"Distrito Federal\",\r\n\"instructions\":\"Dejar en el buzón\"\r\n},\r\n{\"firstName\":\"Claudia\",\r\n\"lastName\":\"Cerda\",\r\n\"email\":\"claudiac@email.com\",\r\n\"phone\":\"123456789\",\r\n\"addressStreet\":\"Falsa2\",\r\n\"addressNumber\":\"123\",\r\n\"city\":\"Caracas\",\r\n\"country\":\"Venezuela\",\r\n\"province\":\"Distrito Federal\",\r\n\"instructions\":\"Tocar timbre\"\r\n}\r\n],\r\n\"shipFrom_city\":\"Buenos Aires\",\r\n\"shipFrom_country\":\"Argentina\",\r\n\"shipFrom_addressStreet\":\"Rivadavia\",
  \r\n\"shipFrom_province\":\"CABA\",\r\n\"shipFrom_addressNumber\":\"123\",\r\n\"packageWidth\":22.50,\r\n\"packageLarge\":22.50,\r\n\"packageHeight\":22.50,\r\n\"packageWeight\":1.00,\r\n\"currency: 'USD'\"\r\n}")

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
  "shipTo": [
        {
            "firstName": "Ulises",
            "lastName":  "Vargas",
            "email":     "ulisesv@email.com",
            "phone":     "123456789",
            "addressStreet": "Falsa",
            "addressNumber":  "123",
            "city":           "Caracas",
            "country":        "Venezuela",
            "province":       "Distrito Federal",
            "instructions":   "Dejar en el buzón"
        },
        {
            "firstName": "Claudia",
            "lastName":  "Cerda",
            "email":     "claudiac@email.com",
            "phone":     "123456789",
            "addressStreet": "Falsa2",
            "addressNumber":  "123",
            "city":           "Caracas",
            "country":        "Venezuela",
            "province":       "Distrito Federal",
            "instructions":   "Tocar timbre"
        }
    ],
    "shipFrom_city": "Buenos Aires",
    "shipFrom_country": "Argentina",
    "shipFrom_addressStreet": "Rivadavia",
    "shipFrom_addressNumber": "123",
    "shipFrom_province": "CABA",
    "packageWidth": 22.50,
    "packageLarge": 22.50,
    "packageHeight": 22.50,
    "packageWeight": 1.00,
    "currency": "USD"
}
Response Example
[
    {
        "id": 13322,
        "userFromID": 306,
        "placeFromID": 26222,
        "placeToID": 26223,
        "activationDate": "2018-07-06T16:32:14.313Z",
        "userToID": 306,
        "mailUserTo": "ulisesv@email.com",
        "userToPhone": "123456789",
        "shipmentNumber": "",
        "creatorUserId": 306,
        "userSurnameTo": "Vargas",
        "userNameTo": "Ulises",
        "type": "LS",
        "try": 0,
        "parentID": 13321
    },
    {
        "id": 13323,
        "userFromID": 306,
        "placeFromID": 26222,
        "placeToID": 26224,
        "activationDate": "2018-07-06T16:32:14.313Z",
        "userToID": 306,
        "mailUserTo": "claudiac@email.com",
        "userToPhone": "123456789",
        "shipmentNumber": "",
        "creatorUserId": 306,
        "userSurnameTo": "Cerda",
        "userNameTo": "Claudia",
        "type": "LS",
        "try": 0,
        "parentID": 13321
    }
]
```

The users can init a new shipment with an unique origin and multiple destinations (each destination as object in an array). 

### HTTP Request

`POST https://api.ando.la/v1/enterprise/shipments`

Header | Content
--------- | -----------
Authorization | Bearer 4b73b11dc60ee75959eca2c117614e9741dfc99a
Content-type | application/json

### BODY Parameters

Parameter | Description
--------- | -----------
shipTo:   |  Array
firstName:| `String` First name of receiver.
lastName: | `String`  Last Name of receiver.
email:    | `String`     Email of receiver.
phone:    | `String`     Phone of receiver.
addressStreet: | `String` Street of receiver.
addressNumber: | `String` Address number of receiver.
city:     | `String`     City of receiver.
country:  | `String`     Country of receiver.
province: | `String`     Province of receiver.
phone:    | `String`     Phone of receiver.
instructions:  | `String` Instructions given by receiver.
orderNumber: (OPTIONAL)| `String` Number of order.
floor: (OPTIONAL)| `String` Floor number of receiver.
apartment: (OPTIONAL)| `String` Apartment number of receiver.
--------- | -----------
shipFrom_city:          | `String` City of sender.
shipFrom_country:       | `String` Country number of sender.
shipFrom_province:      | `String` Province number of sender.
shipFrom_addressStreet: | `String` Street number of sender. 
shipFrom_addressNumber: | `String` Address number of sender. 
packageWidth:           | `Double` Width of package.
packageLarge:           | `Double` Large of package.
packageHeight:          | `Double` Height of package.
packageWeight:          | `Double` Weight of package.
currency:               | `String` Currency used in payment.
shipFrom_Instructions: (OPTIONAL) | `String` Instructions given by sender.
floor: (OPTIONAL)| `String` Floor number of sender.
apartment: (OPTIONAL)| `String` Apartment number of sender.

## Get Multishipment By ID

```shell
curl --request GET \
  --url 'https://api.ando.la/v1/enterprise/shipments' \
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
    "enterprise",
    "shipments"
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

url = URI("https://api.ando.la/v1/enterprise/shipments")

http = Net::HTTP.new(url.host, url.port)

request = Net::HTTP::Get.new(url)
request["Authorization"] = 'Bearer Ec2_giC2EuDGPvXBvQ-ej4SF4bpB4rAF9PKH8XSqMmmZ4VLh062P1s1EBFYm_xP5ox9QtFXjEw9odekbuqyKop0zEHokJJsQdrK9X-fzuVEH-0IOq-c2IgxbmCB5NBDKJR1tYIN7NEob5UG5iLgcpsjsqJzbY_257moesQ0dD0Pxhg5P_SHWn-Xd_-WC5TIq4DRUNWFcft35-o2cskrw9zt_klG8PmjJXYRP83EK7las3rKwxs_EozTZ1cOnzK_-Jjppg_gUkFBgrLi6QFRdM8FhY8fdAD5fU4f0d4UUGCo'

response = http.request(request)
puts response.read_body
```

```python
import requests

url = "https://api.ando.la/v1/enterprise/shipments"

headers = {'Authorization': 'Bearer Ec2_giC2EuDGPvXBvQ-ej4SF4bpB4rAF9PKH8XSqMmmZ4VLh062P1s1EBFYm_xP5ox9QtFXjEw9odekbuqyKop0zEHokJJsQdrK9X-fzuVEH-0IOq-c2IgxbmCB5NBDKJR1tYIN7NEob5UG5iLgcpsjsqJzbY_257moesQ0dD0Pxhg5P_SHWn-Xd_-WC5TIq4DRUNWFcft35-o2cskrw9zt_klG8PmjJXYRP83EK7las3rKwxs_EozTZ1cOnzK_-Jjppg_gUkFBgrLi6QFRdM8FhY8fdAD5fU4f0d4UUGCo'}

response = requests.request("GET", url, headers=headers)

print(response.text)
```

```php
<?php

$curl = curl_init();

curl_setopt_array($curl, array(
  CURLOPT_URL => "https://api.ando.la/v1/enterprise/shipments",
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

	url := "https://api.ando.la/v1/enterprise/shipments"

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
    "specialInstructions": null,
    "orderNumber": null,
    "type": "LS",
    "shipmentNumber": "",
    "activationDate": "2018-07-06T16:32:14.313Z",
    "shipmentStatus": [
        {
            "id": 91842,
            "id_envio": 13322,
            "estado": "SIN_TRANSPORTE",
            "subestado": "",
            "fecha_desde": "2018-07-06T16:32:15.163Z",
            "fecha_hasta": null
        }
    ]
}
```


The users can to get a multiple shipment with their ID's. 

### HTTP Request

`GET https://api.ando.la/v1/enterprise/shipments/:id`

Header | Content
--------- | -----------
Authorization | Bearer 4b73b11dc60ee75959eca2c117614e9741dfc99a
Content-type | application/json

### URL Parameters

Parameter | Description
--------- | -----------
id | `Integer` Your ID.



