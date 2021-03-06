---
title: API Reference

language_tabs: # must be one of https://git.io/vQNgJ
  - shell
  - ruby
  - python
  - javascript

toc_footers:
  - <a href='"mailto:tech@gojourny.com"'>Email us for a Developer Key</a>
  - <a href='https://github.com/slatedocs/slate'>Documentation Powered by Slate</a>

includes:
  - errors

search: true

code_clipboard: true
---

# Introduction

Welcome to the Journy API! You can use our API to access Journy API endpoints, where you can create itineraries for display in Journy's itineraries .

We have language examples in Shell, Ruby, Python, and JavaScript! You can view code examples in the dark area to the right, and you can switch the programming language of the examples with the tabs in the top right.

# Authentication

> To authorize, include the Bearer token in each request:

```ruby
require 'net/http'

uri     = URI("https://staging.gojourny.com/api/v2/itineraries")
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

url     = "https://staging.gojourny.com/api/v2/itineraries"
headers = {
    'Authorization': 'Bearer exampleJournyToken',
    'Content-Type': 'application/json',
    'Accept': 'application/json'
}

response = requests.get(url, headers=headers)
```

```shell
# With shell, you can just pass the correct header with each request
curl "https://staging.gojourny.com/api/v2/itineraries" \
  -H "Authorization: Bearer exampleJournyToken"
```

```javascript
const url     = "https://staging.gojourny.com/api/v2/itineraries"
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

> Make sure to replace `exampleJournyToken` with your API key.

Journy uses API keys to allow access to the API. You can be issued a Journy API key by contacting us directly.

Journy expects for the API key to be included in all API requests to the server in a header that looks like the following:

`Authorization: Bearer exampleJournyToken`

<aside class="notice">
You must replace <code>exampleJournyToken</code> with your personal API key.
</aside>

# Countries

## Get All Countries

```ruby
require 'net/http'

uri     = URI("https://staging.gojourny.com/api/v2/countries")
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

url     = "https://staging.gojourny.com/api/v2/countries"
headers = {
    'Authorization': 'Bearer exampleJournyToken',
    'Content-Type': 'application/json',
    'Accept': 'application/json'
}

response = requests.get(url, headers=headers)
```

```shell
# With shell, you can just pass the correct header with each request
curl "https://staging.gojourny.com/api/v2/countries"
  -H "Authorization: Bearer exampleJournyToken"
```

```javascript
const url     = "https://staging.gojourny.com/api/v2/countries"
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
[
  {
    "id": 14,
    "destination_region_id": 6,
    "name": "Aruba",
    "code": "AW",
    "slug": "aruba",
    "latitude": "12.52111",
    "longitude": "-69.968338"
  }
]
```

This endpoint retrieves all itineraries for your entity.

### HTTP Request

`GET https://staging.gojourny.com/api/v2/countries`

### Query Parameters

Parameter | Default | Description
--------- | ------- | -----------
page | 1 | Integer, used in combination with page_size
page_size | 25 | Integer, used to set array return size

<aside class="success">
Remember — all requests need to carry the authentication token!
</aside>

## Get a Specific Country

```ruby
require 'net/http'

uri     = URI("https://staging.gojourny.com/api/v2/countries/14")
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

url     = "https://staging.gojourny.com/api/v2/countries/14"
headers = {
    'Authorization': 'Bearer exampleJournyToken',
    'Content-Type': 'application/json',
    'Accept': 'application/json'
}

response = requests.get(url, headers=headers)
```

```shell
# With shell, you can just pass the correct header with each request
curl "https://staging.gojourny.com/api/v2/countries/14"
  -H "Authorization: Bearer exampleJournyToken"
```

```javascript
const url     = "https://staging.gojourny.com/api/v2/countries/14"
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
  "id": 14,
  "destination_region_id": 6,
  "name": "Aruba",
  "code": "AW",
  "slug": "aruba",
  "latitude": "12.52111",
  "longitude": "-69.968338"
}
```

This endpoint retrieves a specific itinerary.

### HTTP Request

`GET http://staging.gojourny.com/api/v2/countries/<ID>`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the itinerary to retrieve

# Destinations

