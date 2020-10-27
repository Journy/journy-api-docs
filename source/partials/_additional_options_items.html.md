
# AdditionalOptionItems
## Index

### HTTP Request

`GET http://staging.gojourny.com/api/v3/itineraries/<ITINERARY_ID>/additional_option_items/>`

### Query Parameters

Parameter | Description
--------- | -------
ITINERARY_ID | The Itinerary ID

> The above command returns JSON structured like this:

```json
{
    "additional_option_items": {
        "848063": {
            "id": 848063,
            "name": "Dining & Drinks ",
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
        },
        "848064": {
            "id": 848064,
            "name": "Activities ",
            "note": null,
            "trip_section_id": null,
            "row_order_position": 1,
            "description": null,
            "itinerary_id": "58Dy",
            "location_items": [
                {
                    "resource_type": "location_item",
                    "id": 848096
                },
                {
                    "resource_type": "location_item",
                    "id": 848089
                },
                {
                    "resource_type": "location_item",
                    "id": 848088
                },
                {
                    "resource_type": "location_item",
                    "id": 848091
                },
                {
                    "resource_type": "location_item",
                    "id": 848084
                }
            ]
        },
        "848619": {
            "id": 848619,
            "name": "name of the additional_option_item",
            "note": "note",
            "trip_section_id": null,
            "row_order_position": 2,
            "description": "test",
            "itinerary_id": "58Dy",
            "location_items": []
        }
    }
}
```
## Show

### HTTP Request

