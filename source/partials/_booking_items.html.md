
# Booking Items

## index

Allows the user to retrieve all the booking items for a given booking

### HTTP Request

`GET http://staging.gojourny.com/api/v3/bookings/<BOOKING_ID>/booking_options/<BOOKING_OPTION_ID>/booking_items/>`

### Query Parameters

Parameter | Description
--------- | -------
BOOKING_ID | The booking id
BOOKING_OPTION | The booking option id

```json
[
  {
    "id": "2f6d2db7-034c-423a-8c95-dc34385a3029",
    "name": "Custom Name for booking",
    "description": "description",
    "bookable_id": "",
    "bookable_type": "",
    "start_date": "2021-03-15 15:00 PM",
    "end_date": "2021-03-20 11:00 AM",
    "people_count": "2",
    "booking_option_id": "237ffb97-6d6b-4575-ac56-ce5002841712",
    "taxes": "10000.0",
    "commission": "10.0",
    "gross_price": "160000.0",
    "net_price": "150000.0",
    "markup": null,
    "total_price": "182500.0",
    "vendor_rate_id": "XXX",
    "currency": "EUR",
    "confirmation_id": "XXX"
}
]
```

## show

Allows the user to retrieve a specific booking item

### HTTP Request

`GET http://staging.gojourny.com/api/v3/bookings/<BOOKING_ID>/booking_options/<BOOKING_OPTION_ID>/booking_items/<BOOKING_ITEM_ID>`

### Query Parameters

Parameter | Description
--------- | -------
BOOKING_ID | The booking id
BOOKING_OPTION | The booking option id
BOOKING_ITEM_ID | The booking item id

> The above command returns JSON structured like this:

```json
{
    "id": "2f6d2db7-034c-423a-8c95-dc34385a3029",
    "name": "Custom Name for booking",
    "description": "description",
    "bookable_id": "",
    "bookable_type": "",
    "start_date": "2021-03-15 15:00 PM",
    "end_date": "2021-03-20 11:00 AM",
    "people_count": "2",
    "booking_option_id": "237ffb97-6d6b-4575-ac56-ce5002841712",
    "taxes": "10000.0",
    "commission": "10.0",
    "gross_price": "160000.0",
    "net_price": "150000.0",
    "markup": null,
    "total_price": "182500.0",
    "vendor_rate_id": "XXX",
    "currency": "EUR",
    "confirmation_id": "XXX"
}
```

## Create

Allows the user to create a booking item

### HTTP Request

`POST http://staging.gojourny.com/api/v3/bookings/<BOOKING_ID>/booking_options/<BOOKING_OPTION_ID>/booking_items/`

### Query Parameters

Parameter | Description
--------- | -------
BOOKING_ID | The booking id
BOOKING_OPTION | The booking option id

### Body Parameters

Parameter | Description
----------|-------------
booking['name'] | The name in case there is no bookable object to associat the booking item with
booking['description'] | The description of the bookable item if needed
booking['bookable_id'] | The bookable id (hotel id or room id)
booking['bookable_type'] |  The bookable type (The class, like: Room or tour)
booking['booking_option_id'] | The booking option id associated
booking['start_date'] | The start datetime `YYYY-MM-DD hh:mmm`
booking['end_date'] | The end datetime `YYYY-MM-DD hh:mmm`
booking['people_count'] | The people count or units
booking['gross_price'] | The gross price
booking['net_price'] | The net price
booking['taxes'] | The consolidated taxes amount
booking['source'] | Source
booking['commission'] | Our commission
booking['markup'] | The markup when there is no commission set
booking['total_price'] | The consolidated price
booking['vendor_rate_id'] | The vendor rate id if any, for example for hotel beds
booking['confirmation_id'] | The confirmation id returned by the api if present
booking['currency'] | They currency in ISO 4217 code
booking['payment_id'] | The associated payment id

> The above command returns JSON structured like this:

