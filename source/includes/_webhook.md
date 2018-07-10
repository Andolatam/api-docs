# Webhook

```json
Response Example
{
"webhook": 
[ 
  { "id": 13349,
   "creatorID": 306,
   "status": { 
     "statusCode": 23, 
     "status": "Waiting for Confirmation" 
    },
   "total": 123,
   "MultishipmentByID": "13348",
   "orderNumber": "customOrderNumber"
   } 
]
}
```

The users will receive an array with information about their shipments with multiple destinations. In order to add a new webhook, you must send an email to `soporte@ando.la` with the subject `API-WEBHOOK`. 

### Status Codes

There are 25 possible status of a multiple shipment that users can tracking through webhook.

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