`GET http://staging.gojourny.com/api/v3/itineraries/<ITINERARY_ID>/additional_option_items/<ADDITIONAL_OPTION_ITEM>`

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
            "name": "Dining & Drinks ",
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
    },
    "location_items": {
        "848080": {
            "id": 848080,
            "name": null,
            "description": null,
            "location_id": 29645,
            "full_data": false,
            "display_title": "Cochinita Pibil (Mayan pork) at the No-frills Taqueria El Paisa (Breakfast Only)",
            "description_short": null,
            "note": null,
            "image": "/uploads/images/d78e30f4-b15e-40f7-8d63-2fe2a000709f.jpg",
            "type": "restaurant",
            "latitude": "20.211262",
            "longitude": "-87.458028",
            "row_order_position": 5,
            "itinerary_id": 16563,
            "section_id": 848063,
            "slot_id": null,
            "group_id": null,
            "estimated_time_to_spend": "1800",
            "reservations": {}
        },
        "848094": {
            "id": 848094,
            "name": "Clan-Destino",
            "description": null,
            "location_id": 69895,
            "full_data": false,
            "display_title": "Drinks at Tulum's only cenote bar, Clan-Destino",
            "description_short": "",
            "note": null,
            "image": "/uploads/images/f5180398-256c-4c54-b4a3-dd9a493cb4c6.jpg",
            "type": "night_time",
            "latitude": "20.1536882",
            "longitude": "-87.45790719999999",
            "row_order_position": 3,
            "itinerary_id": 16563,
            "section_id": 848063,
            "slot_id": null,
            "group_id": null,
            "estimated_time_to_spend": "5400",
            "reservations": {}
        },
        "848100": {
            "id": 848100,
            "name": null,
            "description": null,
            "location_id": 40560,
            "full_data": false,
            "display_title": "Cocktails in the jungle vibes at Wild",
            "description_short": null,
            "note": null,
            "image": "/uploads/images/38bac640-0c1b-433a-acd8-804409ebb9d7.png",
            "type": "night_time",
            "latitude": "20.1351321",
            "longitude": "-87.46427039999999",
            "row_order_position": 0,
            "itinerary_id": 16563,
            "section_id": 848063,
            "slot_id": null,
            "group_id": null,
            "estimated_time_to_spend": "2700",
            "reservations": {}
        },
        "848079": {
            "id": 848079,
            "name": null,
            "description": null,
            "location_id": 9502,
            "full_data": false,
            "display_title": "Fresh no-frills seafood at El Camello Jr.",
            "description_short": "Always bustling with locals and tourists alike, El Camello is the place to go for fabulously fresh, no-frills seafood. Heaping plates of ceviche explode with fruity, spicy, and tangy flavors, while filets of caught-that-day fish are cooked to fall right off the bone and melt into your mouth. You won’t find a place that combines such extraordinary seafood with such a casual, fun atmosphere anywhere else.",
            "note": null,
            "image": "/uploads/images/b9c3ae1a-48bb-492c-8213-4b7ee559eaa7.jpg",
            "type": "restaurant",
            "latitude": "20.208062",
            "longitude": "-87.4714888",
            "row_order_position": 0,
            "itinerary_id": 16563,
            "section_id": 848063,
            "slot_id": null,
            "group_id": null,
            "estimated_time_to_spend": "5400",
            "reservations": {}
        },
        "848101": {
            "id": 848101,
            "name": null,
            "description": null,
            "location_id": 23615,
            "full_data": false,
            "display_title": "Contemporary Baja Mexican Cuisine & Impressive Cocktails at Mur Mur",
            "description_short": null,
            "note": null,
            "image": "/uploads/images/fafc086b-0a0d-433d-8bcb-b829719d3fd9.jpg",
            "type": "restaurant",
            "latitude": "20.1499807",
            "longitude": "-87.459138",
            "row_order_position": 1,
            "itinerary_id": 16563,
            "section_id": 848063,
            "slot_id": null,
            "group_id": null,
            "estimated_time_to_spend": "5400",
            "reservations": {
                "resource_type": "reservations",
                "id": 38427
            }
        },
        "848269": {
            "id": 848269,
            "name": null,
            "description": null,
            "location_id": 20268,
            "full_data": false,
            "display_title": "8-peso Tacos from Tacos de Canasta (go early)",
            "description_short": null,
            "note": null,
            "image": "/uploads/images/00a78c9c-60d3-4f72-aa58-b43b238f604b.jpg",
            "type": "restaurant",
            "latitude": "20.2103731",
            "longitude": "-87.4577071",
            "row_order_position": 1,
            "itinerary_id": 16563,
            "section_id": 848063,
            "slot_id": null,
            "group_id": null,
            "estimated_time_to_spend": "1800",
            "reservations": {}
        },
        "848103": {
            "id": 848103,
            "name": "Posada Margherita",
            "description": null,
            "location_id": 9483,
            "full_data": false,
            "display_title": "Tulum's most beloved Italian cuisine at Posada Margherita ",
            "description_short": "<div>Run by two Italians, this restaurant combines the extraordinary freshness of Tulum’s seafood with the inimitable freshness of hand-rolled pasta in casual, beachside surrounds. The meal starts with a selection of fresh breads and cheeses, priming you before you indulge in pastas sauced with light renditions of shrimp, mussels, and octopus. Close your eyes as you experience the natural flavors and listen to the lapping waves, if only to make sure you’re not dreaming.&nbsp;<br><br>Tucked inside the Posada Margherita, Loltulum is a cozy beach boutique displaying nifty, soft styles that will have you looking beach-chic and ready for the sun. An emphasis on tropical colors and casual, subtle design helps these dresses, bathing suits, and tops stand out as some of Tulum’s most sought after pieces for visiting fashionistas.</div>",
            "note": null,
            "image": "/uploads/images/ba71701e-efbe-40aa-9390-2fa56cdee417.jpg",
            "type": "restaurant",
            "latitude": "20.16492629999999",
            "longitude": "-87.4524301",
            "row_order_position": 0,
            "itinerary_id": 16563,
            "section_id": 848063,
            "slot_id": null,
            "group_id": null,
            "estimated_time_to_spend": "5400",
            "reservations": {}
        },
        "848291": {
            "id": 848291,
            "name": null,
            "description": null,
            "location_id": 9507,
            "full_data": false,
            "display_title": "Spa & Cocktails by the beach at Hotel Be Tulum",
            "description_short": null,
            "note": null,
            "image": "/uploads/images/c8dfd240-eaa8-468d-8320-77ef551fdf4b.jpg",
            "type": "restaurant",
            "latitude": "20.13716",
            "longitude": "-87.463381",
            "row_order_position": 0,
            "itinerary_id": 16563,
            "section_id": 848063,
            "slot_id": null,
            "group_id": null,
            "estimated_time_to_spend": "5400",
            "reservations": {}
        },
        "848081": {
            "id": 848081,
            "name": null,
            "description": null,
            "location_id": 28658,
            "full_data": false,
            "display_title": "Grab Mayan breakfast with locals at Don Cafeto",
            "description_short": null,
            "note": null,
            "image": "/uploads/images/65740d13-ce0c-455c-9121-729b92511e08.jpg",
            "type": "restaurant",
            "latitude": "20.2116956",
            "longitude": "-87.4603807",
            "row_order_position": 4,
            "itinerary_id": 16563,
            "section_id": 848063,
            "slot_id": null,
            "group_id": null,
            "estimated_time_to_spend": "3600",
            "reservations": {}
        },
        "848271": {
            "id": 848271,
            "name": "La Malquerida",
            "description": null,
            "location_id": 40542,
            "full_data": false,
            "display_title": "Gluten-Free and Veggie Friendly Eats at La Malquerida",
            "description_short": "",
            "note": null,
            "image": "/uploads/images/70927105-2763-47de-8e13-47fba5f6a78f.jpg",
            "type": "restaurant",
            "latitude": "20.2118821",
            "longitude": "-87.4594706",
            "row_order_position": 2,
            "itinerary_id": 16563,
            "section_id": 848063,
            "slot_id": null,
            "group_id": null,
            "estimated_time_to_spend": "5400",
            "reservations": {}
        }
    }
}
```

## Create

Allows the user to create a Additional Option Item

### HTTP Request

`POST http://staging.gojourny.com/api/v3/itineraries/<ITINERARY_ID>/additional_option_items`

