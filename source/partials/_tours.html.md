
# Tours

## show

Allows the user to retrieve a specific tour

### HTTP Request

`GET http://staging.gojourny.com/api/v3/tours/<TOUR_ID>`

### Query Parameters

Parameter | Description
--------- | -------
TOUR_ID | The tour id

> The above command returns JSON structured like this:

```json
{
   "id":"83de064a-c1c6-43fb-9cf3-1f441ce50de0",
   "name":"Paris: Eiffel Tower Summit with Lunch and Seine Cruise",
   "accessibility":"",
   "tour_type":"small_groups",
   "category":"Architecture",
   "duration":"4 hour",
   "pickup_details":"",
   "languages":"en, ar, es, nl, zh, fr, de, it, ja, pl, pt, ru",
   "max_participants":null,
   "age_restrictions":"",
   "meeting_point_latitude":"48.8583698",
   "meeting_point_longitude":"2.2944833",
   "meeting_point_description":"",
   "price_type":"adult",
   "price_per_group":null,
   "price_per_adult":"15762.0",
   "price_per_child":"15762.0",
   "child_age":null,
   "available_days":[
      "sunday",
      "wednesday"
   ],
   "start_times":[
      "900",
      "4500",
      "3600"
   ],
   "short_description":"<div>Experience a trip up the Eiffel Tower and enjoy the exceptional panoramic views. When you feel hungry, go to Le Bistro Parisien to enjoy your delicious lunch with a river view. Later, complete the journey with an iconic Seine River cruise.</div>",
   "long_description":"<div>Experience a trip up the Eiffel Tower and enjoy the exceptional panoramic views. When you feel hungry, go to Le Bistro Parisien to enjoy your delicious lunch with a river view. Later, complete the journey with an iconic Seine River cruise.</div>",
   "exclusions":"",
   "inclusions":"",
   "important_information":"",
   "highlights":"",
   "tours_locations":[
      {
         "resource_type":"tours_location",
         "id":"f4dc7efc-8bde-40cb-b8cf-d2e4485e5994"
      }
   ],
   "api_connections":[
      {
         "resource_type":"api_connection",
         "id":"4fd6506b-b21c-4c99-b148-0cb1e39da8f9"
      }
   ]
}
```

## Create

Allows the user to update a Tour

### HTTP Request

`POST http://staging.gojourny.com/api/v3/tours/<TOUR_ID>`

Parameter | Description
--------- | -------
TOUR_ID | The tour id

### Body Parameters

Parameter | Description
----------|-------------
tour['id'] | The tour id
tour['name'] | The tour name
tour['accessibility'] | Accessibility info
tour['max_participants'] | Max participants
tour['short_description'] | Short description
tour['long_description'] | Long description
tour['highlights'] | The tour highlights
tour['tour_type'] | Tour types, could be: `small_groups`, `large_groups`, `private`
tour['category'] | The tour category, historical, adventure, architecture, etc
tour['duration'] | The tour duration as string
tour['pickup_details'] | Pick up details
tour['languages'] | An array of the tour available languages, ie: `['en', 'fr', 'pt']`
tour['important_information'] | Relevant information
tour['inclusions'] | What is included
tour['exclusions'] | What is not included
tour['age_restrictions'] | String: Age restrictions
tour['meeting_point_latitude'] | Meeting point latitude
tour['meeting_point_longitude'] | Meeting point longitude
tour['meeting_point_description'] | Meeting point escription
tour['price_per_child'] | Price per child in cents
tour['price_per_adult'] | Price per adult in cents
tour['price_per_group'] | Price per group in cents
tour['child_age'] | The maximum age stablished to consider a person child
tour['price_type'] | Price type, available options: `group`,  `adult_child`, `adult`
tour['available_days'] | Array of days
tour['start_times'] | Array of times in minutes, for example: [3600, 7200] is equivalent to [01:00 am, 02:00 am]
tour['tours_locations_attributes'] | An array of the locations associations, containing the `location_id` and `id` of the association. An existing association can be marked for destruction setting the `_delete` attribute to true.

