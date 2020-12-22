
# Booking Options

## index

Allows the user to retrieve all the booking options for a given booking

### HTTP Request

`GET http://staging.gojourny.com/api/v3/bookings/<BOOKING_ID>/booking_options`

### Query Parameters

Parameter | Description
--------- | -------
BOOKING_ID | The booking id
BOOKING_OPTION | The booking option id

```json
[
  {
    "id": "237ffb97-6d6b-4575-ac56-ce5002841712",
    "description": "Booking Option Description",
    "booking_id": "cec314cd-2722-4baa-8638-0ca3cefcbc79",
    "location_id": 18733
  }
]
```

## show

Allows the user to retrieve a specific booking option

### HTTP Request

`GET http://staging.gojourny.com/api/v3/bookings/<BOOKING_ID>/booking_options/<BOOKING_OPTION_ID>`

### Query Parameters

Parameter | Description
--------- | -------
BOOKING_ID | The booking id
BOOKING_OPTION | The booking option id

> The above command returns JSON structured like this:

```json
{
  "id": "237ffb97-6d6b-4575-ac56-ce5002841712",
  "description": "Booking Option Description",
  "booking_id": "cec314cd-2722-4baa-8638-0ca3cefcbc79",
  "location_id": 18733
}
```

## Create

Allows the user to create a booking option

### HTTP Request

`POST http://staging.gojourny.com/api/v3/bookings/<BOOKING_ID>/booking_options>`

### Query Parameters

Parameter | Description
--------- | -------
BOOKING_ID | The booking id
BOOKING_OPTION | The booking option id

### Body Parameters

Parameter | Description
----------|-------------
booking['description'] | The description of the booking option description
booking['location_id'] | The location id

> The above command returns JSON structured like this:

```json
{
  "id": "237ffb97-6d6b-4575-ac56-ce5002841712",
  "description": "Booking Option Description",
  "booking_id": "cec314cd-2722-4baa-8638-0ca3cefcbc79",
  "location_id": 18733
}
```

## Update

Allows the user to update a booking option

### HTTP Request

`PUT http://staging.gojourny.com/api/v3/bookings/<BOOKING_ID>/booking_options/<BOOKING_OPTION_ID>`

### Query Parameters

Parameter | Description
--------- | -------
BOOKING_ID | The booking id
BOOKING_OPTION | The booking option id

### Body Parameters

Parameter | Description
----------|-------------
booking['description'] | The description of the booking option description
booking['location_id'] | The location id

> The above command returns JSON structured like this:

```json
{
  "id": "237ffb97-6d6b-4575-ac56-ce5002841712",
  "description": "Booking Option Description",
  "booking_id": "cec314cd-2722-4baa-8638-0ca3cefcbc79",
  "location_id": 18733
}
```

## Destroy

Allows the user to delete a booking option

### HTTP Request

`DELETE http://staging.gojourny.com/api/v3/bookings/<BOOKING_ID>/booking_options/<BOOKING_OPTION_ID>`

Parameter | Description
--------- | -------
BOOKING_ID | The booking id
BOOKING_OPTION | The booking option id

> The above command returns JSON structured like this:

```json
{
  "id": "237ffb97-6d6b-4575-ac56-ce5002841712",
  "description": "Booking Option Description",
  "booking_id": "cec314cd-2722-4baa-8638-0ca3cefcbc79",
  "location_id": 18733
}
```