## Get All Itineraries

```ruby
require 'net/http'

uri     = URI("https://staging.gojourny.com/api/v2/itineraries")
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

url     = "https://staging.gojourny.com/api/v2/itineraries"
headers = {
    'Authorization': 'Bearer exampleJournyToken',
    'Content-Type': 'application/json',
    'Accept': 'application/json'
}

response = requests.get(url, headers=headers)
```

```shell
# With shell, you can just pass the correct header with each request
curl "https://staging.gojourny.com/api/v2/itineraries"
  -H "Authorization: Bearer exampleJournyToken"
```

```javascript
const url     = "https://staging.gojourny.com/api/v2/itineraries"
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

`GET https://staging.gojourny.com/api/v2/itineraries`

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

uri     = URI("https://staging.gojourny.com/api/v2/itineraries/15700")
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

url     = "https://staging.gojourny.com/api/v2/itineraries/15700"
headers = {
    'Authorization': 'Bearer exampleJournyToken',
    'Content-Type': 'application/json',
    'Accept': 'application/json'
}

response = requests.get(url, headers=headers)
```

```shell
# With shell, you can just pass the correct header with each request
curl "https://staging.gojourny.com/api/v2/itineraries/15700"
  -H "Authorization: Bearer exampleJournyToken"
```

```javascript
const url     = "https://staging.gojourny.com/api/v2/itineraries/15700"
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

`GET http://staging.gojourny.com/api/v2/itineraries/<ID>`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the itinerary to retrieve

## Update a Specific Itinerary

```ruby
require 'net/http'

uri     = URI("https://staging.gojourny.com/api/v2/itineraries/15700")
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

url     = "https://staging.gojourny.com/api/v2/itineraries/15700"
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
     "https://staging.gojourny.com/api/v2/itineraries/15700"
```

```javascript
const url     = "https://staging.gojourny.com/api/v2/itineraries/15700"
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

`PATCH http://staging.gojourny.com/api/v2/itineraries/<ID>`
`PUT http://staging.gojourny.com/api/v2/itineraries/<ID>`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the itinerary to retrieve


## Delete a Specific itinerary

```ruby
require 'net/http'

uri     = URI("https://staging.gojourny.com/api/v2/itineraries/15700")
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

url     = "https://staging.gojourny.com/api/v2/itineraries/15700"
headers = {
    'Authorization': 'Bearer exampleJournyToken',
    'Content-Type': 'application/json',
    'Accept': 'application/json'
}

response = requests.delete(url, headers=headers)
```

```shell
# With shell, you can just pass the correct header with each request
curl -X DELETE "https://staging.gojourny.com/api/v2/itineraries" \
  -H "Authorization: Bearer exampleJournyToken"
```

```javascript
const url     = "https://staging.gojourny.com/api/v2/itineraries/15700"
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

`DELETE http://staging.gojourny.com/api/v2/itineraries/<ID>`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the itinerary to delete


# Destination Regions

## Get All Destination Regions

```ruby
require 'net/http'

uri     = URI("https://staging.gojourny.com/api/v2/destination_regions")
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

url     = "https://staging.gojourny.com/api/v2/destination_regions"
headers = {
    'Authorization': 'Bearer exampleJournyToken',
    'Content-Type': 'application/json',
    'Accept': 'application/json'
}

response = requests.get(url, headers=headers)
```

```shell
# With shell, you can just pass the correct header with each request
curl "https://staging.gojourny.com/api/v2/destination_regions"
  -H "Authorization: Bearer exampleJournyToken"
```

```javascript
const url     = "https://staging.gojourny.com/api/v2/destination_regions"
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
[
  {
    "id": 1,
    "name": "Africa",
    "code": "africa",
    "slug": "africa"
  }
]
```

This endpoint retrieves all destination regions for your entity.

### HTTP Request

`GET https://staging.gojourny.com/api/v2/destination_regions`

### Query Parameters

Parameter | Default | Description
--------- | ------- | -----------
page | 1 | Integer, used in combination with page_size
page_size | 25 | Integer, used to set array return size

<aside class="success">
Remember — all requests need to carry the authentication token!
</aside>