```json
{
    "id": "2f6d2db7-034c-423a-8c95-dc34385a3029",
    "name": "Custom Name for booking",
    "description": "description",
    "bookable_id": "",
    "bookable_type": "",
    "start_date": "2021-03-15 15:00 PM",
    "end_date": "2021-03-20 11:00 AM",
    "people_count": "2",
    "booking_option_id": "237ffb97-6d6b-4575-ac56-ce5002841712",
    "taxes": "10000.0",
    "commission": "10.0",
    "gross_price": "160000.0",
    "net_price": "150000.0",
    "markup": null,
    "total_price": "182500.0",
    "vendor_rate_id": "XXX",
    "currency": "EUR",
    "confirmation_id": "XXX"
}
```

## Update

Allows the user to update a booking item

### HTTP Request

`PUT http://staging.gojourny.com/api/v3/bookings/<BOOKING_ID>/booking_options/<BOOKING_OPTION_ID>/booking_items/<BOOKING_ITEM_ID>`

### Query Parameters

Parameter | Description
--------- | -------
BOOKING_ID | The booking id
BOOKING_OPTION | The booking option id
BOOKING_ITEM_ID | The booking item id

### Body Parameters

Parameter | Description
----------|-------------
booking['name'] | The name in case there is no bookable object to associat the booking item with
booking['description'] | The description of the bookable item if needed
booking['bookable_id'] | The bookable id (hotel id or room id)
booking['bookable_type'] |  The bookable type (The class, like: Room or tour)
booking['booking_option_id'] | The booking option id associated
booking['start_date'] | The start datetime `YYYY-MM-DD hh:mmm`
booking['end_date'] | The end datetime `YYYY-MM-DD hh:mmm`
booking['people_count'] | The people count or units
booking['gross_price'] | The gross price
booking['net_price'] | The net price
booking['taxes'] | The consolidated taxes amount
booking['source'] | Source
booking['commission'] | Our commission
booking['markup'] | The markup when there is no commission set
booking['total_price'] | The consolidated price
booking['vendor_rate_id'] | The vendor rate id if any, for example for hotel beds
booking['confirmation_id'] | The confirmation id returned by the api if present
booking['currency'] | They currency in ISO 4217 code
booking['payment_id'] | The associated payment id

> The above command returns JSON structured like this:

```json
{
    "id": "2f6d2db7-034c-423a-8c95-dc34385a3029",
    "name": "Custom Name for booking",
    "description": "description",
    "bookable_id": "",
    "bookable_type": "",
    "start_date": "2021-03-15 15:00 PM",
    "end_date": "2021-03-20 11:00 AM",
    "people_count": "2",
    "booking_option_id": "237ffb97-6d6b-4575-ac56-ce5002841712",
    "taxes": "10000.0",
    "commission": "10.0",
    "gross_price": "160000.0",
    "net_price": "150000.0",
    "markup": null,
    "total_price": "182500.0",
    "vendor_rate_id": "XXX",
    "currency": "EUR",
    "confirmation_id": "XXX"
}
```

## Destroy

Allows the user to delete a booking item

### HTTP Request

`DELETE http://staging.gojourny.com/api/v3/bookings/<BOOKING_ID>/booking_options/<BOOKING_OPTION_ID>/booking_items/<BOOKING_ITEM_ID>`

Parameter | Description
--------- | -------
BOOKING_ID | The booking id
BOOKING_OPTION | The booking option id
BOOKING_ITEM_ID | The booking item id

> The above command returns JSON structured like this:

```json
{
    "id": "2f6d2db7-034c-423a-8c95-dc34385a3029",
    "name": "Custom Name for booking",
    "description": "description",
    "bookable_id": "",
    "bookable_type": "",
    "start_date": "2021-03-15 15:00 PM",
    "end_date": "2021-03-20 11:00 AM",
    "people_count": "2",
    "booking_option_id": "237ffb97-6d6b-4575-ac56-ce5002841712",
    "taxes": "10000.0",
    "commission": "10.0",
    "gross_price": "160000.0",
    "net_price": "150000.0",
    "markup": null,
    "total_price": "182500.0",
    "vendor_rate_id": "XXX",
    "currency": "EUR",
    "confirmation_id": "XXX"
}
```
