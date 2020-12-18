
# Bookings

## index

Allows the user to retrieve all the bookings for a given itinerary

### HTTP Request

`GET http://staging.gojourny.com/api/v3/itineraries/<ITINERARY_ID>/bookings>`

### Query Parameters

Parameter | Description
--------- | -------
ITINERARY_ID | The itinerary id

```json
[
  {
      "id": "cec314cd-2722-4baa-8638-0ca3cefcbc79",
      "bookable_id": "c3f12ef1-4e51-4d67-a6db-ec7bad5df445",
      "bookable_type": "Hotel",
      "itinerary_id": "NYLL",
      "net_price": "50000.0",
      "commission": "5.0",
      "tax": "1000.0",
      "status": "pending",
      "note": "Example note",
      "start_date": "2022-01-15",
      "end_date": "2022-01-23",
      "booking_items": [],
      "booking_comments": []
  }
]
```

## show

Allows the user to retrieve a specific booking

### HTTP Request

`GET http://staging.gojourny.com/api/v3/itineraries/<ITINERARY_ID>/bookings/<BOOKING_ID>`

### Query Parameters

Parameter | Description
--------- | -------
ITINERARY_ID | The itinerary id
BOOKING_ID | The booking id

> The above command returns JSON structured like this:

```json
{
    "id": "cec314cd-2722-4baa-8638-0ca3cefcbc79",
    "bookable_id": "c3f12ef1-4e51-4d67-a6db-ec7bad5df445",
    "bookable_type": "Hotel",
    "itinerary_id": "NYLL",
    "status": "pending",
    "note": "Example note",
    "start_date": "2022-01-15",
    "end_date": "2022-01-23",
    "booking_items": [],
    "booking_comments": []
}
```

## Create

Allows the user to create a booking

### HTTP Request

`POST http://staging.gojourny.com/api/v3/itineraries/<ITINERARY_ID>/bookings`

### Query Parameters

Parameter | Description
--------- | -------
ITINERARY_ID | The itinerary id

### Body Parameters

Parameter | Description
----------|-------------
booking['bookable_id'] | The bookable id (hotel id or room id)
booking['bookable_type'] | The bookable type (The class, like: Hotel or Room)
booking['trip_section_id'] | The trip section id
booking['day_item_id'] | The day item id
booking['itinerary_item_id'] | The location item or accommodation item id
booking['booker_id'] | The trip designer o admin user who is managing the booking
booking['amount_paid'] | The paid amount for the itinerary
booking['status'] | The status
booking['note'] | Any note
booking['start_date'] | Start date or check in date
booking['end_date'] | End date or check out date

> The above command returns JSON structured like this:

```json
{
    "id": "cec314cd-2722-4baa-8638-0ca3cefcbc79",
    "bookable_id": "c3f12ef1-4e51-4d67-a6db-ec7bad5df445",
    "bookable_type": "Hotel",
    "itinerary_id": "NYLL",
    "status": "pending",
    "note": "Example note",
    "start_date": "2022-01-15",
    "end_date": "2022-01-23",
    "booking_items": [],
    "booking_comments": []
}
```

## Update

Allows the user to update a booking

### HTTP Request

`PUT http://staging.gojourny.com/api/v3/itineraries/<ITINERARY_ID>/bookings<BOOKING_ID>`

### Query Parameters

Parameter | Description
--------- | -------
ITINERARY_ID | The itinerary id
BOOKING_ID | The booking id

### Body Parameters

Parameter | Description
----------|-------------
booking['bookable_id'] | The bookable id (hotel id or room id)
booking['bookable_type'] | The bookable type (The class, like: Hotel or Room)
booking['trip_section_id'] | The trip section id
booking['day_item_id'] | The day item id
booking['itinerary_item_id'] | The location item or accommodation item id
booking['booker_id'] | The trip designer o admin user who is managing the booking
booking['amount_paid'] | The paid amount for the itinerary
booking['status'] | The status
booking['note'] | Any note
booking['start_date'] | Start date or check in date
booking['end_date'] | End date or check out date

> The above command returns JSON structured like this:

```json
{
    "id": "cec314cd-2722-4baa-8638-0ca3cefcbc79",
    "bookable_id": "c3f12ef1-4e51-4d67-a6db-ec7bad5df445",
    "bookable_type": "Hotel",
    "itinerary_id": "NYLL",
    "status": "pending",
    "note": "Example note",
    "start_date": "2022-01-15",
    "end_date": "2022-01-23",
    "booking_items": [],
    "booking_comments": []
}
```

## Destroy

Allows the user to delete a booking

### HTTP Request

`DELETE http://staging.gojourny.com/api/v3/bookings/<BOOKING_ID>`

Parameter | Description
--------- | -------
BOOKING_ID | The booking id

> The above command returns JSON structured like this:

```json
{
    "id": "cec314cd-2722-4baa-8638-0ca3cefcbc79",
    "bookable_id": "c3f12ef1-4e51-4d67-a6db-ec7bad5df445",
    "bookable_type": "Hotel",
    "itinerary_id": "NYLL",
    "status": "pending",
    "note": "Example note",
    "start_date": "2022-01-15",
    "end_date": "2022-01-23",
    "booking_items": [],
    "booking_comments": []
}
```
