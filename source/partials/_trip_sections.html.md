
# TripSections

## Show

Allows the user to edit any field on the trip section

### HTTP Request

`GET http://staging.gojourny.com/api/v3/itinerary/<ITINERARY_ID>/trip_sections/<TRIP_SECTION_ID>`

### Query Parameters

Parameter | Description
--------- | -------
ITINERARY_ID | The itinerary id.
TRIP_SECTION_ID | The trip section id.

> The above command returns JSON structured like this:

```json
{
    "trip_sections": {
        "ed2e58fb-7b25-443d-929e-1b7758a72e3b": {
            "id": "ed2e58fb-7b25-443d-929e-1b7758a72e3b",
            "destination_id": 296,
            "start_date": null,
            "end_date": null,
            "package_id": null,
            "row_order_position": 0,
            "description": "New Trip Section Description",
            "itinerary_id": "pZq2",
            "days": [],
            "transit_items": [],
            "destination": {
                "id": 296,
                "display_title": "Capri",
                "description": null,
                "use_desktop_photo": false,
                "use_mobile_photo": false,
                "desktop_photo_url": null,
                "mobile_photo_url": null,
                "latitude": "40.5532009",
                "longitude": "14.222154"
            }
        }
    }
}
```

## Create

Allows the user to created a Trip Section

### HTTP Request

`POST http://staging.gojourny.com/api/v3/itinerary/<ITINERARY_ID>/trip_sections`

### Query Parameters

Parameter | Description
--------- | -------
ITINERARY_ID | The itinerary id

### Body Parameters

Parameter | Description
----------|-------------
trip_section['name'] | The trip_section name
trip_section['description'] | The trip_section description, supports rich text
trip_section['destination_id'] | The destination_id
trip_section['section_type'] | If its a regular or optional trip section
trip_section['package_id'] | The package id if it belongs to a package
trip_section['row_order_position'] | The trip section position as an integer value

> The above command returns JSON structured like this:

```json
{
    "trip_sections": {
        "ed2e58fb-7b25-443d-929e-1b7758a72e3b": {
            "id": "ed2e58fb-7b25-443d-929e-1b7758a72e3b",
            "destination_id": 296,
            "start_date": null,
            "end_date": null,
            "package_id": null,
            "row_order_position": 0,
            "description": "New Trip Section Description",
            "itinerary_id": "pZq2",
            "days": [],
            "transit_items": [],
            "destination": {
                "id": 296,
                "display_title": "Capri",
                "description": null,
                "use_desktop_photo": false,
                "use_mobile_photo": false,
                "desktop_photo_url": null,
                "mobile_photo_url": null,
                "latitude": "40.5532009",
                "longitude": "14.222154"
            }
        }
    }
}
```

## Update

Allows the user to edit any field on the trip section

### HTTP Request

`PUT http://staging.gojourny.com/api/v3/itinerary/<ITINERARY_ID>/trip_sections/<TRIP_SECTION_ID>`

### Query Parameters

Parameter | Description
--------- | -------
ITINERARY_ID | The itinerary id.
TRIP_SECTION_ID | The trip section id.

### Body Parameters

Parameter | Description
----------|-------------
trip_section['name'] | The trip_section name
trip_section['description'] | The trip_section description, supports rich text
trip_section['destination_id'] | The destination_id
trip_section['section_type'] | If its a regular or optional trip section
trip_section['package_id'] | The package id if it belongs to a package
trip_section['row_order_position'] | The trip section position as an integer value

> The above command returns JSON structured like this:

```json
{
    "trip_sections": {
        "ed2e58fb-7b25-443d-929e-1b7758a72e3b": {
            "id": "ed2e58fb-7b25-443d-929e-1b7758a72e3b",
            "destination_id": 296,
            "start_date": null,
            "end_date": null,
            "package_id": null,
            "row_order_position": 0,
            "description": "New Trip Section Description",
            "itinerary_id": "pZq2",
            "days": [],
            "transit_items": [],
            "destination": {
                "id": 296,
                "display_title": "Capri",
                "description": null,
                "use_desktop_photo": false,
                "use_mobile_photo": false,
                "desktop_photo_url": null,
                "mobile_photo_url": null,
                "latitude": "40.5532009",
                "longitude": "14.222154"
            }
        }
    }
}
```

## Delete

Destroys the trip sections, this delete cascades and deletes all nested items (Days, Locations, etc)

### HTTP Request

`DELETE http://staging.gojourny.com/api/v3/itinerary/<ITINERARY_ID>/trip_sections/<TRIP_SECTION_ID>`

### Query Parameters

Parameter | Description
--------- | -------
ITINERARY_ID | The itinerary id.
TRIP_SECTION_ID | The trip section id.

> The above command returns JSON structured like this:

```json
{}
```
