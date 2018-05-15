## Get user's trade offers

#### HTTP Request

`GET http://api.vgo.gg/ITrade/GetOffers/v1/`

#### Input

Parameter | Type | Required   | Description
--------- | -----| :--------: | -----------
uid | int |  - | ID of other user, involved in offers
state | string |  - | A comma-separated list of offer states to filter by (See available states in [ITrade](ITrade)). 
type | string |  - | One of `sent`, `received`
page | int | - | page number in response (starting with 1, default to 1) 
per_page | int | - | number of items per_page in response (no more then 100)
ids | int-csv | - | Trade offer IDs list filter
    
#### Output

Parameter | Type | Description
--------- | -----| -------- 
total     | int    | Total number of offers (filtered)
offers    | array-object | items list, based on pagination and search filters. 
  - id    | int | offer id
  - sender| array-object | Offer sender's information
  -- uid  | int | Sender's uid
  -- display_name | string | Sender's display name
  -- avatar | string | Sender's avatar url
  -- items| array-object | Items which sender offered for trade in the offer. All items are in standard item format (see in [VGO-API-Documentation](VGO-API-Documentation))
  - recipient| array-object | Offer recipient's information
  -- uid  | int | Recipient's uid
  -- display_name | string | Recipient's display name
  -- avatar | string | Recipient's avatar url
  -- items| array-object | Recipient's items which sender wanted to receive in the offer. All items are in standard item format (see in [VGO-API-Documentation](VGO-API-Documentation))
  - state | int | Offer state code (See available state constants in [ITrade](ITrade))
  - state_name | string | State's display name
  - time_created | int | Offer creation timestamp
  - time_updated | int | Last update timestamp
  - time_expires | int | Offer expiration timestamp
  - message | string | Message (not used)