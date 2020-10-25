
# Itineraries

## Get All Itineraries

```ruby
require 'net/http'

uri     = URI("https://staging.gojourny.com/api/v3/itineraries")
headers = {
    'Authorization'=>'Bearer exampleJournyToken',
    'Content-Type' =>'application/json',
    'Accept'=>'application/json'
}

http     = Net::HTTP.new(uri.host, uri.port)
request  = Net::HTTP::Get.new(uri.request_uri, headers)
response = http.request(request)
```

```python
import requests

url     = "https://staging.gojourny.com/api/v3/itineraries"
headers = {
    'Authorization': 'Bearer exampleJournyToken',
    'Content-Type': 'application/json',
    'Accept': 'application/json'
}

response = requests.get(url, headers=headers)
```

```shell
# With shell, you can just pass the correct header with each request
curl "https://staging.gojourny.com/api/v3/itineraries"
  -H "Authorization: Bearer exampleJournyToken"
```

```javascript
const url     = "https://staging.gojourny.com/api/v3/itineraries"
const headers = {
    'Authorization': 'Bearer exampleJournyToken',
    'Content-Type': 'application/json',
    'Accept': 'application/json'
}
const response = await fetch(url, {
    method: 'GET',
    headers: headers
})

return response.json();
```

> The above command returns JSON structured like this:

```json
{
  "itineraries": [
    {
      "id": 16397,
      "title": "Paris for Anon Strudlebauer",
      "display": "Paris for Anon Strudlebauer ( 16397 )"
    }
  ]
}
```

This endpoint retrieves all itineraries for your entity.

### HTTP Request

`GET https://staging.gojourny.com/api/v3/itineraries`

### Query Parameters

Parameter | Default | Description
--------- | ------- | -----------
page | 1 | Integer, used in combination with page_size
page_size | 50 | Integer, used to set array return size
sort_field | 'created_at' | String, which field to sort on
sort_order | 'desc' | 'desc' or 'asc'
title | | String, limits return to itineraries matching string in title
start_date_from | | Date, limits return to itineraries starting after date
start_date_to | | Date, limits return to itineraries starting before date
end_date_from | | Date, limits return to itineraries ending after date
end_date_to | | Date, limits return to itineraries starting before date
status | | Array, limits return to itineries with matching statuses

<aside class="success">
Remember — all requests need to carry the authentication token!
</aside>

## Get a Specific Itinerary

```ruby
require 'net/http'

uri     = URI("https://staging.gojourny.com/api/v3/itineraries/15700")
headers = {
    'Authorization'=>'Bearer exampleJournyToken',
    'Content-Type' =>'application/json',
    'Accept'=>'application/json'
}

http     = Net::HTTP.new(uri.host, uri.port)
request  = Net::HTTP::Get.new(uri.request_uri, headers)
response = http.request(request)
```

```python
import requests

url     = "https://staging.gojourny.com/api/v3/itineraries/15700"
headers = {
    'Authorization': 'Bearer exampleJournyToken',
    'Content-Type': 'application/json',
    'Accept': 'application/json'
}

response = requests.get(url, headers=headers)
```

```shell
# With shell, you can just pass the correct header with each request
curl "https://staging.gojourny.com/api/v3/itineraries/15700"
  -H "Authorization: Bearer exampleJournyToken"
```

```javascript
const url     = "https://staging.gojourny.com/api/v3/itineraries/15700"
const headers = {
    'Authorization': 'Bearer exampleJournyToken',
    'Content-Type': 'application/json',
    'Accept': 'application/json'
}
const response = await fetch(url, {
    method: 'GET',
    headers: headers
})

return response.json();
````
> The above command returns JSON structured like this:

```json
{
  "id": 15700,
  "title": "Japan for Larry",
  "user_id": 27215,
  "created_at": "2019-11-25T01:40:38.737Z",
  "updated_at": "2020-04-15T08:04:09.829Z",
  "request": {},
  "status": "nps_survey_sent",
  "assignee_id": 22295,
  "notes": "",
  "blockers": [],
  "travel_type": "chronological",
  "promotion_id": 1080,
  "sample": false,
  "opened_by_id": 6223,
  "opened_at": "2020-03-15T02:06:09.615Z",
  "multi_purchase": false,
  "checkout_description": null,
  "special_terms": null,
  "include_upsell": true,
  "purchase_price": null,
  "sequence_number": 0,
  "parent_id": null,
  "experience": false,
  "max_available": null,
  "total_purchase_count": 0,
  "total_people": 0,
  "travel_plan_id": null,
  "customer_request": false,
  "package_type": "Full",
  "package_change_type": "",
  "package_change_notes": "",
  "added_other_info": false,
  "itinerary_notes": "architecture, botanical gardens, boutique/artisan shops, not much alcohol and no red meat. ",
  "summary": "",
  "app_title": "",
  "payment_status": "paid",
  "package_id": null
}
```

This endpoint retrieves a specific itinerary.

### HTTP Request

`GET http://staging.gojourny.com/api/v3/itineraries/<ID>`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the itinerary to retrieve

## Update a Specific Itinerary

```ruby
require 'net/http'

uri     = URI("https://staging.gojourny.com/api/v3/itineraries/15700")
headers = {
    'Authorization': 'Bearer exampleJournyToken',
    'Content-Type': 'application/json',
    'Accept': 'application/json'
}
body = {
  title: 'This is a new title',
}

http     = Net::HTTP.new(uri.host, uri.port)
request  = Net::HTTP::Put.new(uri.request_uri, body, headers)
response = http.request(request)
```

```python
import requests

url     = "https://staging.gojourny.com/api/v3/itineraries/15700"
headers = {
    'Authorization': 'Bearer exampleJournyToken',
    'Content-Type': 'application/json',
    'Accept': 'application/json'
}
body = {
  "title": 'This is a new title',
}

response = requests.put(url, data=json.dumps(payload), headers=headers)
```

```shell
# With shell, you have to pass the correct header with each request
curl -X PUT \
     -H "Content-Type: application/json" \
     -H "Authorization: Bearer exampleJournyToken" \
     -d '{"title":"New shell title"}' \
     "https://staging.gojourny.com/api/v3/itineraries/15700"
```

```javascript
const url     = "https://staging.gojourny.com/api/v3/itineraries/15700"
const headers = {
    'Authorization': 'Bearer exampleJournyToken',
    'Content-Type': 'application/json',
    'Accept': 'application/json'
}

const data = {
  title: 'This is a new title',
}

const response = await fetch(url, {
    method: 'PUT',
    headers: headers,
    body: JSON.stringify(data)
})

return response.json();
````
> The above command returns JSON structured like this:

```json
{
  "id": 15700,
  "title": "This is a new title",
  "user_id": 27215,
  "created_at": "2019-11-25T01:40:38.737Z",
  "updated_at": "2020-04-15T08:04:09.829Z",
  "request": {},
  "status": "nps_survey_sent",
  "assignee_id": 22295,
  "notes": "",
  "blockers": [],
  "travel_type": "chronological",
  "promotion_id": 1080,
  "sample": false,
  "opened_by_id": 6223,
  "opened_at": "2020-03-15T02:06:09.615Z",
  "multi_purchase": false,
  "checkout_description": null,
  "special_terms": null,
  "include_upsell": true,
  "purchase_price": null,
  "sequence_number": 0,
  "parent_id": null,
  "experience": false,
  "max_available": null,
  "total_purchase_count": 0,
  "total_people": 0,
  "travel_plan_id": null,
  "customer_request": false,
  "package_type": "Full",
  "package_change_type": "",
  "package_change_notes": "",
  "added_other_info": false,
  "itinerary_notes": "architecture, botanical gardens, boutique/artisan shops, not much alcohol and no red meat. ",
  "summary": "",
  "app_title": "",
  "payment_status": "paid",
  "package_id": null
}
```

This endpoint retrieves a specific itinerary.

### HTTP Request

`PATCH http://staging.gojourny.com/api/v3/itineraries/<ID>`
`PUT http://staging.gojourny.com/api/v3/itineraries/<ID>`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the itinerary to retrieve


## Delete a Specific itinerary