# Itineraries

## Get All Itineraries

```ruby
require 'net/http'

uri     = URI("https://staging.gojourny.com/api/v2/itineraries")
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

url     = "https://staging.gojourny.com/api/v2/itineraries"
headers = {
    'Authorization': 'Bearer exampleJournyToken',
    'Content-Type': 'application/json',
    'Accept': 'application/json'
}

response = requests.get(url, headers=headers)
```

```shell
# With shell, you can just pass the correct header with each request
curl "https://staging.gojourny.com/api/v2/itineraries"
  -H "Authorization: Bearer exampleJournyToken"
```

```javascript
const url     = "https://staging.gojourny.com/api/v2/itineraries"
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

`GET https://staging.gojourny.com/api/v2/itineraries`

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

uri     = URI("https://staging.gojourny.com/api/v2/itineraries/15700")
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

url     = "https://staging.gojourny.com/api/v2/itineraries/15700"
headers = {
    'Authorization': 'Bearer exampleJournyToken',
    'Content-Type': 'application/json',
    'Accept': 'application/json'
}

response = requests.get(url, headers=headers)
```

```shell
# With shell, you can just pass the correct header with each request
curl "https://staging.gojourny.com/api/v2/itineraries/15700"
  -H "Authorization: Bearer exampleJournyToken"
```

```javascript
const url     = "https://staging.gojourny.com/api/v2/itineraries/15700"
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

`GET http://staging.gojourny.com/api/v2/itineraries/<ID>`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the itinerary to retrieve

## Update a Specific Itinerary

```ruby
require 'net/http'

uri     = URI("https://staging.gojourny.com/api/v2/itineraries/15700")
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

url     = "https://staging.gojourny.com/api/v2/itineraries/15700"
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
     "https://staging.gojourny.com/api/v2/itineraries/15700"
```

```javascript
const url     = "https://staging.gojourny.com/api/v2/itineraries/15700"
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

`PATCH http://staging.gojourny.com/api/v2/itineraries/<ID>`
`PUT http://staging.gojourny.com/api/v2/itineraries/<ID>`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the itinerary to retrieve


## Delete a Specific itinerary

```ruby
require 'net/http'

uri     = URI("https://staging.gojourny.com/api/v2/itineraries/15700")
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

url     = "https://staging.gojourny.com/api/v2/itineraries/15700"
headers = {
    'Authorization': 'Bearer exampleJournyToken',
    'Content-Type': 'application/json',
    'Accept': 'application/json'
}

response = requests.delete(url, headers=headers)
```

```shell
# With shell, you can just pass the correct header with each request
curl -X DELETE "https://staging.gojourny.com/api/v2/itineraries" \
  -H "Authorization: Bearer exampleJournyToken"
```

```javascript
const url     = "https://staging.gojourny.com/api/v2/itineraries/15700"
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

`DELETE http://staging.gojourny.com/api/v2/itineraries/<ID>`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the itinerary to delete

# ItineraryItems

## Get All Itineraries

```ruby
require 'Journy'

api = Journy::APIClient.authorize!('meowmeowmeow')
api.itineraries.get
```

```python
import Journy

api = Journy.authorize('meowmeowmeow')
api.itineraries.get()
```

```shell
curl "http://staging.gojourny.com/api/itineraries"
  -H "Authorization: meowmeowmeow"
```

```javascript
const Journy = require('Journy');

let api = Journy.authorize('meowmeowmeow');
let itineraries = api.itineraries.get();
```

> The above command returns JSON structured like this:

```json
[
  {
    "id": 1,
    "name": "Fluffums",
    "breed": "calico",
    "fluffiness": 6,
    "cuteness": 7
  },
  {
    "id": 2,
    "name": "Max",
    "breed": "unknown",
    "fluffiness": 5,
    "cuteness": 10
  }
]
```

This endpoint retrieves all itineraries.

### HTTP Request

`GET http://staging.gojourny.com/api/v2/itineraries`

### Query Parameters

Parameter | Default | Description
--------- | ------- | -----------
include_cats | false | If set to true, the result will also include cats.
available | true | If set to false, the result will include itineraries that have already been adopted.

