
# Booking Items

## index

Allows the user to retrieve all the booking items for a given booking

### HTTP Request

`GET http://staging.gojourny.com/api/v3/bookings/<BOOKING_ID>/booking_items/>`

### Query Parameters

Parameter | Description
--------- | -------
BOOKING_ID | The booking id

```json
[
  {
    "id": "cd9bf003-48d9-46d1-8d30-424b6f4c4ee9",
    "name": "Cutom name",
    "description": "Description if needed",
    "bookable_id": "1626a4cd-cf29-4686-b878-4e4d6548de48",
    "bookable_type": "Room"
  }
]
```

## show

Allows the user to retrieve a specific booking item

### HTTP Request

`GET http://staging.gojourny.com/api/v3/bookings/<BOOKING_ID>/booking_items/<BOOKING_ITEM_ID>`

### Query Parameters

Parameter | Description
--------- | -------
BOOKING_ID | The booking id
BOOKING_ITEM_ID | The booking item id

> The above command returns JSON structured like this:

```json
{
  "id": "cd9bf003-48d9-46d1-8d30-424b6f4c4ee9",
  "name": "Cutom name",
  "description": "Description if needed",
  "bookable_id": "1626a4cd-cf29-4686-b878-4e4d6548de48",
  "bookable_type": "Room"
}
```

## Create

Allows the user to create a booking item

### HTTP Request

`POST http://staging.gojourny.com/api/v3/bookings/<BOOKING_ID>/booking_items/`

### Query Parameters

Parameter | Description
--------- | -------
BOOKING_ID | The booking id

### Body Parameters

Parameter | Description
----------|-------------
booking['name'] | The name in case there is no bookable object to associat the booking item with
booking['description'] | The description of the bookable item if needed
booking['bookable_id'] | The bookable id (hotel id or room id)
booking['bookable_type'] |  The bookable type (The class, like: Hotel or Room)

> The above command returns JSON structured like this:

```json
{
    "id": "cd9bf003-48d9-46d1-8d30-424b6f4c4ee9",
    "name": "Cutom name",
    "description": "Description if needed",
    "bookable_id": "1626a4cd-cf29-4686-b878-4e4d6548de48",
    "bookable_type": "Room"
}
```

## Update

Allows the user to update a booking item

### HTTP Request

`PUT http://staging.gojourny.com/api/v3/bookings/<BOOKING_ID>/booking_items/<BOOKING_ITEM_ID>`

### Query Parameters

Parameter | Description
--------- | -------
BOOKING_ID | The booking id
BOOKING_ITEM_ID | The booking item id

### Body Parameters

Parameter | Description
----------|-------------
booking['name'] | The name in case there is no bookable object to associat the booking item with
booking['description'] | The description of the bookable item if needed
booking['bookable_id'] | The bookable id (hotel id or room id)
booking['bookable_type'] |  The bookable type (The class, like: Hotel or Room)

> The above command returns JSON structured like this:

```json
{
    "id": "cd9bf003-48d9-46d1-8d30-424b6f4c4ee9",
    "name": "Cutom name",
    "description": "Description if needed",
    "bookable_id": "1626a4cd-cf29-4686-b878-4e4d6548de48",
    "bookable_type": "Room"
}
```

## Destroy

Allows the user to delete a booking item

### HTTP Request

`DELETE http://staging.gojourny.com/api/v3/bookings/<BOOKING_ID>`

Parameter | Description
--------- | -------
BOOKING_ID | The booking id

> The above command returns JSON structured like this:

```json
{
    "id": "cd9bf003-48d9-46d1-8d30-424b6f4c4ee9",
    "name": "Cutom name",
    "description": "Description if needed",
    "bookable_id": "1626a4cd-cf29-4686-b878-4e4d6548de48",
    "bookable_type": "Room"
}
```