```ruby
require 'net/http'

uri     = URI("https://staging.gojourny.com/api/v3/itineraries/15700")
headers = {
    'Authorization'=>'Bearer exampleJournyToken',
    'Content-Type' =>'application/json',
    'Accept'=>'application/json'
}

http     = Net::HTTP.new(uri.host, uri.port)
request  = Net::HTTP::Delete.new(uri.request_uri, headers)
response = http.request(request)
```

```python
import requests

url     = "https://staging.gojourny.com/api/v3/itineraries/15700"
headers = {
    'Authorization': 'Bearer exampleJournyToken',
    'Content-Type': 'application/json',
    'Accept': 'application/json'
}

response = requests.delete(url, headers=headers)
```

```shell
# With shell, you can just pass the correct header with each request
curl -X DELETE "https://staging.gojourny.com/api/v3/itineraries" \
  -H "Authorization: Bearer exampleJournyToken"
```

```javascript
const url     = "https://staging.gojourny.com/api/v3/itineraries/15700"
const headers = {
    'Authorization': 'Bearer exampleJournyToken',
    'Content-Type': 'application/json',
    'Accept': 'application/json'
}
const response = await fetch(url, {
    method: 'DELETE',
    headers: headers
})

return response.json();
````

> The above command returns JSON structured like this:

```json
{
  "id": 2,
  "status" : "deleted"
}
```

This endpoint deletes a specific itinerary.

### HTTP Request

`DELETE http://staging.gojourny.com/api/v3/itineraries/<ID>`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the itinerary to delete

## Get all trip sections

This endpoint retrieves all trip sections.

### HTTP Request

`GET http://staging.gojourny.com/api/v3/itineraries/<ID>/trip_sections`

```ruby
require 'Journy'

api = Journy::APIClient.authorize!('secret-token')
api.itineraries.get
```

```python
import Journy

api = Journy.authorize('secret-token')
api.itineraries.get()
```

```shell
curl "http://staging.gojourny.com/api/itineraries/:id/trip_sections"
  -H "Authorization: secret-token"
```

```javascript
const Journy = require('Journy');

let api = Journy.authorize('secret-token');
let itineraries = api.itineraries.get();
```

> The above command returns JSON structured like this:

```json
{
   "trip_sections":{
      "d92ff4b0-8d4c-4421-941e-08175e88bed7":{
         "id":"d92ff4b0-8d4c-4421-941e-08175e88bed7",
         "destination":{
            "id":846,
            "display_title":"Sacred Valley",
            "description":"The Sacred Valley is a window into traditional ways of life then and now. Small towns like Ollantaytambo, Urubamba, and Pisac feature markets with locally made textiles and ceramics, as well as restaurants celebrating local harvests and methods of preparation. As the heart of the former Incan Empire, archeological sites abound, providing glimpses into the mysterious rituals and practices of the ancient culture. Just passing through? The train ride through this swath of fertile farmland is one of the most spectacular in the world. ",
            "use_desktop_photo":true,
            "use_mobile_photo":false,
            "desktop_photo_url":"/Users/maurocampillo/journy/nexus/spec/support/uploads/destinations/846_desktop_photo.jpg?v=1593107365",
            "mobile_photo_url":null,
            "latitude":"-13.3328163",
            "longitude":"-72.0844649"
         },
         "start_date":"2020-08-20",
         "end_date":"2020-08-23",
         "days":[
            {
               "resource_type":"day_item",
               "id":840558
            },
            {
               "resource_type":"day_item",
               "id":840550
            },
            {
               "resource_type":"day_item",
               "id":840534
            }
         ],
         "transit_items":[

         ]
      },
      "ca4ca619-01d1-43f9-aeb2-acd0cf4d160d":{
         "id":"ca4ca619-01d1-43f9-aeb2-acd0cf4d160d",
         "destination":{
            "id":851,
            "display_title":"Lima",
            "description":"",
            "use_desktop_photo":true,
            "use_mobile_photo":true,
            "desktop_photo_url":"/Users/maurocampillo/journy/nexus/spec/support/uploads/destinations/851_desktop_photo.jpg?v=1587157503",
            "mobile_photo_url":"/Users/maurocampillo/journy/nexus/spec/support/uploads/destinations/851_mobile_photo.jpg?v=1587157503",
            "latitude":"-12.0463731",
            "longitude":"-77.042754"
         },
         "start_date":"2020-08-22",
         "end_date":"2020-08-22",
         "days":[
            {
               "resource_type":"day_item",
               "id":840542
            }
         ],
         "transit_items":[

         ]
      },
      "bd9ba573-dd9d-4b4c-b914-3bdd8a2d53b1":{
         "id":"bd9ba573-dd9d-4b4c-b914-3bdd8a2d53b1",
         "destination":{
            "id":736,
            "display_title":"Cusco",
            "description":"Situated 11,000 feet high in the Andes, Cusco is the former capital of the Incan Empire and now the gateway to the region’s notable archeology and geography. The charming town has become one of Peru’s top destinations in its own right, with colorful colonial architecture, bustling local markets, and historically significant ruins. An exceptional cup of coffee, or bar of chocolate, is never more than a couple of blocks away. \r\n",
            "use_desktop_photo":false,
            "use_mobile_photo":false,
            "desktop_photo_url":null,
            "mobile_photo_url":null,
            "latitude":"-13.53195",
            "longitude":"-71.9674626"
         },
         "start_date":"2020-08-26",
         "end_date":"2020-08-26",
         "days":[
            {
               "resource_type":"day_item",
               "id":840605
            }
         ],
         "transit_items":[

         ]
      },
      "a8d4adf4-0ba3-4825-9683-163f23818104":{
         "id":"a8d4adf4-0ba3-4825-9683-163f23818104",
         "destination":{
            "id":853,
            "display_title":"Machu Picchu",
            "description":"Nestled between the Andes and the Amazon, amid lush jungle landscapes and soaring mountain peaks, Machu Picchu would be notable for its stunning geography alone. Add to that one of humanity’s most significant architectural and artistic achievements, and you have a truly bucket list-worthy destination. The massive complex was built in the 15th century by the Incan Empire and spans 200 structures divided into a residential or urban sector and an agricultural sector. In one direction towers Machu Picchu Mountain, in the other, Huayna Picchu. The trek to get here — literally, for many travelers — is well worth it. ",
            "use_desktop_photo":false,
            "use_mobile_photo":false,
            "desktop_photo_url":null,
            "mobile_photo_url":null,
            "latitude":"-13.1631412",
            "longitude":"-72.5449629"
         },
         "start_date":"2020-08-24",
         "end_date":"2020-08-25",
         "days":[
            {
               "resource_type":"day_item",
               "id":840526
            },
            {
               "resource_type":"day_item",
               "id":840518
            }
         ],
         "transit_items":[

         ]
      }
   },
   "destinations":{
      "736":{
         "id":736,
         "display_title":"Cusco",
         "description":"Situated 11,000 feet high in the Andes, Cusco is the former capital of the Incan Empire and now the gateway to the region’s notable archeology and geography. The charming town has become one of Peru’s top destinations in its own right, with colorful colonial architecture, bustling local markets, and historically significant ruins. An exceptional cup of coffee, or bar of chocolate, is never more than a couple of blocks away. \r\n",
         "use_desktop_photo":false,
         "use_mobile_photo":false,
         "desktop_photo_url":null,
         "mobile_photo_url":null,
         "latitude":"-13.53195",
         "longitude":"-71.9674626"
      },
      "846":{
         "id":846,
         "display_title":"Sacred Valley",
         "description":"The Sacred Valley is a window into traditional ways of life then and now. Small towns like Ollantaytambo, Urubamba, and Pisac feature markets with locally made textiles and ceramics, as well as restaurants celebrating local harvests and methods of preparation. As the heart of the former Incan Empire, archeological sites abound, providing glimpses into the mysterious rituals and practices of the ancient culture. Just passing through? The train ride through this swath of fertile farmland is one of the most spectacular in the world. ",
         "use_desktop_photo":true,
         "use_mobile_photo":false,
         "desktop_photo_url":"/Users/maurocampillo/journy/nexus/spec/support/uploads/destinations/846_desktop_photo.jpg?v=1593107365",
         "mobile_photo_url":null,
         "latitude":"-13.3328163",
         "longitude":"-72.0844649"
      },
      "851":{
         "id":851,
         "display_title":"Lima",
         "description":"",
         "use_desktop_photo":true,
         "use_mobile_photo":true,
         "desktop_photo_url":"/Users/maurocampillo/journy/nexus/spec/support/uploads/destinations/851_desktop_photo.jpg?v=1587157503",
         "mobile_photo_url":"/Users/maurocampillo/journy/nexus/spec/support/uploads/destinations/851_mobile_photo.jpg?v=1587157503",
         "latitude":"-12.0463731",
         "longitude":"-77.042754"
      },
      "853":{
         "id":853,
         "display_title":"Machu Picchu",
         "description":"Nestled between the Andes and the Amazon, amid lush jungle landscapes and soaring mountain peaks, Machu Picchu would be notable for its stunning geography alone. Add to that one of humanity’s most significant architectural and artistic achievements, and you have a truly bucket list-worthy destination. The massive complex was built in the 15th century by the Incan Empire and spans 200 structures divided into a residential or urban sector and an agricultural sector. In one direction towers Machu Picchu Mountain, in the other, Huayna Picchu. The trek to get here — literally, for many travelers — is well worth it. ",
         "use_desktop_photo":false,
         "use_mobile_photo":false,
         "desktop_photo_url":null,
         "mobile_photo_url":null,
         "latitude":"-13.1631412",
         "longitude":"-72.5449629"
      }
   }
}
```
## Get a all day items

