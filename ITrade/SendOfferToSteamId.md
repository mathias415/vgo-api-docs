## Sends trade offer to another VGo user including your and their items

#### HTTP Request

`POST http://api.vgo.gg/ITrade/SendOfferToSteamId/v1/`

#### Input

Parameter | Type | Required   | Description
--------- | -----| :--------: | -----------
steam_id | int |  <p_required>+</p_required> | Steam ID of user you want to send your trade offer to
items | string | <p_required>+</p_required> | A comma-separated list of item ids you wish to include in trade offer. There should be both yours and recipients items. 100 maximum per each side.
twofactor_code | string |  <p_required>+</p_required> | 2-factor authentication code

    
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
