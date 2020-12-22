
# Amenities

## index

Allows the user to retrieve all available amenities

### HTTP Request

`GET http://staging.gojourny.com/api/v3/amenities`

### Query Parameters

> The above command returns JSON structured like this:

```json
[
   {
      "id":"c4c2dae5-196e-4f50-a5e1-bedf418d6534",
      "name":"Free parking",
      "slug":"free-parking",
      "amadeus_id":"PARKING",
      "impala_id":null,
      "hyperguest_id":null,
      "created_at":"2020-10-26T15:31:29.698Z",
      "updated_at":"2020-10-26T15:31:29.698Z",
      "hotel_beds_id":null
   },
   {
      "id":"3b23f537-86e2-43ac-8a9b-03831a092e64",
      "name":"Gym",
      "slug":"gym",
      "amadeus_id":"FITNESS_CENTER",
      "impala_id":null,
      "hyperguest_id":null,
      "created_at":"2020-10-26T15:31:29.495Z",
      "updated_at":"2020-10-26T15:37:14.446Z",
      "hotel_beds_id":"70470"
   },
   {
      "id":"89c0e4d1-2b0d-4a04-82f1-0e2167bd7fd2",
      "name":"Restaurant",
      "slug":"restaurant",
      "amadeus_id":"RESTAURANT",
      "impala_id":null,
      "hyperguest_id":"71200",
      "created_at":"2020-10-26T15:31:29.675Z",
      "updated_at":"2020-10-26T15:37:14.453Z",
      "hotel_beds_id":null
   },
   {
      "id":"93d1cd95-5a2e-4474-a67d-e6211cd781f3",
      "name":"Bar",
      "slug":"bar",
      "amadeus_id":"BAR",
      "impala_id":null,
      "hyperguest_id":"31",
      "created_at":"2020-10-26T15:31:29.680Z",
      "updated_at":"2020-10-26T15:37:14.456Z",
      "hotel_beds_id":"71130"
   },
   {
      "id":"49d25c04-013e-4715-8165-43777e23104f",
      "name":"24/7 Front Desk",
      "slug":"24-7-front-desk-f855b394-d0d4-4039-8ad7-3a941e339c8e",
      "amadeus_id":null,
      "impala_id":null,
      "hyperguest_id":"192",
      "created_at":"2020-10-26T15:37:14.491Z",
      "updated_at":"2020-10-26T15:37:14.491Z",
      "hotel_beds_id":null
   },
   {
      "id":"b1e59264-cdb6-4743-8bca-6fa9cf0135d8",
      "name":"Spa",
      "slug":"spa",
      "amadeus_id":"SPA",
      "impala_id":null,
      "hyperguest_id":null,
      "created_at":"2020-10-26T15:31:29.688Z",
      "updated_at":"2020-10-26T15:37:14.499Z",
      "hotel_beds_id":"74620"
   },
   {
      "id":"9fc5d215-a919-4562-8cd0-546b76f4c085",
      "name":"Babysitting",
      "slug":"babysitting",
      "amadeus_id":"BABY-SITTING",
      "impala_id":null,
      "hyperguest_id":null,
      "created_at":"2020-10-26T15:31:29.691Z",
      "updated_at":"2020-10-26T15:37:14.502Z",
      "hotel_beds_id":"70485"
   },
   {
      "id":"61fcddba-8391-4344-a534-b922d9c56015",
      "name":"Free Wi-Fi",
      "slug":"free-wi-fi",
      "amadeus_id":"WI-FI_IN_ROOM",
      "impala_id":null,
      "hyperguest_id":null,
      "created_at":"2020-10-26T15:31:29.703Z",
      "updated_at":"2020-10-26T15:37:14.505Z",
      "hotel_beds_id":"60261"
   },
   {
      "id":"26bb199d-ce64-409f-af77-fc5c3da8d7eb",
      "name":"Indoor swimming pool",
      "slug":"indoor-swimming-pool",
      "amadeus_id":null,
      "impala_id":null,
      "hyperguest_id":null,
      "created_at":"2020-10-26T15:37:14.508Z",
      "updated_at":"2020-10-26T15:37:14.508Z",
      "hotel_beds_id":"60313"
   },
   {
      "id":"ea543334-9a00-4eb7-b7ae-a1174c602531",
      "name":"Outdoor swimming pool",
      "slug":"outdoor-swimming-pool",
      "amadeus_id":"SWIMMING_POOL",
      "impala_id":null,
      "hyperguest_id":"5544",
      "created_at":"2020-10-26T15:31:29.711Z",
      "updated_at":"2020-10-26T15:37:14.510Z",
      "hotel_beds_id":"60306"
   },
   {
      "id":"813a2948-b17e-4977-a0e0-7fb4d03a3218",
      "name":"Beach access",
      "slug":"24-7-front-desk",
      "amadeus_id":null,
      "impala_id":null,
      "hyperguest_id":null,
      "created_at":"2020-10-26T15:31:29.684Z",
      "updated_at":"2020-10-26T15:37:14.512Z",
      "hotel_beds_id":"4040"
   }
]
```