This endpoint retrieves all day items for a specific itinerary.

### HTTP Request

`GET http://staging.gojourny.com/api/v3/itineraries/<ITINERARY_ID>/day_items/<DAY_ITEM_ID>`

### URL Parameters

Parameter | Description
--------- | -----------
ITINERARY_ID | The ID of the itinerary to delete


```ruby
require 'Journy'

api = Journy::APIClient.authorize!('secret-token')
api.itineraries.get
```

```python
import Journy

api = Journy.authorize('secret-token')
api.itineraries.get()
```

```shell
curl "http://staging.gojourny.com/api/itineraries/:id/trip_sections"
  -H "Authorization: secret-token"
```

```javascript
const Journy = require('Journy');

let api = Journy.authorize('secret-token');
let itineraries = api.itineraries.get();
```

> The above command returns JSON structured like this:

```json

```ruby
require 'Journy'

api = Journy::APIClient.authorize!('secret-token')
api.itineraries.get
```

```python
import Journy

api = Journy.authorize('secret-token')
api.itineraries.get()
```

```shell
curl "http://staging.gojourny.com/api/itineraries/:id/trip_sections"
  -H "Authorization: secret-token"
```

```javascript
const Journy = require('Journy');

let api = Journy.authorize('secret-token');
let itineraries = api.itineraries.get();
```

> The above command returns JSON structured like this:

```json
{
    "day_items": {
        "580825": {
            "id": 580825,
            "date": "2020-03-27",
            "name": "Day 5",
            "accommodation_items": [
                {
                    "resource_type": "accommodation_item",
                    "id": 842445
                }
            ],
            "slots": [
                {
                    "name": "breakfast",
                    "items": [
                        {
                            "resource_type": "location_item",
                            "id": 586331
                        }
                    ]
                },
                {
                    "name": "morning_activities",
                    "items": [
                        {
                            "resource_type": "location_item",
                            "id": 586318
                        },
                        {
                            "resource_type": "location_item",
                            "id": 588564
                        },
                        {
                            "resource_type": "location_item",
                            "id": 586206
                        },
                        {
                            "resource_type": "location_item",
                            "id": 586333
                        },
                        {
                            "resource_type": "location_item",
                            "id": 586345
                        }
                    ]
                },
                {
                    "name": "lunch",
                    "items": [
                        {
                            "resource_type": "location_item",
                            "id": 586334
                        }
                    ]
                },
                {
                    "name": "afternoon_activites",
                    "items": [
                        {
                            "resource_type": "location_item",
                            "id": 588574
                        },
                        {
                            "resource_type": "location_item",
                            "id": 586372
                        },
                        {
                            "resource_type": "location_item",
                            "id": 586373
                        },
                        {
                            "resource_type": "location_item",
                            "id": 586374
                        },
                        {
                            "resource_type": "location_item",
                            "id": 586339
                        },
                        {
                            "resource_type": "location_item",
                            "id": 586375
                        },
                        {
                            "resource_type": "location_item",
                            "id": 586358
                        },
                        {
                            "resource_type": "location_item",
                            "id": 588537
                        },
                        {
                            "resource_type": "location_item",
                            "id": 586361
                        },
                        {
                            "resource_type": "location_item",
                            "id": 586357
                        }
                    ]
                },
                {
                    "name": "dinner",
                    "items": [
                        {
                            "resource_type": "location_item",
                            "id": 588566
                        }
                    ]
                },
                {
                    "name": "nighttime",
                    "items": [
                        {
                            "resource_type": "location_item",
                            "id": 588394
                        }
                    ]
                },
                {
                    "name": "lodging",
                    "items": [
                        {
                            "resource_type": "location_item",
                            "id": 586205
                        }
                    ]
                }
            ]
        }
    },
    "accommodation_items": {
        "842445": {
            "location_items": {
                "842445": {
                    "id": 842445,
                    "name": "The Tokyo Station Hotel",
                    "description": null,
                    "location_id": 18733,
                    "full_data": false,
                    "display_title": "Rest up at the Tokyo Station Hotel",
                    "description_short": "Set in a Renaissance-style building dating back to 1915, this upscale hotel is directly connected to Tokyo train station and 2 km from the Imperial Palace. \r\n\r\nAiry rooms with classic furnishings offer free Wi-Fi, flat-screen TVs and iPod docks, plus tea and coffeemakers. Chic, upgraded rooms feature chandeliers and plush fabrics; some have palace or station views. Suites, some of which are split-level, have separate lounges.\r\n\r\nA free breakfast buffet is served in an atrium lobby lounge. Other dining options include high-end French and Cantonese restaurants, an Italian eatery and a cozy cocktail bar. There's also a gym and an expansive spa.",
                    "note": null,
                    "image": "https://assets.gojourny.com/uploads/images/attachments/6f628c53-f0d6-4b5e-b73d-31fd14331fad.jpg",
                    "type": "lodging",
                    "latitude": "35.68125289999999",
                    "longitude": "139.7660004",
                    "row_order_position": 0,
                    "itinerary_id": 16237,
                    "section_id": 580825,
                    "slot_id": null,
                    "group_id": null,
                    "estimated_time_to_spend": "1800"
                }
            }
        }
    },
    "location_items": {
        "586331": {
            "location_items": {
                "586331": {
                    "id": 586331,
                    "name": "Ueshima Coffee Shop | Yaesu Underground Mall",
                    "description": null,
                    "location_id": 66519,
                    "full_data": false,
                    "display_title": "Grab breakfast and coffee for the train at Ueshima Coffee Shop | Yaesu Underground Mall",
                    "description_short": "",
                    "note": null,
                    "image": "https://assets.gojourny.com/uploads/images/attachments/6bc4a330-df46-4f26-83fb-80b38fa1ceee.jpeg",
                    "type": "cafe",
                    "latitude": "35.6790482",
                    "longitude": "139.7680455",
                    "row_order_position": 0,
                    "itinerary_id": 16237,
                    "section_id": 580825,
                    "slot_id": 610609,
                    "group_id": null,
                    "estimated_time_to_spend": "900"
                }
            }
        },
        "588574": {
            "location_items": {
                "588574": {
                    "id": 588574,
                    "name": "Yugen",
                    "description": null,
                    "location_id": 63267,
                    "full_data": false,
                    "display_title": "High-Quality Matcha in Modern Tea Room Yugen ",
                    "description_short": null,
                    "note": null,
                    "image": "https://assets.gojourny.com/uploads/images/attachments/c72c9dad-4b28-4a6b-bb4e-7aa8d821126a.jpeg",
                    "type": "cafe",
                    "latitude": "35.0014045",
                    "longitude": "135.7658035",
                    "row_order_position": 0,
                    "itinerary_id": 16237,
                    "section_id": 580825,
                    "slot_id": 610638,
                    "group_id": null,
                    "estimated_time_to_spend": "2700"
                }
            }
        },
        "586361": {
            "location_items": {
                "586361": {
                    "id": 586361,
                    "name": null,
                    "description": null,
                    "location_id": 26786,
                    "full_data": false,
                    "display_title": "Glimpse a Geisha Along Hanami-Koji Street, Gion District's Most Picturesque Area",
                    "description_short": null,
                    "note": null,
                    "image": "https://assets.gojourny.com/uploads/images/attachments/0522f277-6a22-4253-9fa1-19f0c8f9ea86.jpg",
                    "type": "activity",
                    "latitude": "35.002762",
                    "longitude": "135.774912",
                    "row_order_position": 8,
                    "itinerary_id": 16237,
                    "section_id": 580825,
                    "slot_id": 610638,
                    "group_id": null,
                    "estimated_time_to_spend": "900"
                }
            }
        },
        "588537": {
            "location_items": {
                "588537": {
                    "id": 588537,
                    "name": "Gion",
                    "description": null,
                    "location_id": 9345,
                    "full_data": false,
                    "display_title": "Explore the Streets of the Gion District",
                    "description_short": "Down by the Kamogawa river banks, you’ll find the Gion District: a fascinating mix of old and new Kyoto. One street is lit by teahouse lanterns, while tall buildings line the next. \r\n\r\nGion is famous as one of Kyoto’s geisha districts, so keep an eye out for kimonos in the crowd while you make your way to one of the many restaurants and teahouses.",
                    "note": null,
                    "image": "https://assets.gojourny.com/uploads/images/attachments/a85d2fc6-9dfe-4e18-ad98-1d7f3a312d03.jpg",
                    "type": "activity",
                    "latitude": "35.003776",
                    "longitude": "135.777132",
                    "row_order_position": 7,
                    "itinerary_id": 16237,
                    "section_id": 580825,
                    "slot_id": 610638,
                    "group_id": null,
                    "estimated_time_to_spend": "3600"
                }
            }
        },
        "588566": {
            "location_items": {
                "588566": {
                    "id": 588566,
                    "name": "Izuu ",
                    "description": null,
                    "location_id": 57027,
                    "full_data": false,
                    "display_title": "Kyoto-Style Pressed Sushi at Izuu ",
                    "description_short": null,
                    "note": null,
                    "image": "https://assets.gojourny.com/uploads/images/attachments/8b33e224-ae08-4f2c-9582-af358ee821b3.jpg",
                    "type": "restaurant",
                    "latitude": "35.0048407",
                    "longitude": "135.7745153",
                    "row_order_position": 0,
                    "itinerary_id": 16237,
                    "section_id": 580825,
                    "slot_id": 610656,
                    "group_id": null,
                    "estimated_time_to_spend": "3600"
                }
            }
        },
        "586205": {
            "location_items": {
                "586205": {
                    "id": 586205,
                    "name": "Toshiharu Ryokan",
                    "description": null,
                    "location_id": 40446,
                    "full_data": false,
                    "display_title": "Rest Up at Toshiharu Ryokan",
                    "description_short": "",
                    "note": null,
                    "image": "https://assets.gojourny.com/uploads/images/attachments/066da731-2518-485d-b36e-a39c61e2ad04.jpg",
                    "type": "lodging",
                    "latitude": "34.998421",
                    "longitude": "135.758695",
                    "row_order_position": 0,
                    "itinerary_id": 16237,
                    "section_id": 580825,
                    "slot_id": 610679,
                    "group_id": null,
                    "estimated_time_to_spend": "2700"
                }
            }
        },
        "586206": {
            "location_items": {
                "586206": {
                    "id": 586206,
                    "name": "Toshiharu Ryokan",
                    "description": null,
                    "location_id": 40446,
                    "full_data": false,
                    "display_title": "Rest Up at Toshiharu Ryokan",
                    "description_short": "",
                    "note": null,
                    "image": "https://assets.gojourny.com/uploads/images/attachments/066da731-2518-485d-b36e-a39c61e2ad04.jpg",
                    "type": "lodging",
                    "latitude": "34.998421",
                    "longitude": "135.758695",
                    "row_order_position": 2,
                    "itinerary_id": 16237,
                    "section_id": 580825,
                    "slot_id": 610617,
                    "group_id": null,
                    "estimated_time_to_spend": "2700"
                }
            }
        },
        "586339": {
            "location_items": {
                "586339": {
                    "id": 586339,
                    "name": "Ichihara Heibei Shoten ",
                    "description": null,
                    "location_id": 21617,
                    "full_data": false,
                    "display_title": "Handmade Chopsticks at Ichihara Heibei Shoten (市原平兵衛商店)",
                    "description_short": null,
                    "note": null,
                    "image": "https://assets.gojourny.com/uploads/images/attachments/f33f8f6e-c650-4592-89fe-a9f8d1ef4057.jpg",
                    "type": "shopping",
                    "latitude": "35.00294459999999",
                    "longitude": "135.7634184",
                    "row_order_position": 4,
                    "itinerary_id": 16237,
                    "section_id": 580825,
                    "slot_id": 610638,
                    "group_id": null,
                    "estimated_time_to_spend": "900"
                }
            }
        },
        "586373": {
            "location_items": {
                "586373": {
                    "id": 586373,
                    "name": null,
                    "description": null,
                    "location_id": 26803,
                    "full_data": false,
                    "display_title": "Walk Down the Picturesque Preserved Shopping Streets of Ninen-zaka Leading to Kiyomizudera",
                    "description_short": null,
                    "note": null,
                    "image": "https://assets.gojourny.com/uploads/images/attachments/6acb5227-0ae4-414b-91fa-21d79da08895.jpg",
                    "type": "activity",
                    "latitude": "34.998122",
                    "longitude": "135.7808431",
                    "row_order_position": 2,
                    "itinerary_id": 16237,
                    "section_id": 580825,
                    "slot_id": 610638,
                    "group_id": null,
                    "estimated_time_to_spend": "900"
                }
            }
        },
        "586357": {
            "location_items": {
                "586357": {
                    "id": 586357,
                    "name": "Maruyama Park",
                    "description": null,
                    "location_id": 26959,
                    "full_data": false,
                    "display_title": "Visit Maruyama Park, Kyoto's Most Popular Public Park (Especially for Cherry Blossom Parties)",
                    "description_short": null,
                    "note": null,
                    "image": "https://assets.gojourny.com/uploads/images/attachments/2cd9d85c-e9dd-4803-97b8-132c4b2a15a5.jpg",
                    "type": "activity",
                    "latitude": "35.00388030000001",
                    "longitude": "135.7809168",
                    "row_order_position": 9,
                    "itinerary_id": 16237,
                    "section_id": 580825,
                    "slot_id": 610638,
                    "group_id": null,
                    "estimated_time_to_spend": "3600"
                }
            }
        },
        "586358": {
            "location_items": {
                "586358": {
                    "id": 586358,
                    "name": "Yasaka Shrine ",
                    "description": null,
                    "location_id": 9349,
                    "full_data": false,
                    "display_title": "Stop and See the Lanterns at Yasaka Shrine",
                    "description_short": null,
                    "note": null,
                    "image": "https://assets.gojourny.com/uploads/images/attachments/b8c67c89-5959-48df-b2b4-a5bab9f5a680.jpg",
                    "type": "activity",
                    "latitude": "35.0036559",
                    "longitude": "135.7785534",
                    "row_order_position": 6,
                    "itinerary_id": 16237,
                    "section_id": 580825,
                    "slot_id": 610638,
                    "group_id": null,
                    "estimated_time_to_spend": "1800"
                }
            }
        },
        "586372": {
            "location_items": {
                "586372": {
                    "id": 586372,
                    "name": null,
                    "description": null,
                    "location_id": 26794,
                    "full_data": false,
                    "display_title": "See the Hokan-ji Temple / Yasaka Pagoda from Afar 法観寺",
                    "description_short": null,
                    "note": null,
                    "image": "https://assets.gojourny.com/uploads/images/attachments/78fd632d-fced-4471-a604-64e1aab6f98d.jpg",
                    "type": "activity",
                    "latitude": "34.9985543",
                    "longitude": "135.7792257",
                    "row_order_position": 1,
                    "itinerary_id": 16237,
                    "section_id": 580825,
                    "slot_id": 610638,
                    "group_id": null,
                    "estimated_time_to_spend": "1800"
                }
            }
        },
        "586375": {
            "location_items": {
                "586375": {
                    "id": 586375,
                    "name": "Kiyomizu-dera",
                    "description": null,
                    "location_id": 9347,
                    "full_data": false,
                    "display_title": "Visit Kiyomizudera Temple (catch the sunrise or sunset if you can)",
                    "description_short": "Kiyomizu-dera is one of Japan's most popular temples. It stands in the wooded hills of eastern Kyoto and offers visitors a nice view over the city from its famous wooden terrace. The busy approach to the temple is lined by dozens of shops and restaurants that have been catering to pilgrims and tourists for centuries. Don’t forget to enter the subterranean Tainai-Meguri, which symbolically represents the womb of Daizuigu Bosatsu, a female Bodhisattva who has the power to grant any human wish. Inside, you're plunged into darkness with nothing guiding you save for some glowing stones. \r\n\r\n400 yen admission. During certain days throughout the year, the temple is open until 9PM.",
                    "note": null,
                    "image": "https://assets.gojourny.com/uploads/images/attachments/b9f763a0-600d-4da9-9aa8-ed9ec7fa1327.jpg",
                    "type": "activity",
                    "latitude": "34.9948561",
                    "longitude": "135.7850463",
                    "row_order_position": 5,
                    "itinerary_id": 16237,
                    "section_id": 580825,
                    "slot_id": 610638,
                    "group_id": null,
                    "estimated_time_to_spend": "3600"
                }
            }
        },
        "586374": {
            "location_items": {
                "586374": {
                    "id": 586374,
                    "name": null,
                    "description": null,
                    "location_id": 26806,
                    "full_data": false,
                    "display_title": "Walk through the Historic and Charming Street of Sannen-zaka ",
                    "description_short": null,
                    "note": null,
                    "image": "https://assets.gojourny.com/uploads/images/attachments/9ec204da-fa60-4b7d-86fc-664cb9217f76.jpeg",
                    "type": "activity",
                    "latitude": "34.9963442",
                    "longitude": "135.7808771",
                    "row_order_position": 3,
                    "itinerary_id": 16237,
                    "section_id": 580825,
                    "slot_id": 610638,
                    "group_id": null,
                    "estimated_time_to_spend": "900"
                }
            }
        },
        "586334": {
            "location_items": {
                "586334": {
                    "id": 586334,
                    "name": "Hale",
                    "description": null,
                    "location_id": 20751,
                    "full_data": false,
                    "display_title": "Traditional Vegan Monk Eats at Hale ",
                    "description_short": null,
                    "note": null,
                    "image": "https://assets.gojourny.com/uploads/images/attachments/b4037572-29d8-4bd1-86aa-9faf6492715b.jpg",
                    "type": "restaurant",
                    "latitude": "35.0050743",
                    "longitude": "135.7653435",
                    "row_order_position": 0,
                    "itinerary_id": 16237,
                    "section_id": 580825,
                    "slot_id": 610627,
                    "group_id": null,
                    "estimated_time_to_spend": "3600"
                }
            }
        },
        "586333": {
            "location_items": {
                "586333": {
                    "id": 586333,
                    "name": "Nishiki Market ",
                    "description": null,
                    "location_id": 10229,
                    "full_data": false,
                    "display_title": "Explore and Snack in Nishiki Food Market",
                    "description_short": null,
                    "note": null,
                    "image": "https://assets.gojourny.com/uploads/images/attachments/c93b0388-bf6b-4034-a8af-9b505715baca.jpeg",
                    "type": "activity",
                    "latitude": "35.00500019999999",
                    "longitude": "135.7632709",
                    "row_order_position": 3,
                    "itinerary_id": 16237,
                    "section_id": 580825,
                    "slot_id": 610617,
                    "group_id": null,
                    "estimated_time_to_spend": "5400"
                }
            }
        },
        "586345": {
            "location_items": {
                "586345": {
                    "id": 586345,
                    "name": "Kidoairaku ",
                    "description": null,
                    "location_id": 61180,
                    "full_data": false,
                    "display_title": "Shop Handmade Pottery at Kidoairaku ",
                    "description_short": null,
                    "note": null,
                    "image": "https://assets.gojourny.com/uploads/images/attachments/2a9ce9c3-767c-41e1-ba63-33d6b38e019e.JPG",
                    "type": "shopping",
                    "latitude": "35.0051092",
                    "longitude": "135.7634688",
                    "row_order_position": 4,
                    "itinerary_id": 16237,
                    "section_id": 580825,
                    "slot_id": 610617,
                    "group_id": null,
                    "estimated_time_to_spend": "900"
                }
            }
        },
        "588394": {
            "location_items": {
                "588394": {
                    "id": 588394,
                    "name": "Shirakawa Canal",
                    "description": null,
                    "location_id": 58723,
                    "full_data": false,
                    "display_title": "Admire the Illuminated Cherry Blossoms Along the Shirakawa Canal ",
                    "description_short": null,
                    "note": null,
                    "image": "https://assets.gojourny.com/uploads/images/attachments/c653525a-8700-44d1-8884-54f33a89f373.jpg",
                    "type": "activity",
                    "latitude": "35.0055356",
                    "longitude": "135.7741435",
                    "row_order_position": 0,
                    "itinerary_id": 16237,
                    "section_id": 580825,
                    "slot_id": 610668,
                    "group_id": null,
                    "estimated_time_to_spend": "1800"
                }
            }
        },
        "588564": {
            "location_items": {
                "588564": {
                    "id": 588564,
                    "name": "Kyoto Station",
                    "description": null,
                    "location_id": 52125,
                    "full_data": false,
                    "display_title": "Arrive/Depart Kyoto Station",
                    "description_short": "Kyoto Station is a major railway station and transportation hub in Kyoto, Japan. It has Japan's second-largest station building (after Nagoya Station) and is one of the country's largest buildings, incorporating a shopping mall, hotel, movie theater, Isetan department store, and several local government facilities under one 15-story roof.\r\n\r\nLockers can be found throughout the station building. They come in a range of sizes at fees of 300, 500 and 700 yen. There is usually a change machine nearby, or sign pointing the way to one. These are easy to use and can change 1000 yen notes for appropriate coins. If your luggage is too bulky for a locker you can use the Baggage Room on the B1 floor. ",
                    "note": null,
                    "image": "https://assets.gojourny.com/uploads/images/attachments/01481968-d61b-413f-a058-f0cc55496b1e.jpg",
                    "type": "activity",
                    "latitude": "34.9854082",
                    "longitude": "135.7580554",
                    "row_order_position": 1,
                    "itinerary_id": 16237,
                    "section_id": 580825,
                    "slot_id": 610617,
                    "group_id": null,
                    "estimated_time_to_spend": "1800"
                }
            }
        },
        "586318": {
            "location_items": {
                "586318": {
                    "id": 586318,
                    "name": "Tokyo Station",
                    "description": null,
                    "location_id": 46081,
                    "full_data": false,
                    "display_title": "Arrive/Depart Tokyo Station ",
                    "description_short": null,
                    "note": null,
                    "image": "https://assets.gojourny.com/uploads/images/attachments/ff478f77-eb02-4f80-b221-3cd112f90c48.jpg",
                    "type": "activity",
                    "latitude": "35.680552",
                    "longitude": "139.7670038",
                    "row_order_position": 0,
                    "itinerary_id": 16237,
                    "section_id": 580825,
                    "slot_id": 610617,
                    "group_id": null,
                    "estimated_time_to_spend": "2700"
                }
            }
        }
    },
    "group_items": {},
    "reservations": {}
}
```

## Get a specific day item

This endpoint retrieves all trip sections for a specific itinerary.

### HTTP Request

`GET http://staging.gojourny.com/api/v3/itineraries/<ITINERARY_ID>/day_items/<DAY_ITEM_ID>`

