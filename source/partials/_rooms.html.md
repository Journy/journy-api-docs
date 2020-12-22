
# Rooms

## show

Allows the user to retrieve a specific hotel

### HTTP Request

`GET http://staging.gojourny.com/api/v3/hotels/<HOTEL_ID>/rooms/<ROOM_ID>`

### Query Parameters

Parameter | Description
--------- | -------
ROOM_ID | The room id

> The above command returns JSON structured like this:

```json
{
    "id": "4bad8718-0574-4695-80c1-5fad47753300",
    "name": "DOUBLE CLASSIC PARK VIEW",
    "square_footage": 100.0,
    "view": "",
    "min_people": 1,
    "max_people": 2,
    "max_occupancy_adults": 2,
    "max_occupancy_kids": 1,
    "amenities": [],
    "beds": [
        {
            "name": "Double bed",
            "size": "large",
            "slug": "double-bed"
        }
    ]
}
```

## Create

Allows the user to create a Hotel

### HTTP Request

`POST http://staging.gojourny.com/api/v3/hotels/<HOTEL_ID>/rooms/`

### Body Parameters

Parameter | Description
----------|-------------
room['id'] | The room id
room['name'] | The room name
room['square_footage'] | The room square footage
room['view'] | The view orientation
room['min_people'] | The max party size
room['max_people'] | The min party size
room['max_occupancy_adults'] | The max allowed adults
room['max_occupancy_kids'] | The max allowed kids
room['rooms_amenities_attributes'] | An array composed by `id`, `amenity_id` to associate the amenity. It can be marked for desturction setting the `_destroy` attribute to `true`, this will only destroy the association.
room['rooms_beds_attributes'] | An array composed by `id`, `bed_id` to associate the bed. It can be marked for desturction setting the `_destroy` attribute to `true`, this will only destroy the association.

> The above command returns JSON structured like this:

```json
{
    "id": "4bad8718-0574-4695-80c1-5fad47753300",
    "name": "DOUBLE CLASSIC PARK VIEW",
    "square_footage": 100.0,
    "view": "",
    "min_people": 1,
    "max_people": 2,
    "max_occupancy_adults": 2,
    "max_occupancy_kids": 1,
    "amenities": [],
    "beds": [
        {
            "name": "Double bed",
            "size": "large",
            "slug": "double-bed"
        }
    ]
}
```

## Update

Allows the user to update a Hotel

### HTTP Request

`PUT http://staging.gojourny.com/api/v3/hotels/<HOTEL_ID>/rooms/<ROOM_ID>`

Parameter | Description
--------- | -------
ROOM_ID | The room id

### Body Parameters

Parameter | Description
----------|-------------
room['id'] | The room id
room['name'] | The room name
room['square_footage'] | The room square footage
room['view'] | The view orientation
room['min_people'] | The max party size
room['max_people'] | The min party size
room['max_occupancy_adults'] | The max allowed adults
room['max_occupancy_kids'] | The max allowed kids
room['rooms_amenities_attributes'] | An array composed by `id`, `amenity_id` to associate the amenity. It can be marked for desturction setting the `_destroy` attribute to `true`, this will only destroy the association.
room['rooms_beds_attributes'] | An array composed by `id`, `bed_id` to associate the bed. It can be marked for desturction setting the `_destroy` attribute to `true`, this will only destroy the association.


> The above command returns JSON structured like this:

```json
{
    "id": "4bad8718-0574-4695-80c1-5fad47753300",
    "name": "DOUBLE CLASSIC PARK VIEW",
    "square_footage": 100.0,
    "view": "",
    "min_people": 1,
    "max_people": 2,
    "max_occupancy_adults": 2,
    "max_occupancy_kids": 1,
    "amenities": [],
    "beds": [
        {
            "name": "Double bed",
            "size": "large",
            "slug": "double-bed"
        }
    ]
}
```

## Destroy

Allows the user to delete the Hotel, this will also delete all the associated rooms, beds associations and api connections

### HTTP Request

`DELETE http://staging.gojourny.com/api/v3/hotels/<HOTEL_ID>/rooms/<ROOM_ID>`

Parameter | Description
--------- | -------
ROOM_ID | The room id

> The above command returns JSON structured like this:

```json
{
    "id": "4bad8718-0574-4695-80c1-5fad47753300",
    "name": "DOUBLE CLASSIC PARK VIEW",
    "square_footage": 100.0,
    "view": "",
    "min_people": 1,
    "max_people": 2,
    "max_occupancy_adults": 2,
    "max_occupancy_kids": 1,
    "amenities": [],
    "beds": [
        {
            "name": "Double bed",
            "size": "large",
            "slug": "double-bed"
        }
    ]
}
```
