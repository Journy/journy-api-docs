
# AdditionalOptionItems

## Show

### HTTP Request

`GET http://staging.gojourny.com/api/v3/itinerary/<ITINERARY_ID>/additional_option_items/<ADDITIONAL_OPTION_ITEM>`

### Query Parameters

Parameter | Description
--------- | -------
ITINERARY_ID | The Itinerary ID
ADDITIONAL_OPTION_ITEM | The date item ID

> The above command returns JSON structured like this:

```json
{
    "additional_option_items": {
        "848063": {
            "id": 848063,
            "name": "Dining & Drinks",
            "note": null,
            "trip_section_id": null,
            "row_order_position": 0,
            "description": null,
            "itinerary_id": "58Dy",
            "location_items": [
                {
                    "resource_type": "location_item",
                    "id": 848291
                },
                {
                    "resource_type": "location_item",
                    "id": 848269
                },
                {
                    "resource_type": "location_item",
                    "id": 848271
                },
                {
                    "resource_type": "location_item",
                    "id": 848094
                },
                {
                    "resource_type": "location_item",
                    "id": 848103
                },
                {
                    "resource_type": "location_item",
                    "id": 848081
                },
                {
                    "resource_type": "location_item",
                    "id": 848079
                },
                {
                    "resource_type": "location_item",
                    "id": 848101
                },
                {
                    "resource_type": "location_item",
                    "id": 848080
                },
                {
                    "resource_type": "location_item",
                    "id": 848100
                }
            ]
        }
    }
}
```

## Create

Allows the user to create a Additional Option Item

### HTTP Request

`POST http://staging.gojourny.com/api/v3/itinerary/<ITINERARY_ID>/additional_option_items`

### Query Parameters

Parameter | Description
--------- | -------
ITINERARY_ID | The itinerary id

### Body Parameters

Parameter | Description
----------|-------------
additional_otpion_item['name'] | The item name
additional_otpion_item['description'] | The item description
additional_otpion_item['trip_section_id'] | The item trip_section_id
additional_otpion_item['row_order_position'] | The item position as an integer value

> The above command returns JSON structured like this:

```json
{
    "additional_option_items": {
        "848063": {
            "id": 848063,
            "name": "Dining & Drinks",
            "note": null,
            "trip_section_id": null,
            "row_order_position": 0,
            "description": null,
            "itinerary_id": "58Dy",
            "location_items": [
                {
                    "resource_type": "location_item",
                    "id": 848291
                },
                {
                    "resource_type": "location_item",
                    "id": 848269
                },
                {
                    "resource_type": "location_item",
                    "id": 848271
                },
                {
                    "resource_type": "location_item",
                    "id": 848094
                },
                {
                    "resource_type": "location_item",
                    "id": 848103
                },
                {
                    "resource_type": "location_item",
                    "id": 848081
                },
                {
                    "resource_type": "location_item",
                    "id": 848079
                },
                {
                    "resource_type": "location_item",
                    "id": 848101
                },
                {
                    "resource_type": "location_item",
                    "id": 848080
                },
                {
                    "resource_type": "location_item",
                    "id": 848100
                }
            ]
        }
    }
}
```

## Update

Allows the user to edit a Additional Option Item

### HTTP Request

`PUT http://staging.gojourny.com/api/v3/itinerary/<ITINERARY_ID>/additional_option_items/<ADDITIONAL_OPTION_ITEM>`

### Query Parameters

Parameter | Description
--------- | -------
ITINERARY_ID | The Itinerary ID
ADDITIONAL_OPTION_ITEM | The date item ID

### Body Parameters

Parameter | Description
----------|-------------
additional_otpion_item['name'] | The item name
additional_otpion_item['description'] | The item description
additional_otpion_item['trip_section_id'] | The item trip_section_id
additional_otpion_item['row_order_position'] | The item position as an integer value

> The above command returns JSON structured like this:

```json
{
    "additional_option_items": {
        "842457": {
            "id": 842457,
            "date": "2020-04-08",
            "name": "Day 1",
            "accommodation_items": [],
            "slots": [
                {
                    "name": "breakfast",
                    "items": []
                },
                {
                    "name": "morning_activities",
                    "items": []
                },
                {
                    "name": "lunch",
                    "items": []
                },
                {
                    "name": "afternoon_activites",
                    "items": []
                },
                {
                    "name": "dinner",
                    "items": []
                },
                {
                    "name": "nighttime",
                    "items": []
                },
                {
                    "name": "lodging",
                    "items": []
                }
            ]
        }
    },
    "accommodation_items": {},
    "location_items": {},
    "group_items": {},
    "reservations": {}
}
```

## Delete

Allows the user to destroy a Additional Option Item, this change cascades and also destroys all nested items.

### HTTP Request

`DELETE http://staging.gojourny.com/api/v3/itinerary/<ITINERARY_ID>/additional_option_items/<ADDITIONAL_OPTION_ITEM>`

### Query Parameters

Parameter | Description
--------- | -------
ITINERARY_ID | The Itinerary ID
ADDITIONAL_OPTION_ITEM | The date item ID

> The above command returns JSON structured like this:

```json
{}
```