### Query Parameters

Parameter | Description
--------- | -------
ITINERARY_ID | The itinerary id

### Body Parameters

Parameter | Description
----------|-------------
additional_option_item['name'] | The item name
additional_option_item['description'] | The item description
additional_option_item['trip_section_id'] | The item trip_section_id
additional_option_item['row_order_position'] | The item position as an integer value

> The above command returns JSON structured like this:

```json
{
    "additional_option_items": {
        "848619": {
            "id": 848619,
            "name": "name of the additional_option_item",
            "note": "note",
            "trip_section_id": null,
            "row_order_position": 2,
            "description": "test",
            "itinerary_id": "58Dy",
            "location_items": []
        }
    },
    "location_items": {}
}
```

## Update

Allows the user to edit a Additional Option Item

### HTTP Request

`PUT http://staging.gojourny.com/api/v3/itineraries/<ITINERARY_ID>/additional_option_items/<ADDITIONAL_OPTION_ITEM>`

### Query Parameters

Parameter | Description
--------- | -------
ITINERARY_ID | The Itinerary ID
ADDITIONAL_OPTION_ITEM | The date item ID

### Body Parameters

Parameter | Description
----------|-------------
additional_option_item['name'] | The item name
additional_option_item['description'] | The item description
additional_option_item['trip_section_id'] | The item trip_section_id
additional_option_item['row_order_position'] | The item position as an integer value

> The above command returns JSON structured like this:

```json
{
    "additional_option_items": {
        "848063": {
            "id": 848063,
            "name": "Dining & Drinks",
            "note": "note",
            "trip_section_id": null,
            "row_order_position": 0,
            "description": "test",
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
    },
    "location_items": {
        "848080": {
            "id": 848080,
            "name": null,
            "description": null,
            "location_id": 29645,
            "full_data": false,
            "display_title": "Cochinita Pibil (Mayan pork) at the No-frills Taqueria El Paisa (Breakfast Only)",
            "description_short": null,
            "note": null,
            "image": "/uploads/images/d78e30f4-b15e-40f7-8d63-2fe2a000709f.jpg",
            "type": "restaurant",
            "latitude": "20.211262",
            "longitude": "-87.458028",
            "row_order_position": 5,
            "itinerary_id": 16563,
            "section_id": 848063,
            "slot_id": null,
            "group_id": null,
            "estimated_time_to_spend": "1800",
            "reservations": {}
        },
        "848094": {
            "id": 848094,
            "name": "Clan-Destino",
            "description": null,
            "location_id": 69895,
            "full_data": false,
            "display_title": "Drinks at Tulum's only cenote bar, Clan-Destino",
            "description_short": "",
            "note": null,
            "image": "/uploads/images/f5180398-256c-4c54-b4a3-dd9a493cb4c6.jpg",
            "type": "night_time",
            "latitude": "20.1536882",
            "longitude": "-87.45790719999999",
            "row_order_position": 3,
            "itinerary_id": 16563,
            "section_id": 848063,
            "slot_id": null,
            "group_id": null,
            "estimated_time_to_spend": "5400",
            "reservations": {}
        },
        "848100": {
            "id": 848100,
            "name": null,
            "description": null,
            "location_id": 40560,
            "full_data": false,
            "display_title": "Cocktails in the jungle vibes at Wild",
            "description_short": null,
            "note": null,
            "image": "/uploads/images/38bac640-0c1b-433a-acd8-804409ebb9d7.png",
            "type": "night_time",
            "latitude": "20.1351321",
            "longitude": "-87.46427039999999",
            "row_order_position": 0,
            "itinerary_id": 16563,
            "section_id": 848063,
            "slot_id": null,
            "group_id": null,
            "estimated_time_to_spend": "2700",
            "reservations": {}
        },
        "848079": {
            "id": 848079,
            "name": null,
            "description": null,
            "location_id": 9502,
            "full_data": false,
            "display_title": "Fresh no-frills seafood at El Camello Jr.",
            "description_short": "Always bustling with locals and tourists alike, El Camello is the place to go for fabulously fresh, no-frills seafood. Heaping plates of ceviche explode with fruity, spicy, and tangy flavors, while filets of caught-that-day fish are cooked to fall right off the bone and melt into your mouth. You won’t find a place that combines such extraordinary seafood with such a casual, fun atmosphere anywhere else.",
            "note": null,
            "image": "/uploads/images/b9c3ae1a-48bb-492c-8213-4b7ee559eaa7.jpg",
            "type": "restaurant",
            "latitude": "20.208062",
            "longitude": "-87.4714888",
            "row_order_position": 0,
            "itinerary_id": 16563,
            "section_id": 848063,
            "slot_id": null,
            "group_id": null,
            "estimated_time_to_spend": "5400",
            "reservations": {}
        },
        "848101": {
            "id": 848101,
            "name": null,
            "description": null,
            "location_id": 23615,
            "full_data": false,
            "display_title": "Contemporary Baja Mexican Cuisine & Impressive Cocktails at Mur Mur",
            "description_short": null,
            "note": null,
            "image": "/uploads/images/fafc086b-0a0d-433d-8bcb-b829719d3fd9.jpg",
            "type": "restaurant",
            "latitude": "20.1499807",
            "longitude": "-87.459138",
            "row_order_position": 1,
            "itinerary_id": 16563,
            "section_id": 848063,
            "slot_id": null,
            "group_id": null,
            "estimated_time_to_spend": "5400",
            "reservations": {
                "resource_type": "reservations",
                "id": 38427
            }
        },
        "848269": {
            "id": 848269,
            "name": null,
            "description": null,
            "location_id": 20268,
            "full_data": false,
            "display_title": "8-peso Tacos from Tacos de Canasta (go early)",
            "description_short": null,
            "note": null,
            "image": "/uploads/images/00a78c9c-60d3-4f72-aa58-b43b238f604b.jpg",
            "type": "restaurant",
            "latitude": "20.2103731",
            "longitude": "-87.4577071",
            "row_order_position": 1,
            "itinerary_id": 16563,
            "section_id": 848063,
            "slot_id": null,
            "group_id": null,
            "estimated_time_to_spend": "1800",
            "reservations": {}
        },
        "848103": {
            "id": 848103,
            "name": "Posada Margherita",
            "description": null,
            "location_id": 9483,
            "full_data": false,
            "display_title": "Tulum's most beloved Italian cuisine at Posada Margherita ",
            "description_short": "<div>Run by two Italians, this restaurant combines the extraordinary freshness of Tulum’s seafood with the inimitable freshness of hand-rolled pasta in casual, beachside surrounds. The meal starts with a selection of fresh breads and cheeses, priming you before you indulge in pastas sauced with light renditions of shrimp, mussels, and octopus. Close your eyes as you experience the natural flavors and listen to the lapping waves, if only to make sure you’re not dreaming.&nbsp;<br><br>Tucked inside the Posada Margherita, Loltulum is a cozy beach boutique displaying nifty, soft styles that will have you looking beach-chic and ready for the sun. An emphasis on tropical colors and casual, subtle design helps these dresses, bathing suits, and tops stand out as some of Tulum’s most sought after pieces for visiting fashionistas.</div>",
            "note": null,
            "image": "/uploads/images/ba71701e-efbe-40aa-9390-2fa56cdee417.jpg",
            "type": "restaurant",
            "latitude": "20.16492629999999",
            "longitude": "-87.4524301",
            "row_order_position": 0,
            "itinerary_id": 16563,
            "section_id": 848063,
            "slot_id": null,
            "group_id": null,
            "estimated_time_to_spend": "5400",
            "reservations": {}
        },
        "848291": {
            "id": 848291,
            "name": null,
            "description": null,
            "location_id": 9507,
            "full_data": false,
            "display_title": "Spa & Cocktails by the beach at Hotel Be Tulum",
            "description_short": null,
            "note": null,
            "image": "/uploads/images/c8dfd240-eaa8-468d-8320-77ef551fdf4b.jpg",
            "type": "restaurant",
            "latitude": "20.13716",
            "longitude": "-87.463381",
            "row_order_position": 0,
            "itinerary_id": 16563,
            "section_id": 848063,
            "slot_id": null,
            "group_id": null,
            "estimated_time_to_spend": "5400",
            "reservations": {}
        },
        "848081": {
            "id": 848081,
            "name": null,
            "description": null,
            "location_id": 28658,
            "full_data": false,
            "display_title": "Grab Mayan breakfast with locals at Don Cafeto",
            "description_short": null,
            "note": null,
            "image": "/uploads/images/65740d13-ce0c-455c-9121-729b92511e08.jpg",
            "type": "restaurant",
            "latitude": "20.2116956",
            "longitude": "-87.4603807",
            "row_order_position": 4,
            "itinerary_id": 16563,
            "section_id": 848063,
            "slot_id": null,
            "group_id": null,
            "estimated_time_to_spend": "3600",
            "reservations": {}
        },
        "848271": {
            "id": 848271,
            "name": "La Malquerida",
            "description": null,
            "location_id": 40542,
            "full_data": false,
            "display_title": "Gluten-Free and Veggie Friendly Eats at La Malquerida",
            "description_short": "",
            "note": null,
            "image": "/uploads/images/70927105-2763-47de-8e13-47fba5f6a78f.jpg",
            "type": "restaurant",
            "latitude": "20.2118821",
            "longitude": "-87.4594706",
            "row_order_position": 2,
            "itinerary_id": 16563,
            "section_id": 848063,
            "slot_id": null,
            "group_id": null,
            "estimated_time_to_spend": "5400",
            "reservations": {}
        }
    }
}
```

## Delete

Allows the user to destroy a Additional Option Item, this change cascades and also destroys all nested items.

### HTTP Request

`DELETE http://staging.gojourny.com/api/v3/itineraries/<ITINERARY_ID>/additional_option_items/<ADDITIONAL_OPTION_ITEM>`

### Query Parameters

Parameter | Description
--------- | -------
ITINERARY_ID | The Itinerary ID
ADDITIONAL_OPTION_ITEM | The date item ID

> The above command returns JSON structured like this:

```json
{}
```