### URL Parameters

Parameter | Description
--------- | -----------
ITINERARY_ID | The ID of the itinerary to delete
DAY_ITEM_ID  | The Day Item Id

```ruby
require 'Journy'

api = Journy::APIClient.authorize!('secret-token')
api.itineraries.get
```

```python
import Journy

api = Journy.authorize('secret-token')
api.itineraries.get()
```

```shell
curl "http://staging.gojourny.com/api/itineraries/:id/trip_sections"
  -H "Authorization: secret-token"
```

```javascript
const Journy = require('Journy');

let api = Journy.authorize('secret-token');
let itineraries = api.itineraries.get();
```

> The above command returns JSON structured like this:

```json
{
    "day_items": {
        "580825": {
            "id": 580825,
            "date": "2020-03-27",
            "name": "Day 5",
            "accommodation_items": [
                {
                    "resource_type": "accommodation_item",
                    "id": 842445
                }
            ],
            "slots": [
                {
                    "name": "breakfast",
                    "items": [
                        {
                            "resource_type": "location_item",
                            "id": 586331
                        }
                    ]
                },
                {
                    "name": "morning_activities",
                    "items": [
                        {
                            "resource_type": "location_item",
                            "id": 586318
                        },
                        {
                            "resource_type": "location_item",
                            "id": 588564
                        },
                        {
                            "resource_type": "location_item",
                            "id": 586206
                        },
                        {
                            "resource_type": "location_item",
                            "id": 586333
                        },
                        {
                            "resource_type": "location_item",
                            "id": 586345
                        }
                    ]
                },
                {
                    "name": "lunch",
                    "items": [
                        {
                            "resource_type": "location_item",
                            "id": 586334
                        }
                    ]
                },
                {
                    "name": "afternoon_activites",
                    "items": [
                        {
                            "resource_type": "location_item",
                            "id": 588574
                        },
                        {
                            "resource_type": "location_item",
                            "id": 586372
                        },
                        {
                            "resource_type": "location_item",
                            "id": 586373
                        },
                        {
                            "resource_type": "location_item",
                            "id": 586374
                        },
                        {
                            "resource_type": "location_item",
                            "id": 586339
                        },
                        {
                            "resource_type": "location_item",
                            "id": 586375
                        },
                        {
                            "resource_type": "location_item",
                            "id": 586358
                        },
                        {
                            "resource_type": "location_item",
                            "id": 588537
                        },
                        {
                            "resource_type": "location_item",
                            "id": 586361
                        },
                        {
                            "resource_type": "location_item",
                            "id": 586357
                        }
                    ]
                },
                {
                    "name": "dinner",
                    "items": [
                        {
                            "resource_type": "location_item",
                            "id": 588566
                        }
                    ]
                },
                {
                    "name": "nighttime",
                    "items": [
                        {
                            "resource_type": "location_item",
                            "id": 588394
                        }
                    ]
                },
                {
                    "name": "lodging",
                    "items": [
                        {
                            "resource_type": "location_item",
                            "id": 586205
                        }
                    ]
                }
            ]
        }
    },
    "accommodation_items": {
        "842445": {
            "location_items": {
                "842445": {
                    "id": 842445,
                    "name": "The Tokyo Station Hotel",
                    "description": null,
                    "location_id": 18733,
                    "full_data": false,
                    "display_title": "Rest up at the Tokyo Station Hotel",
                    "description_short": "Set in a Renaissance-style building dating back to 1915, this upscale hotel is directly connected to Tokyo train station and 2 km from the Imperial Palace. \r\n\r\nAiry rooms with classic furnishings offer free Wi-Fi, flat-screen TVs and iPod docks, plus tea and coffeemakers. Chic, upgraded rooms feature chandeliers and plush fabrics; some have palace or station views. Suites, some of which are split-level, have separate lounges.\r\n\r\nA free breakfast buffet is served in an atrium lobby lounge. Other dining options include high-end French and Cantonese restaurants, an Italian eatery and a cozy cocktail bar. There's also a gym and an expansive spa.",
                    "note": null,
                    "image": "https://assets.gojourny.com/uploads/images/attachments/6f628c53-f0d6-4b5e-b73d-31fd14331fad.jpg",
                    "type": "lodging",
                    "latitude": "35.68125289999999",
                    "longitude": "139.7660004",
                    "row_order_position": 0,
                    "itinerary_id": 16237,
                    "section_id": 580825,
                    "slot_id": null,
                    "group_id": null,
                    "estimated_time_to_spend": "1800"
                }
            }
        }
    },
    "location_items": {
        "586331": {
            "location_items": {
                "586331": {
                    "id": 586331,
                    "name": "Ueshima Coffee Shop | Yaesu Underground Mall",
                    "description": null,
                    "location_id": 66519,
                    "full_data": false,
                    "display_title": "Grab breakfast and coffee for the train at Ueshima Coffee Shop | Yaesu Underground Mall",
                    "description_short": "",
                    "note": null,
                    "image": "https://assets.gojourny.com/uploads/images/attachments/6bc4a330-df46-4f26-83fb-80b38fa1ceee.jpeg",
                    "type": "cafe",
                    "latitude": "35.6790482",
                    "longitude": "139.7680455",
                    "row_order_position": 0,
                    "itinerary_id": 16237,
                    "section_id": 580825,
                    "slot_id": 610609,
                    "group_id": null,
                    "estimated_time_to_spend": "900"
                }
            }
        },
        "588574": {
            "location_items": {
                "588574": {
                    "id": 588574,
                    "name": "Yugen",
                    "description": null,
                    "location_id": 63267,
                    "full_data": false,
                    "display_title": "High-Quality Matcha in Modern Tea Room Yugen ",
                    "description_short": null,
                    "note": null,
                    "image": "https://assets.gojourny.com/uploads/images/attachments/c72c9dad-4b28-4a6b-bb4e-7aa8d821126a.jpeg",
                    "type": "cafe",
                    "latitude": "35.0014045",
                    "longitude": "135.7658035",
                    "row_order_position": 0,
                    "itinerary_id": 16237,
                    "section_id": 580825,
                    "slot_id": 610638,
                    "group_id": null,
                    "estimated_time_to_spend": "2700"
                }
            }
        },
        "586361": {
            "location_items": {
                "586361": {
                    "id": 586361,
                    "name": null,
                    "description": null,
                    "location_id": 26786,
                    "full_data": false,
                    "display_title": "Glimpse a Geisha Along Hanami-Koji Street, Gion District's Most Picturesque Area",
                    "description_short": null,
                    "note": null,
                    "image": "https://assets.gojourny.com/uploads/images/attachments/0522f277-6a22-4253-9fa1-19f0c8f9ea86.jpg",
                    "type": "activity",
                    "latitude": "35.002762",
                    "longitude": "135.774912",
                    "row_order_position": 8,
                    "itinerary_id": 16237,
                    "section_id": 580825,
                    "slot_id": 610638,
                    "group_id": null,
                    "estimated_time_to_spend": "900"
                }
            }
        },
        "588537": {
            "location_items": {
                "588537": {
                    "id": 588537,
                    "name": "Gion",
                    "description": null,
                    "location_id": 9345,
                    "full_data": false,
                    "display_title": "Explore the Streets of the Gion District",
                    "description_short": "Down by the Kamogawa river banks, you’ll find the Gion District: a fascinating mix of old and new Kyoto. One street is lit by teahouse lanterns, while tall buildings line the next. \r\n\r\nGion is famous as one of Kyoto’s geisha districts, so keep an eye out for kimonos in the crowd while you make your way to one of the many restaurants and teahouses.",
                    "note": null,
                    "image": "https://assets.gojourny.com/uploads/images/attachments/a85d2fc6-9dfe-4e18-ad98-1d7f3a312d03.jpg",
                    "type": "activity",
                    "latitude": "35.003776",
                    "longitude": "135.777132",
                    "row_order_position": 7,
                    "itinerary_id": 16237,
                    "section_id": 580825,
                    "slot_id": 610638,
                    "group_id": null,
                    "estimated_time_to_spend": "3600"
                }
            }
        },
        "588566": {
            "location_items": {
                "588566": {
                    "id": 588566,
                    "name": "Izuu ",
                    "description": null,
                    "location_id": 57027,
                    "full_data": false,
                    "display_title": "Kyoto-Style Pressed Sushi at Izuu ",
                    "description_short": null,
                    "note": null,
                    "image": "https://assets.gojourny.com/uploads/images/attachments/8b33e224-ae08-4f2c-9582-af358ee821b3.jpg",
                    "type": "restaurant",
                    "latitude": "35.0048407",
                    "longitude": "135.7745153",
                    "row_order_position": 0,
                    "itinerary_id": 16237,
                    "section_id": 580825,
                    "slot_id": 610656,
                    "group_id": null,
                    "estimated_time_to_spend": "3600"
                }
            }
        },
        "586205": {
            "location_items": {
                "586205": {
                    "id": 586205,
                    "name": "Toshiharu Ryokan",
                    "description": null,
                    "location_id": 40446,
                    "full_data": false,
                    "display_title": "Rest Up at Toshiharu Ryokan",
                    "description_short": "",
                    "note": null,
                    "image": "https://assets.gojourny.com/uploads/images/attachments/066da731-2518-485d-b36e-a39c61e2ad04.jpg",
                    "type": "lodging",
                    "latitude": "34.998421",
                    "longitude": "135.758695",
                    "row_order_position": 0,
                    "itinerary_id": 16237,
                    "section_id": 580825,
                    "slot_id": 610679,
                    "group_id": null,
                    "estimated_time_to_spend": "2700"
                }
            }
        },
        "586206": {
            "location_items": {
                "586206": {
                    "id": 586206,
                    "name": "Toshiharu Ryokan",
                    "description": null,
                    "location_id": 40446,
                    "full_data": false,
                    "display_title": "Rest Up at Toshiharu Ryokan",
                    "description_short": "",
                    "note": null,
                    "image": "https://assets.gojourny.com/uploads/images/attachments/066da731-2518-485d-b36e-a39c61e2ad04.jpg",
                    "type": "lodging",
                    "latitude": "34.998421",
                    "longitude": "135.758695",
                    "row_order_position": 2,
                    "itinerary_id": 16237,
                    "section_id": 580825,
                    "slot_id": 610617,
                    "group_id": null,
                    "estimated_time_to_spend": "2700"
                }
            }
        },
        "586339": {
            "location_items": {
                "586339": {
                    "id": 586339,
                    "name": "Ichihara Heibei Shoten ",
                    "description": null,
                    "location_id": 21617,
                    "full_data": false,
                    "display_title": "Handmade Chopsticks at Ichihara Heibei Shoten (市原平兵衛商店)",
                    "description_short": null,
                    "note": null,
                    "image": "https://assets.gojourny.com/uploads/images/attachments/f33f8f6e-c650-4592-89fe-a9f8d1ef4057.jpg",
                    "type": "shopping",
                    "latitude": "35.00294459999999",
                    "longitude": "135.7634184",
                    "row_order_position": 4,
                    "itinerary_id": 16237,
                    "section_id": 580825,
                    "slot_id": 610638,
                    "group_id": null,
                    "estimated_time_to_spend": "900"
                }
            }
        },
        "586373": {
            "location_items": {
                "586373": {
                    "id": 586373,
                    "name": null,
                    "description": null,
                    "location_id": 26803,
                    "full_data": false,
                    "display_title": "Walk Down the Picturesque Preserved Shopping Streets of Ninen-zaka Leading to Kiyomizudera",
                    "description_short": null,
                    "note": null,
                    "image": "https://assets.gojourny.com/uploads/images/attachments/6acb5227-0ae4-414b-91fa-21d79da08895.jpg",
                    "type": "activity",
                    "latitude": "34.998122",
                    "longitude": "135.7808431",
                    "row_order_position": 2,
                    "itinerary_id": 16237,
                    "section_id": 580825,
                    "slot_id": 610638,
                    "group_id": null,
                    "estimated_time_to_spend": "900"
                }
            }
        },
        "586357": {
            "location_items": {
                "586357": {
                    "id": 586357,
                    "name": "Maruyama Park",
                    "description": null,
                    "location_id": 26959,
                    "full_data": false,
                    "display_title": "Visit Maruyama Park, Kyoto's Most Popular Public Park (Especially for Cherry Blossom Parties)",
                    "description_short": null,
                    "note": null,
                    "image": "https://assets.gojourny.com/uploads/images/attachments/2cd9d85c-e9dd-4803-97b8-132c4b2a15a5.jpg",
                    "type": "activity",
                    "latitude": "35.00388030000001",
                    "longitude": "135.7809168",
                    "row_order_position": 9,
                    "itinerary_id": 16237,
                    "section_id": 580825,
                    "slot_id": 610638,
                    "group_id": null,
                    "estimated_time_to_spend": "3600"
                }
            }
        },
        "586358": {
            "location_items": {
                "586358": {
                    "id": 586358,
                    "name": "Yasaka Shrine ",
                    "description": null,
                    "location_id": 9349,
                    "full_data": false,
                    "display_title": "Stop and See the Lanterns at Yasaka Shrine",
                    "description_short": null,
                    "note": null,
                    "image": "https://assets.gojourny.com/uploads/images/attachments/b8c67c89-5959-48df-b2b4-a5bab9f5a680.jpg",
                    "type": "activity",
                    "latitude": "35.0036559",
                    "longitude": "135.7785534",
                    "row_order_position": 6,
                    "itinerary_id": 16237,
                    "section_id": 580825,
                    "slot_id": 610638,
                    "group_id": null,
                    "estimated_time_to_spend": "1800"
                }
            }
        },
        "586372": {
            "location_items": {
                "586372": {
                    "id": 586372,
                    "name": null,
                    "description": null,
                    "location_id": 26794,
                    "full_data": false,
                    "display_title": "See the Hokan-ji Temple / Yasaka Pagoda from Afar 法観寺",
                    "description_short": null,
                    "note": null,
                    "image": "https://assets.gojourny.com/uploads/images/attachments/78fd632d-fced-4471-a604-64e1aab6f98d.jpg",
                    "type": "activity",
                    "latitude": "34.9985543",
                    "longitude": "135.7792257",
                    "row_order_position": 1,
                    "itinerary_id": 16237,
                    "section_id": 580825,
                    "slot_id": 610638,
                    "group_id": null,
                    "estimated_time_to_spend": "1800"
                }
            }
        },
        "586375": {
            "location_items": {
                "586375": {
                    "id": 586375,
                    "name": "Kiyomizu-dera",
                    "description": null,
                    "location_id": 9347,
                    "full_data": false,
                    "display_title": "Visit Kiyomizudera Temple (catch the sunrise or sunset if you can)",
                    "description_short": "Kiyomizu-dera is one of Japan's most popular temples. It stands in the wooded hills of eastern Kyoto and offers visitors a nice view over the city from its famous wooden terrace. The busy approach to the temple is lined by dozens of shops and restaurants that have been catering to pilgrims and tourists for centuries. Don’t forget to enter the subterranean Tainai-Meguri, which symbolically represents the womb of Daizuigu Bosatsu, a female Bodhisattva who has the power to grant any human wish. Inside, you're plunged into darkness with nothing guiding you save for some glowing stones. \r\n\r\n400 yen admission. During certain days throughout the year, the temple is open until 9PM.",
                    "note": null,
                    "image": "https://assets.gojourny.com/uploads/images/attachments/b9f763a0-600d-4da9-9aa8-ed9ec7fa1327.jpg",
                    "type": "activity",
                    "latitude": "34.9948561",
                    "longitude": "135.7850463",
                    "row_order_position": 5,
                    "itinerary_id": 16237,
                    "section_id": 580825,
                    "slot_id": 610638,
                    "group_id": null,
                    "estimated_time_to_spend": "3600"
                }
            }
        },
        "586374": {
            "location_items": {
                "586374": {
                    "id": 586374,
                    "name": null,
                    "description": null,
                    "location_id": 26806,
                    "full_data": false,
                    "display_title": "Walk through the Historic and Charming Street of Sannen-zaka ",
                    "description_short": null,
                    "note": null,
                    "image": "https://assets.gojourny.com/uploads/images/attachments/9ec204da-fa60-4b7d-86fc-664cb9217f76.jpeg",
                    "type": "activity",
                    "latitude": "34.9963442",
                    "longitude": "135.7808771",
                    "row_order_position": 3,
                    "itinerary_id": 16237,
                    "section_id": 580825,
                    "slot_id": 610638,
                    "group_id": null,
                    "estimated_time_to_spend": "900"
                }
            }
        },
        "586334": {
            "location_items": {
                "586334": {
                    "id": 586334,
                    "name": "Hale",
                    "description": null,
                    "location_id": 20751,
                    "full_data": false,
                    "display_title": "Traditional Vegan Monk Eats at Hale ",
                    "description_short": null,
                    "note": null,
                    "image": "https://assets.gojourny.com/uploads/images/attachments/b4037572-29d8-4bd1-86aa-9faf6492715b.jpg",
                    "type": "restaurant",
                    "latitude": "35.0050743",
                    "longitude": "135.7653435",
                    "row_order_position": 0,
                    "itinerary_id": 16237,
                    "section_id": 580825,
                    "slot_id": 610627,
                    "group_id": null,
                    "estimated_time_to_spend": "3600"
                }
            }
        },
        "586333": {
            "location_items": {
                "586333": {
                    "id": 586333,
                    "name": "Nishiki Market ",
                    "description": null,
                    "location_id": 10229,
                    "full_data": false,
                    "display_title": "Explore and Snack in Nishiki Food Market",
                    "description_short": null,
                    "note": null,
                    "image": "https://assets.gojourny.com/uploads/images/attachments/c93b0388-bf6b-4034-a8af-9b505715baca.jpeg",
                    "type": "activity",
                    "latitude": "35.00500019999999",
                    "longitude": "135.7632709",
                    "row_order_position": 3,
                    "itinerary_id": 16237,
                    "section_id": 580825,
                    "slot_id": 610617,
                    "group_id": null,
                    "estimated_time_to_spend": "5400"
                }
            }
        },
        "586345": {
            "location_items": {
                "586345": {
                    "id": 586345,
                    "name": "Kidoairaku ",
                    "description": null,
                    "location_id": 61180,
                    "full_data": false,
                    "display_title": "Shop Handmade Pottery at Kidoairaku ",
                    "description_short": null,
                    "note": null,
                    "image": "https://assets.gojourny.com/uploads/images/attachments/2a9ce9c3-767c-41e1-ba63-33d6b38e019e.JPG",
                    "type": "shopping",
                    "latitude": "35.0051092",
                    "longitude": "135.7634688",
                    "row_order_position": 4,
                    "itinerary_id": 16237,
                    "section_id": 580825,
                    "slot_id": 610617,
                    "group_id": null,
                    "estimated_time_to_spend": "900"
                }
            }
        },
        "588394": {
            "location_items": {
                "588394": {
                    "id": 588394,
                    "name": "Shirakawa Canal",
                    "description": null,
                    "location_id": 58723,
                    "full_data": false,
                    "display_title": "Admire the Illuminated Cherry Blossoms Along the Shirakawa Canal ",
                    "description_short": null,
                    "note": null,
                    "image": "https://assets.gojourny.com/uploads/images/attachments/c653525a-8700-44d1-8884-54f33a89f373.jpg",
                    "type": "activity",
                    "latitude": "35.0055356",
                    "longitude": "135.7741435",
                    "row_order_position": 0,
                    "itinerary_id": 16237,
                    "section_id": 580825,
                    "slot_id": 610668,
                    "group_id": null,
                    "estimated_time_to_spend": "1800"
                }
            }
        },
        "588564": {
            "location_items": {
                "588564": {
                    "id": 588564,
                    "name": "Kyoto Station",
                    "description": null,
                    "location_id": 52125,
                    "full_data": false,
                    "display_title": "Arrive/Depart Kyoto Station",
                    "description_short": "Kyoto Station is a major railway station and transportation hub in Kyoto, Japan. It has Japan's second-largest station building (after Nagoya Station) and is one of the country's largest buildings, incorporating a shopping mall, hotel, movie theater, Isetan department store, and several local government facilities under one 15-story roof.\r\n\r\nLockers can be found throughout the station building. They come in a range of sizes at fees of 300, 500 and 700 yen. There is usually a change machine nearby, or sign pointing the way to one. These are easy to use and can change 1000 yen notes for appropriate coins. If your luggage is too bulky for a locker you can use the Baggage Room on the B1 floor. ",
                    "note": null,
                    "image": "https://assets.gojourny.com/uploads/images/attachments/01481968-d61b-413f-a058-f0cc55496b1e.jpg",
                    "type": "activity",
                    "latitude": "34.9854082",
                    "longitude": "135.7580554",
                    "row_order_position": 1,
                    "itinerary_id": 16237,
                    "section_id": 580825,
                    "slot_id": 610617,
                    "group_id": null,
                    "estimated_time_to_spend": "1800"
                }
            }
        },
        "586318": {
            "location_items": {
                "586318": {
                    "id": 586318,
                    "name": "Tokyo Station",
                    "description": null,
                    "location_id": 46081,
                    "full_data": false,
                    "display_title": "Arrive/Depart Tokyo Station ",
                    "description_short": null,
                    "note": null,
                    "image": "https://assets.gojourny.com/uploads/images/attachments/ff478f77-eb02-4f80-b221-3cd112f90c48.jpg",
                    "type": "activity",
                    "latitude": "35.680552",
                    "longitude": "139.7670038",
                    "row_order_position": 0,
                    "itinerary_id": 16237,
                    "section_id": 580825,
                    "slot_id": 610617,
                    "group_id": null,
                    "estimated_time_to_spend": "2700"
                }
            }
        }
    },
    "group_items": {},
    "reservations": {}
}
```




