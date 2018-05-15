## Get an individual trade offer

You must be one of the parties involved in the offer (sender/receiver).

#### HTTP Request

`GET http://api.vgo.gg/ITrade/GetOffer/v1/`

#### Input

Parameter | Type | Required   | Description
--------- | -----| :--------: | -----------
offer_id | int |  + | ID of trade offer

#### Output

Parameter | Type | Description
--------- | -----| -------- 
offer    | object | Holds offer and item data
  - id    | int | offer id
  - sender| object | Offer sender's information
  -- uid  | int | Sender's uid
  -- items| array-object | Items which sender offered for trade in the offer. All items are in standard item format (see in [VGO-API-Documentation](VGO-API-Documentation))
  - recipient| object | Offer recipient's information
  -- uid  | int | Recipient's uid
  -- items| array-object | Recipient's items which sender wanted to receive in the offer. All items are in standard item format (see in [VGO-API-Documentation](VGO-API-Documentation))
  - state | int | Offer state code (See available state constants in [ITrade](ITrade))
  - state_name | string | State's display name
  - time_created | int | Offer creation timestamp
  - time_updated | int | Last update timestamp
  - time_expires | int | Offer expiration timestamp
  - message | string | Message (not used)