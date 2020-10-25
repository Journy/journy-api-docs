# LocationItems

## Show

Allows the user to retrieve a Location Item

### HTTP Request

`GET http://staging.gojourny.com/api/v3/itinerary/<ITINERARY_ID>/location_items/<LOCATION_ID>?full_location=<FULL>`

### Query Parameters

Parameter | Description
--------- | -------
ITINERARY_ID | The itinerary id
LOCATION_ID | The location id
FULL | You can pass a boolean variable to retrieve the base or full location details

> The above command returns JSON structured like this:

```json
{
    "location_items": {
        "842456": {
            "id": 842456,
            "name": "Roman Forum",
            "description": "Capri description",
            "location_id": 12170,
            "full_data": false,
            "display_title": "Walk through history in the Roman Forum",
            "description_short": "The Roman Forum — located between Piazza Venezia and the Colosseum — is one of the most interesting archaeological sites in the world. Although it was meant to become the social and political center of the Roman Empire, it became submerged in marshland, was then uncovered, and finally assumed its role as a bonafide social hub by the end of the seventh century. Today, there’s plenty to see at the Forum complex, including the forum’s oldest Christian church, the last Republican basilica, and more. For the most direct route, enter directly from the Palatino and let history take you away. ",
            "note": null,
            "image": "https://assets.gojourny.com/uploads/images/attachments/79b9cad5-dedb-4aad-b9e6-243f1388f467.jpg",
            "type": "activity",
            "latitude": "41.8924623",
            "longitude": "12.485325",
            "row_order_position": 0,
            "itinerary_id": 16458,
            "section_id": 837419,
            "slot_id": 837421,
            "group_id": null,
            "estimated_time_to_spend": "3600"
        }
    }
}
```

## Create

Allows the user to create a Day Item

### HTTP Request

`POST http://staging.gojourny.com/api/v3/itinerary/<ITINERARY_ID>/location_items?full_location=<FULL>`

### Query Parameters

Parameter | Description
--------- | -------
ITINERARY_ID | The itinerary id
FULL | You can pass a boolean variable to retrieve the base or full location details

### Body Parameters

Parameter | Description
----------|-------------
location_item['section_id'] | The day_item id or additional_item id
location_item['slot_id'] | The slot_id to which this location item belongs (should be null for additional options)
location_item['slot'] | The slot slug to which this location item belongs (should be null for additional options), temporary to keep backwards compatibility
location_item['group_id'] | The group id if you want to add this to group block
location_item['location_id'] | The location_id
location_item['reservation_id'] | The reservation id
location_item['note'] | A note on this item
location_item['row_order_position'] | The day_item position as an integer value (persisted but not in used yet, day items are still sorted by date)

> The above command returns JSON structured like this:

```json
{
    "location_items": {
        "842456": {
            "id": 842456,
            "name": "Roman Forum",
            "description": "Capri description",
            "location_id": 12170,
            "full_data": false,
            "display_title": "Walk through history in the Roman Forum",
            "description_short": "The Roman Forum — located between Piazza Venezia and the Colosseum — is one of the most interesting archaeological sites in the world. Although it was meant to become the social and political center of the Roman Empire, it became submerged in marshland, was then uncovered, and finally assumed its role as a bonafide social hub by the end of the seventh century. Today, there’s plenty to see at the Forum complex, including the forum’s oldest Christian church, the last Republican basilica, and more. For the most direct route, enter directly from the Palatino and let history take you away. ",
            "note": null,
            "image": "https://assets.gojourny.com/uploads/images/attachments/79b9cad5-dedb-4aad-b9e6-243f1388f467.jpg",
            "type": "activity",
            "latitude": "41.8924623",
            "longitude": "12.485325",
            "row_order_position": 0,
            "itinerary_id": 16458,
            "section_id": 837419,
            "slot_id": 837421,
            "group_id": null,
            "estimated_time_to_spend": "3600"
        }
    }
}
```

## Update

Allows the user to create a Day Item

### HTTP Request

`PUT http://staging.gojourny.com/api/v3/itinerary/<ITINERARY_ID>/location_items?full_location=<FULL>`

### Query Parameters

Parameter | Description
--------- | -------
ITINERARY_ID | The itinerary id
FULL | You can pass a boolean variable to retrieve the base or full location details

### Body Parameters

Parameter | Description
----------|-------------
location_item['section_id'] | The day_item id or additional_item id
location_item['slot_id'] | The slot_id to which this location item belongs (should be null for additional options)
location_item['slot'] | The slot slug to which this location item belongs (should be null for additional options), temporary to keep backwards compatibility
location_item['group_id'] | The group id if you want to add this to group block
location_item['location_id'] | The location_id
location_item['reservation_id'] | The reservation id
location_item['note'] | A note on this item
location_item['row_order_position'] | The day_item position as an integer value (persisted but not in used yet, day items are still sorted by date)

> The above command returns JSON structured like this:

```json
{
    "location_items": {
        "842456": {
            "id": 842456,
            "name": "Roman Forum",
            "description": "Capri description",
            "location_id": 12170,
            "full_data": false,
            "display_title": "Walk through history in the Roman Forum",
            "description_short": "The Roman Forum — located between Piazza Venezia and the Colosseum — is one of the most interesting archaeological sites in the world. Although it was meant to become the social and political center of the Roman Empire, it became submerged in marshland, was then uncovered, and finally assumed its role as a bonafide social hub by the end of the seventh century. Today, there’s plenty to see at the Forum complex, including the forum’s oldest Christian church, the last Republican basilica, and more. For the most direct route, enter directly from the Palatino and let history take you away. ",
            "note": null,
            "image": "https://assets.gojourny.com/uploads/images/attachments/79b9cad5-dedb-4aad-b9e6-243f1388f467.jpg",
            "type": "activity",
            "latitude": "41.8924623",
            "longitude": "12.485325",
            "row_order_position": 0,
            "itinerary_id": 16458,
            "section_id": 837419,
            "slot_id": 837421,
            "group_id": null,
            "estimated_time_to_spend": "3600"
        }
    }
}
```

## DELETE

Allows the user to destroy a Location Item, it does not destroy the underlaying location.

### HTTP Request

`GET http://staging.gojourny.com/api/v3/itinerary/<ITINERARY_ID>/location_items/<LOCATION_ID>`

### Query Parameters

Parameter | Description
--------- | -------
ITINERARY_ID | The itinerary id
LOCATION_ID | The location_id

> The above command returns JSON structured like this:

```json
{}
```
