
# DayItems

## Create

Allows the user to create a Day Item

### HTTP Request

`POST http://staging.gojourny.com/api/v3/itinerary/<ITINERARY_ID>/day_items`

### Query Parameters

Parameter | Description
--------- | -------
ITINERARY_ID | The itinerary id

### Body Parameters

Parameter | Description
----------|-------------
day_item['date'] | The day_item date as `YYYY-MM-DD`
day_item['description'] | The day_item description
day_item['trip_section_id'] | The day_item trip_section_id
day_item['row_order_position'] | The day_item position as an integer value (persisted but not in used yet, day items are still sorted by date)

> The above command returns JSON structured like this:

```json
{
    "day_items": {
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

## Show

### HTTP Request

`GET http://staging.gojourny.com/api/v3/itinerary/<ITINERARY_ID>/day_items/<DAY_ITEM_ID>`

### Query Parameters

Parameter | Description
--------- | -------
ITINERARY_ID | The Itinerary ID
DAY_ITEM_ID | The date item ID

> The above command returns JSON structured like this:

```json
{
    "day_items": {
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

## Update

Allows the user to edit a Day Item

### HTTP Request

`PUT http://staging.gojourny.com/api/v3/itinerary/<ITINERARY_ID>/day_items/<DAY_ITEM_ID>`

### Query Parameters

Parameter | Description
--------- | -------
ITINERARY_ID | The Itinerary ID
DAY_ITEM_ID | The date item ID

### Body Parameters

Parameter | Description
----------|-------------
day_item['date'] | The day_item date as `YYYY-MM-DD`
day_item['description'] | The day_item description
day_item['trip_section_id'] | The day_item trip_section_id
day_item['row_order_position'] | The day_item position as an integer value (persisted but not in used yet, day items are still sorted by date)

> The above command returns JSON structured like this:

```json
{
    "day_items": {
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

Allows the user to destroy a Day Item, this change cascades and also destroys all nested items.

### HTTP Request

`DELETE http://staging.gojourny.com/api/v3/itinerary/<ITINERARY_ID>/day_items/<DAY_ITEM_ID>`

### Query Parameters

Parameter | Description
--------- | -------
ITINERARY_ID | The Itinerary ID
DAY_ITEM_ID | The date item ID

> The above command returns JSON structured like this:

```json
{}
```