> The above command returns JSON structured like this:

```json
{
   "id":"83de064a-c1c6-43fb-9cf3-1f441ce50de0",
   "name":"Paris: Eiffel Tower Summit with Lunch and Seine Cruise",
   "accessibility":"",
   "tour_type":"small_groups",
   "category":"Architecture",
   "duration":"4 hour",
   "pickup_details":"",
   "languages":"en, ar, es, nl, zh, fr, de, it, ja, pl, pt, ru",
   "max_participants":null,
   "age_restrictions":"",
   "meeting_point_latitude":"48.8583698",
   "meeting_point_longitude":"2.2944833",
   "meeting_point_description":"",
   "price_type":"adult",
   "price_per_group":null,
   "price_per_adult":"15762.0",
   "price_per_child":"15762.0",
   "child_age":null,
   "available_days":[
      "sunday",
      "wednesday"
   ],
   "start_times":[
      "900",
      "4500",
      "3600"
   ],
   "short_description":"<div>Experience a trip up the Eiffel Tower and enjoy the exceptional panoramic views. When you feel hungry, go to Le Bistro Parisien to enjoy your delicious lunch with a river view. Later, complete the journey with an iconic Seine River cruise.</div>",
   "long_description":"<div>Experience a trip up the Eiffel Tower and enjoy the exceptional panoramic views. When you feel hungry, go to Le Bistro Parisien to enjoy your delicious lunch with a river view. Later, complete the journey with an iconic Seine River cruise.</div>",
   "exclusions":"",
   "inclusions":"",
   "important_information":"",
   "highlights":"",
   "tours_locations":[
      {
         "resource_type":"tours_location",
         "id":"f4dc7efc-8bde-40cb-b8cf-d2e4485e5994"
      }
   ],
   "api_connections":[
      {
         "resource_type":"api_connection",
         "id":"4fd6506b-b21c-4c99-b148-0cb1e39da8f9"
      }
   ]
}
```

## Update

Allows the user to update a Tour

### HTTP Request

`PUT http://staging.gojourny.com/api/v3/tours/<TOUR_ID>`

Parameter | Description
--------- | -------
TOUR_ID | The tour id

### Body Parameters

Parameter | Description
----------|-------------
tour['id'] | The tour id
tour['name'] | The tour name
tour['accessibility'] | Accessibility info
tour['max_participants'] | Max participants
tour['short_description'] | Short description
tour['long_description'] | Long description
tour['highlights'] | The tour highlights
tour['tour_type'] | Tour types, could be: `small_groups`, `large_groups`, `private`
tour['category'] | The tour category, historical, adventure, architecture, etc
tour['duration'] | The tour duration as string
tour['pickup_details'] | Pick up details
tour['languages'] | An array of the tour available languages, ie: `['en', 'fr', 'pt']`
tour['important_information'] | Relevant information
tour['inclusions'] | What is included
tour['exclusions'] | What is not included
tour['age_restrictions'] | String: Age restrictions
tour['meeting_point_latitude'] | Meeting point latitude
tour['meeting_point_longitude'] | Meeting point longitude
tour['meeting_point_description'] | Meeting point escription
tour['price_per_child'] | Price per child in cents
tour['price_per_adult'] | Price per adult in cents
tour['price_per_group'] | Price per group in cents
tour['child_age'] | The maximum age stablished to consider a person child
tour['price_type'] | Price type, available options: `group`,  `adult_child`, `adult`
tour['available_days'] | Array of days
tour['start_times'] | Array of times in minutes, for example: [3600, 7200] is equivalent to [01:00 am, 02:00 am]
tour['tours_locations_attributes'] | An array of the locations associations, containing the `location_id` and `id` of the association. An existing association can be marked for destruction setting the `_delete` attribute to true.

> The above command returns JSON structured like this:

```json
{
   "id":"83de064a-c1c6-43fb-9cf3-1f441ce50de0",
   "name":"Paris: Eiffel Tower Summit with Lunch and Seine Cruise",
   "accessibility":"",
   "tour_type":"small_groups",
   "category":"Architecture",
   "duration":"4 hour",
   "pickup_details":"",
   "languages":"en, ar, es, nl, zh, fr, de, it, ja, pl, pt, ru",
   "max_participants":null,
   "age_restrictions":"",
   "meeting_point_latitude":"48.8583698",
   "meeting_point_longitude":"2.2944833",
   "meeting_point_description":"",
   "price_type":"adult",
   "price_per_group":null,
   "price_per_adult":"15762.0",
   "price_per_child":"15762.0",
   "child_age":null,
   "available_days":[
      "sunday",
      "wednesday"
   ],
   "start_times":[
      "900",
      "4500",
      "3600"
   ],
   "short_description":"<div>Experience a trip up the Eiffel Tower and enjoy the exceptional panoramic views. When you feel hungry, go to Le Bistro Parisien to enjoy your delicious lunch with a river view. Later, complete the journey with an iconic Seine River cruise.</div>",
   "long_description":"<div>Experience a trip up the Eiffel Tower and enjoy the exceptional panoramic views. When you feel hungry, go to Le Bistro Parisien to enjoy your delicious lunch with a river view. Later, complete the journey with an iconic Seine River cruise.</div>",
   "exclusions":"",
   "inclusions":"",
   "important_information":"",
   "highlights":"",
   "tours_locations":[
      {
         "resource_type":"tours_location",
         "id":"f4dc7efc-8bde-40cb-b8cf-d2e4485e5994"
      }
   ],
   "api_connections":[
      {
         "resource_type":"api_connection",
         "id":"4fd6506b-b21c-4c99-b148-0cb1e39da8f9"
      }
   ]
}
```

## Destroy

Allows the user to delete the Tour, this will also delete all api connections

### HTTP Request

`DELETE http://staging.gojourny.com/api/v3/tour/<TOUR_ID>`

Parameter | Description
--------- | -------
TOUR_ID | The tour id

> The above command returns JSON structured like this:

```json
{
   "id":"83de064a-c1c6-43fb-9cf3-1f441ce50de0",
   "name":"Paris: Eiffel Tower Summit with Lunch and Seine Cruise",
   "accessibility":"",
   "tour_type":"small_groups",
   "category":"Architecture",
   "duration":"4 hour",
   "pickup_details":"",
   "languages":"en, ar, es, nl, zh, fr, de, it, ja, pl, pt, ru",
   "max_participants":null,
   "age_restrictions":"",
   "meeting_point_latitude":"48.8583698",
   "meeting_point_longitude":"2.2944833",
   "meeting_point_description":"",
   "price_type":"adult",
   "price_per_group":null,
   "price_per_adult":"15762.0",
   "price_per_child":"15762.0",
   "child_age":null,
   "available_days":[
      "sunday",
      "wednesday"
   ],
   "start_times":[
      "900",
      "4500",
      "3600"
   ],
   "short_description":"<div>Experience a trip up the Eiffel Tower and enjoy the exceptional panoramic views. When you feel hungry, go to Le Bistro Parisien to enjoy your delicious lunch with a river view. Later, complete the journey with an iconic Seine River cruise.</div>",
   "long_description":"<div>Experience a trip up the Eiffel Tower and enjoy the exceptional panoramic views. When you feel hungry, go to Le Bistro Parisien to enjoy your delicious lunch with a river view. Later, complete the journey with an iconic Seine River cruise.</div>",
   "exclusions":"",
   "inclusions":"",
   "important_information":"",
   "highlights":"",
   "tours_locations":[
      {
         "resource_type":"tours_location",
         "id":"f4dc7efc-8bde-40cb-b8cf-d2e4485e5994"
      }
   ],
   "api_connections":[
      {
         "resource_type":"api_connection",
         "id":"4fd6506b-b21c-4c99-b148-0cb1e39da8f9"
      }
   ]
}
```