<aside class="success">
Remember — a happy itinerary is an authenticated itinerary!
</aside>

## Get a Specific itinerary

```ruby
require 'Journy'

api = Journy::APIClient.authorize!('meowmeowmeow')
api.itineraries.get(2)
```

```python
import Journy

api = Journy.authorize('meowmeowmeow')
api.itineraries.get(2)
```

```shell
curl "http://staging.gojourny.com/api/itineraries/2"
  -H "Authorization: meowmeowmeow"
```

```javascript
const Journy = require('Journy');

let api = Journy.authorize('meowmeowmeow');
let max = api.itineraries.get(2);
```

> The above command returns JSON structured like this:

```json
{
  "id": 2,
  "name": "Max",
  "breed": "unknown",
  "fluffiness": 5,
  "cuteness": 10
}
```

This endpoint retrieves a specific itinerary.

<aside class="warning">Inside HTML code blocks like this one, you can't use Markdown, so use <code>&lt;code&gt;</code> blocks to denote code.</aside>

### HTTP Request

`GET http://staging.gojourny.com/itineraries/<ID>`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the itinerary to retrieve

## Delete a Specific itinerary

```ruby
require 'Journy'

api = Journy::APIClient.authorize!('meowmeowmeow')
api.itineraries.delete(2)
```

```python
import Journy

api = Journy.authorize('meowmeowmeow')
api.itineraries.delete(2)
```

```shell
curl "http://staging.gojourny.com/api/itineraries/2"
  -X DELETE
  -H "Authorization: meowmeowmeow"
```

```javascript
const Journy = require('Journy');

let api = Journy.authorize('meowmeowmeow');
let max = api.itineraries.delete(2);
```

> The above command returns JSON structured like this:

```json
{
  "id": 2,
  "deleted" : ":("
}
```

This endpoint deletes a specific itinerary.

### HTTP Request

`DELETE http://staging.gojourny.com/itineraries/<ID>`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the itinerary to delete

# LocationItems

## Get All Itineraries

```ruby
require 'Journy'

api = Journy::APIClient.authorize!('meowmeowmeow')
api.itineraries.get
```

```python
import Journy

api = Journy.authorize('meowmeowmeow')
api.itineraries.get()
```

```shell
curl "http://staging.gojourny.com/api/itineraries"
  -H "Authorization: meowmeowmeow"
```

```javascript
const Journy = require('Journy');

let api = Journy.authorize('meowmeowmeow');
let itineraries = api.itineraries.get();
```

> The above command returns JSON structured like this:

```json
[
  {
    "id": 1,
    "name": "Fluffums",
    "breed": "calico",
    "fluffiness": 6,
    "cuteness": 7
  },
  {
    "id": 2,
    "name": "Max",
    "breed": "unknown",
    "fluffiness": 5,
    "cuteness": 10
  }
]
```

This endpoint retrieves all itineraries.

### HTTP Request

`GET http://staging.gojourny.com/api/v2/itineraries`

### Query Parameters

Parameter | Default | Description
--------- | ------- | -----------
include_cats | false | If set to true, the result will also include cats.
available | true | If set to false, the result will include itineraries that have already been adopted.

<aside class="success">
Remember — a happy itinerary is an authenticated itinerary!
</aside>

## Get a Specific itinerary

```ruby
require 'Journy'

api = Journy::APIClient.authorize!('meowmeowmeow')
api.itineraries.get(2)
```

```python
import Journy

api = Journy.authorize('meowmeowmeow')
api.itineraries.get(2)
```

```shell
curl "http://staging.gojourny.com/api/itineraries/2"
  -H "Authorization: meowmeowmeow"
```

```javascript
const Journy = require('Journy');

let api = Journy.authorize('meowmeowmeow');
let max = api.itineraries.get(2);
```

> The above command returns JSON structured like this:

```json
{
  "id": 2,
  "name": "Max",
  "breed": "unknown",
  "fluffiness": 5,
  "cuteness": 10
}
```

This endpoint retrieves a specific itinerary.

<aside class="warning">Inside HTML code blocks like this one, you can't use Markdown, so use <code>&lt;code&gt;</code> blocks to denote code.</aside>

