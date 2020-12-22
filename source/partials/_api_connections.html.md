
# API Connections

## show

Allows the user to retrieve a specific api_connections

### HTTP Request

`GET http://staging.gojourny.com/api/v3/api_connections/<TOUR_ID>`

### Query Parameters

Parameter | Description
--------- | -------
API_CONNECTION_ID | The api connection id

> The above command returns JSON structured like this:

```json
{
    "id": "fd6158b5-dcd8-42aa-ac0f-4e946cfe8c19",
    "connectable_id": "d6ff06a8-b49c-48a8-96a4-d1663cae742d",
    "connectable_type": "Hotel",
    "vendor": "hotel_beds",
    "vendor_id": "661294"
}
```

## Create

Allows the user to create an api connection

### HTTP Request

`POST http://staging.gojourny.com/api/v3/api_connections/<API_CONNECTION_ID>`

Parameter | Description
--------- | -------
API_CONNECTION_ID | The api connection id

### Body Parameters

Parameter | Description
----------|-------------
api_connection['id'] | The api connection id
api_connection['connectable_id'] | The model id we are connecting to
api_connection['connectable_type'] | The model class we are connecting to
api_connection['vendor'] | The vendor/client we are using to connect
api_connection['vendor_id'] | The vendor/client object id

> The above command returns JSON structured like this:

```json
{
    "id": "fd6158b5-dcd8-42aa-ac0f-4e946cfe8c19",
    "connectable_id": "d6ff06a8-b49c-48a8-96a4-d1663cae742d",
    "connectable_type": "Hotel",
    "vendor": "hotel_beds",
    "vendor_id": "661294"
}
```

## Update

Allows the user to update an api connection

### HTTP Request

`PUT http://staging.gojourny.com/api/v3/api_connections/<API_CONNECTION_ID>`

Parameter | Description
--------- | -------
API_CONNECTION_ID | The api connection id

### Body Parameters

Parameter | Description
----------|-------------
api_connection['id'] | The api connection id
api_connection['connectable_id'] | The model id we are connecting to
api_connection['connectable_type'] | The model class we are connecting to
api_connection['vendor'] | The vendor/client we are using to connect
api_connection['vendor_id'] | The vendor/client object id

> The above command returns JSON structured like this:

```json
{
    "id": "fd6158b5-dcd8-42aa-ac0f-4e946cfe8c19",
    "connectable_id": "d6ff06a8-b49c-48a8-96a4-d1663cae742d",
    "connectable_type": "Hotel",
    "vendor": "hotel_beds",
    "vendor_id": "661294"
}
```

## Destroy

Allows the user to delete the Tour, this will also delete all api connections

### HTTP Request

`DELETE http://staging.gojourny.com/api/v3/tour/<API_CONNECTION_ID>`

Parameter | Description
--------- | -------
API_CONNECTION_ID | The api connection id

> The above command returns JSON structured like this:

```json
{
    "id": "fd6158b5-dcd8-42aa-ac0f-4e946cfe8c19",
    "connectable_id": "d6ff06a8-b49c-48a8-96a4-d1663cae742d",
    "connectable_type": "Hotel",
    "vendor": "hotel_beds",
    "vendor_id": "661294"
}
```


