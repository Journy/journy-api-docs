
# Reservations

## Show

### HTTP Request

`GET http://staging.gojourny.com/api/v3/itinerary/<ITINERARY_ID>/reservations/<RESERVATION_ID>`

### Query Parameters

Parameter | Description
--------- | -------
ITINERARY_ID | The itinerary id
RESERVATION_ID | Reservation id
LOCATION_ITEM_ID | The location item id to which the reservations is going to be attached


> The above command returns JSON structured like this:

```json
{
    "reservations": {
        "38458": {
            "id": 38458,
            "timestamp_date": "2021-03-10",
            "timestamp_time": "12:00 AM",
            "itinerary_item_id": 848014,
            "number_of_people": 2,
            "notes": null,
            "confirmed": false,
            "no_show_cancellation_fee": null,
            "attachments": []
        }
    }
}
```

## Create

Allows the user to create a Day Item

### HTTP Request

`POST http://staging.gojourny.com/api/v3/itinerary/<ITINERARY_ID>/reservations`

### Query Parameters

Parameter | Description
--------- | -------
ITINERARY_ID | The itinerary id
LOCATION_ITEM_ID | The location item id to which the reservations is going to be attached

### Body Parameters

Parameter | Description
----------|-------------
reservation[timestamp_date] | The reservation date in `YYYY-MM-DD` or `DD/MM/YYYY` format
reservation[timestamp_time] | The reservation time as `hh:mm`
reservation[number_of_people] | The number of people Integer
reservation[notes] | Additional Notes
reservation[confirmed] | If th reservations is confirmed by the restaurant/hotel/etc
reservation[no_show_cancellation_fee] | Cancellation fee in U$S

> The above command returns JSON structured like this:

```json
{
    "reservations": {
        "38458": {
            "id": 38458,
            "timestamp_date": "2021-03-10",
            "timestamp_time": "12:00 AM",
            "itinerary_item_id": 848014,
            "number_of_people": 2,
            "notes": null,
            "confirmed": false,
            "no_show_cancellation_fee": null,
            "attachments": []
        }
    }
}
```

## Update

Allows the user to edit a Reservation

### HTTP Request

`PUT http://staging.gojourny.com/api/v3/itinerary/<ITINERARY_ID>/reservations/<RESERVATION_ID>?location_item_id=<LOCATION_ITEM_ID>`

### Query Parameters

Parameter | Description
--------- | -------
ITINERARY_ID | The itinerary id
RESERVATION_ID | The reservation id
LOCATION_ITEM_ID | The location item id to which the reservations is going to be attached

### Body Parameters

Parameter | Description
----------|-------------
reservation[timestamp_date] | The reservation date in `YYYY-MM-DD` or `DD/MM/YYYY` format
reservation[timestamp_time] | The reservation time as `hh:mm`
reservation[number_of_people] | The number of people Integer
reservation[notes] | Additional Notes
reservation[confirmed] | If th reservations is confirmed by the restaurant/hotel/etc
reservation[no_show_cancellation_fee] | Cancellation fee in U$S
reservation[attachments] | An array of files

> The above command returns JSON structured like this:

```json
{
    "reservations": {
        "38458": {
            "id": 38458,
            "timestamp_date": "2021-03-10",
            "timestamp_time": "12:00 AM",
            "itinerary_item_id": 848014,
            "number_of_people": 2,
            "notes": null,
            "confirmed": false,
            "no_show_cancellation_fee": null,
            "attachments": []
        }
    }
}
```

## Delete

Allows the user to destroy a reservation, the location item remains unchanged

### HTTP Request

`DELETE http://staging.gojourny.com/api/v3/itinerary/<ITINERARY_ID>/reservations/<RESERVATION_ID>?location_item_id=<LOCATION_ITEM_ID>`

### Query Parameters

Parameter | Description
--------- | -------
ITINERARY_ID | The itinerary id
RESERVATION_ID | The reservation id
LOCATION_ITEM_ID | The location item id to which the reservations is going to be attached

> The above command returns JSON structured like this:

```json
{}
```