### HTTP Request

`GET http://staging.gojourny.com/itineraries/<ID>`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the itinerary to retrieve

## Delete a Specific itinerary

```ruby
require 'Journy'

api = Journy::APIClient.authorize!('meowmeowmeow')
api.itineraries.delete(2)
```

```python
import Journy

api = Journy.authorize('meowmeowmeow')
api.itineraries.delete(2)
```

```shell
curl "http://staging.gojourny.com/api/itineraries/2"
  -X DELETE
  -H "Authorization: meowmeowmeow"
```

```javascript
const Journy = require('Journy');

let api = Journy.authorize('meowmeowmeow');
let max = api.itineraries.delete(2);
```

> The above command returns JSON structured like this:

```json
{
  "id": 2,
  "deleted" : ":("
}
```

This endpoint deletes a specific itinerary.

### HTTP Request

`DELETE http://staging.gojourny.com/itineraries/<ID>`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the itinerary to delete


# DayItems

## Get All Itineraries

```ruby
require 'Journy'

api = Journy::APIClient.authorize!('meowmeowmeow')
api.itineraries.get
```

```python
import Journy

api = Journy.authorize('meowmeowmeow')
api.itineraries.get()
```

```shell
curl "http://staging.gojourny.com/api/itineraries"
  -H "Authorization: meowmeowmeow"
```

```javascript
const Journy = require('Journy');

let api = Journy.authorize('meowmeowmeow');
let itineraries = api.itineraries.get();
```

> The above command returns JSON structured like this:

```json
[
  {
    "id": 1,
    "name": "Fluffums",
    "breed": "calico",
    "fluffiness": 6,
    "cuteness": 7
  },
  {
    "id": 2,
    "name": "Max",
    "breed": "unknown",
    "fluffiness": 5,
    "cuteness": 10
  }
]
```

This endpoint retrieves all itineraries.

### HTTP Request

`GET http://staging.gojourny.com/api/v2/itineraries`

### Query Parameters

Parameter | Default | Description
--------- | ------- | -----------
include_cats | false | If set to true, the result will also include cats.
available | true | If set to false, the result will include itineraries that have already been adopted.

<aside class="success">
Remember — a happy itinerary is an authenticated itinerary!
</aside>

## Get a Specific itinerary

```ruby
require 'Journy'

api = Journy::APIClient.authorize!('meowmeowmeow')
api.itineraries.get(2)
```

```python
import Journy

api = Journy.authorize('meowmeowmeow')
api.itineraries.get(2)
```

```shell
curl "http://staging.gojourny.com/api/itineraries/2"
  -H "Authorization: meowmeowmeow"
```

```javascript
const Journy = require('Journy');

let api = Journy.authorize('meowmeowmeow');
let max = api.itineraries.get(2);
```

> The above command returns JSON structured like this:

```json
{
  "id": 2,
  "name": "Max",
  "breed": "unknown",
  "fluffiness": 5,
  "cuteness": 10
}
```

This endpoint retrieves a specific itinerary.

<aside class="warning">Inside HTML code blocks like this one, you can't use Markdown, so use <code>&lt;code&gt;</code> blocks to denote code.</aside>

### HTTP Request

`GET http://staging.gojourny.com/itineraries/<ID>`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the itinerary to retrieve

## Delete a Specific itinerary

```ruby
require 'Journy'

api = Journy::APIClient.authorize!('meowmeowmeow')
api.itineraries.delete(2)
```

```python
import Journy

api = Journy.authorize('meowmeowmeow')
api.itineraries.delete(2)
```

```shell
curl "http://staging.gojourny.com/api/itineraries/2"
  -X DELETE
  -H "Authorization: meowmeowmeow"
```

```javascript
const Journy = require('Journy');

let api = Journy.authorize('meowmeowmeow');
let max = api.itineraries.delete(2);
```

> The above command returns JSON structured like this:

```json
{
  "id": 2,
  "deleted" : ":("
}
```

This endpoint deletes a specific itinerary.

### HTTP Request

`DELETE http://staging.gojourny.com/itineraries/<ID>`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the itinerary to delete

# Locations

