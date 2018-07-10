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

The users will receive an array with information about their shipments with multiple destinations. In order to add a new webhook, you must send an email to `soporte@ando.la` with the subject `API-WEBHOOK`. For more information about `status` you can consult the `Shipment Status` section in `Shipping`.

