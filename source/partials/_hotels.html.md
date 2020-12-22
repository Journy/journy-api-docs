
# Hotels

## show

Allows the user to retrieve a specific hotel

### HTTP Request

`GET http://staging.gojourny.com/api/v3/hotels/<HOTEL_ID>`

### Query Parameters

Parameter | Description
--------- | -------
HOTEL_ID | The hotel id

> The above command returns JSON structured like this:

```json
{
   "id":"d6ff06a8-b49c-48a8-96a4-d1663cae742d",
   "name":"Hotel Parisianer",
   "distance_from_city_center":null,
   "number_of_rooms":null,
   "class_rating":"",
   "affiliation":"",
   "need_to_know":"",
   "direct":"",
   "check_in":null,
   "check_out":null,
   "amenities":[
      {
         "name":"Free Wi-Fi",
         "slug":"free-wi-fi"
      }
   ],
   "rooms":[
      {
         "resource_type":"room",
         "id":"a0dee9e2-19e8-48de-a4b5-66225d5bfac2"
      },
      {
         "resource_type":"room",
         "id":"4bad8718-0574-4695-80c1-5fad47753300"
      },
      {
         "resource_type":"room",
         "id":"51b76105-11b8-4b23-82f7-7aa18ff91cf1"
      },
      {
         "resource_type":"room",
         "id":"3ec8dd28-cf93-4221-b3b4-7a59f9299595"
      }
   ]
}
```

## Create

Allows the user to create a Hotel

### HTTP Request

`POST http://staging.gojourny.com/api/v3/hotels/`

### Body Parameters

Parameter | Description
----------|-------------
hotel['id'] | The hotel id
hotel['short_description'] | The hotel short_description
hotel['long_description'] | The hotel long_description
hotel['check_in'] | The hotel check in time (Format: HH:MM:SS 24hs, ie: 17:00:00)
hotel['check_out'] | The hotel check out time (Format: HH:MM:SS 24hs, ie: 17:00:00)
hotel['distance_from_city_center'] | Distance from the city center in km
hotel['location_id'] | The location id associated with the hotel
hotel['class_rating'] | The hotel stars
hotel['affiliation'] | The chain the hotel belongs to
hotel['need_to_know'] | Relevant information to the customer

> The above command returns JSON structured like this:

```json
{
   "id":"d6ff06a8-b49c-48a8-96a4-d1663cae742d",
   "name":"Hotel Parisianer",
   "distance_from_city_center":null,
   "number_of_rooms":null,
   "class_rating":"",
   "affiliation":"",
   "need_to_know":"",
   "direct":"",
   "check_in":null,
   "check_out":null,
   "amenities":[
      {
         "name":"Free Wi-Fi",
         "slug":"free-wi-fi"
      }
   ],
   "rooms":[
      {
         "resource_type":"room",
         "id":"a0dee9e2-19e8-48de-a4b5-66225d5bfac2"
      },
      {
         "resource_type":"room",
         "id":"4bad8718-0574-4695-80c1-5fad47753300"
      },
      {
         "resource_type":"room",
         "id":"51b76105-11b8-4b23-82f7-7aa18ff91cf1"
      },
      {
         "resource_type":"room",
         "id":"3ec8dd28-cf93-4221-b3b4-7a59f9299595"
      }
   ]
}
```

## Update

Allows the user to update a Hotel

### HTTP Request

`PUT http://staging.gojourny.com/api/v3/hotels/<HOTEL_ID>`

Parameter | Description
--------- | -------
HOTEL_ID | The hotel id

### Body Parameters

Parameter | Description
----------|-------------
hotel['id'] | The hotel id
hotel['short_description'] | The hotel short_description
hotel['long_description'] | The hotel long_description
hotel['check_in'] | The hotel check in time (Format: HH:MM:SS 24hs, ie: 17:00:00)
hotel['check_out'] | The hotel check out time (Format: HH:MM:SS 24hs, ie: 17:00:00)
hotel['distance_from_city_center'] | Distance from the city center in km
hotel['location_id'] | The location id associated with the hotel
hotel['class_rating'] | The hotel stars
hotel['affiliation'] | The chain the hotel belongs to
hotel['need_to_know'] | Relevant information to the customer

> The above command returns JSON structured like this:

```json
{
   "id":"d6ff06a8-b49c-48a8-96a4-d1663cae742d",
   "name":"Hotel Parisianer",
   "distance_from_city_center":null,
   "number_of_rooms":null,
   "class_rating":"",
   "affiliation":"",
   "need_to_know":"",
   "direct":"",
   "check_in":null,
   "check_out":null,
   "amenities":[
      {
         "name":"Free Wi-Fi",
         "slug":"free-wi-fi"
      }
   ],
   "rooms":[
      {
         "resource_type":"room",
         "id":"a0dee9e2-19e8-48de-a4b5-66225d5bfac2"
      },
      {
         "resource_type":"room",
         "id":"4bad8718-0574-4695-80c1-5fad47753300"
      },
      {
         "resource_type":"room",
         "id":"51b76105-11b8-4b23-82f7-7aa18ff91cf1"
      },
      {
         "resource_type":"room",
         "id":"3ec8dd28-cf93-4221-b3b4-7a59f9299595"
      }
   ]
}
```

## Destroy

Allows the user to delete the Hotel, this will also delete all the associated rooms, beds associations and api connections

### HTTP Request

`DELETE http://staging.gojourny.com/api/v3/hotels/<HOTEL_ID>`

Parameter | Description
--------- | -------
HOTEL_ID | The hotel id

> The above command returns JSON structured like this:

```json
{
   "id":"d6ff06a8-b49c-48a8-96a4-d1663cae742d",
   "name":"Hotel Parisianer",
   "distance_from_city_center":null,
   "number_of_rooms":null,
   "class_rating":"",
   "affiliation":"",
   "need_to_know":"",
   "direct":"",
   "check_in":null,
   "check_out":null,
   "amenities":[
      {
         "name":"Free Wi-Fi",
         "slug":"free-wi-fi"
      }
   ],
   "rooms":[
      {
         "resource_type":"room",
         "id":"a0dee9e2-19e8-48de-a4b5-66225d5bfac2"
      },
      {
         "resource_type":"room",
         "id":"4bad8718-0574-4695-80c1-5fad47753300"
      },
      {
         "resource_type":"room",
         "id":"51b76105-11b8-4b23-82f7-7aa18ff91cf1"
      },
      {
         "resource_type":"room",
         "id":"3ec8dd28-cf93-4221-b3b4-7a59f9299595"
      }
   ]
}
```
