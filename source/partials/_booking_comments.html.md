
# Bookings Comments

## index

Allows the user to retrieve all the booking comments for a given booking

### HTTP Request

`GET http://staging.gojourny.com/api/v3/bookings/<BOOKING_ID>/booking_comments/>`

### Query Parameters

Parameter | Description
--------- | -------
BOOKING_ID | The booking id

```json
[
  {
    "id": "984288fb-3927-43b4-bfc2-8a8b5918fb4a",
    "comment": "New Comment",
    "booking_id": "cec314cd-2722-4baa-8638-0ca3cefcbc79",
    "user_id": 23573,
    "user_name": "Mauroo Campillo"
  }
]
```

## show

Allows the user to retrieve a specific booking comment

### HTTP Request

`GET http://staging.gojourny.com/api/v3/bookings/<BOOKING_ID>/booking_comments/<BOOKING_COMMENT_ID>`

### Query Parameters

Parameter | Description
--------- | -------
BOOKING_ID | The booking id
BOOKING_COMMENT_ID | The booking comment id

> The above command returns JSON structured like this:

```json
{
  "id": "984288fb-3927-43b4-bfc2-8a8b5918fb4a",
  "comment": "New Comment",
  "booking_id": "cec314cd-2722-4baa-8638-0ca3cefcbc79",
  "user_id": 23573,
  "user_name": "Mauroo Campillo"
}
```

## Create

Allows the user to create a booking comment

### HTTP Request

`POST http://staging.gojourny.com/api/v3/bookings/<BOOKING_ID>/booking_comments/`

### Query Parameters

Parameter | Description
--------- | -------
BOOKING_ID | The booking id

### Body Parameters

Parameter | Description
----------|-------------
booking_comment['comment'] | The comment

> The above command returns JSON structured like this:

```json
{
  "id": "984288fb-3927-43b4-bfc2-8a8b5918fb4a",
  "comment": "New Comment",
  "booking_id": "cec314cd-2722-4baa-8638-0ca3cefcbc79",
  "user_id": 23573,
  "user_name": "Mauroo Campillo"
}
```

## Update

Allows the user to update a booking comment

### HTTP Request

`PUT http://staging.gojourny.com/api/v3/bookings/<BOOKING_ID>/booking_comments/<BOOKING_COMMENT_ID>`

### Query Parameters

Parameter | Description
--------- | -------
BOOKING_ID | The booking id
BOOKING_COMMENT_ID | The booking comment id

### Body Parameters

Parameter | Description
----------|-------------
booking_comment['comment'] | The comment

> The above command returns JSON structured like this:

```json
{
  "id": "984288fb-3927-43b4-bfc2-8a8b5918fb4a",
  "comment": "New Comment",
  "booking_id": "cec314cd-2722-4baa-8638-0ca3cefcbc79",
  "user_id": 23573,
  "user_name": "Mauroo Campillo"
}
```

## Destroy

Allows the user to delete a booking comment

### HTTP Request

`DELETE http://staging.gojourny.com/api/v3/bookings/<BOOKING_ID>`

Parameter | Description
--------- | -------
BOOKING_ID | The booking id

> The above command returns JSON structured like this:

```json
{
  "id": "984288fb-3927-43b4-bfc2-8a8b5918fb4a",
  "comment": "New Comment",
  "booking_id": "cec314cd-2722-4baa-8638-0ca3cefcbc79",
  "user_id": 23573,
  "user_name": "Mauroo Campillo"
}
```