## Get a specific location item

This endpoint retrieves all trip sections for a specific itinerary.

### HTTP Request

`GET http://staging.gojourny.com/api/v3/itineraries/<ITINERARY_ID>/location_items/<LOCATION_ITEM_ID>`

### URL Parameters

Parameter | Description
--------- | -----------
ITINERARY_ID | The ID of the itinerary to delete
LOCATION_ITEM_ID  | The Location Item Id

```ruby
require 'Journy'

api = Journy::APIClient.authorize!('secret-token')
api.itineraries.get
```

```python
import Journy

api = Journy.authorize('secret-token')
api.itineraries.get()
```

```shell
curl "http://staging.gojourny.com/api/itineraries/:id/trip_sections"
  -H "Authorization: secret-token"
```

```javascript
const Journy = require('Journy');

let api = Journy.authorize('secret-token');
let itineraries = api.itineraries.get();
```

> The above command returns JSON structured like this:

```json
{
    "location_items": {
        "592359": {
            "id": 592359,
            "name": "Aji no Hamoto ",
            "description": null,
            "location_id": 54429,
            "full_data": true,
            "display_title": "Browse the Fishy Snacks at Aji no Hamato 味の浜藤",
            "description_short": null,
            "note": null,
            "image": "https://assets.gojourny.com/uploads/images/attachments/5be68e86-611d-42de-a863-cf5b842be2cc.jpeg",
            "type": "shopping",
            "latitude": "35.66576300000001",
            "longitude": "139.770866",
            "row_order_position": 0,
            "itinerary_id": 16237,
            "section_id": 580822,
            "slot_id": 610410,
            "group_id": 842207,
            "estimated_time_to_spend": "900",
            "vendor": "google",
            "vendor_id": "ChIJnwamJN-LGGARJYKMLeEHKRU",
            "opening_hours": [
                {
                    "open": {
                        "day": 0,
                        "time": "0800"
                    },
                    "close": {
                        "day": 0,
                        "time": "1500"
                    }
                },
                {
                    "open": {
                        "day": 1,
                        "time": "0800"
                    },
                    "close": {
                        "day": 1,
                        "time": "1500"
                    }
                },
                {
                    "open": {
                        "day": 2,
                        "time": "0800"
                    },
                    "close": {
                        "day": 2,
                        "time": "1500"
                    }
                },
                {
                    "open": {
                        "day": 3,
                        "time": "0800"
                    },
                    "close": {
                        "day": 3,
                        "time": "1500"
                    }
                },
                {
                    "open": {
                        "day": 4,
                        "time": "0800"
                    },
                    "close": {
                        "day": 4,
                        "time": "1500"
                    }
                },
                {
                    "open": {
                        "day": 5,
                        "time": "0800"
                    },
                    "close": {
                        "day": 5,
                        "time": "1500"
                    }
                },
                {
                    "open": {
                        "day": 6,
                        "time": "0800"
                    },
                    "close": {
                        "day": 6,
                        "time": "1500"
                    }
                }
            ],
            "place_type_to_show": "shopping",
            "reservation_required": false,
            "permanently_closed": false,
            "url": "http://www.hamato.co.jp/",
            "address": "4-chōme-11-4 Tsukiji, Chuo City, Tōkyō-to 104-0045, Japan",
            "tel": "+81 3-3542-2273"
        }
    }
}
```
