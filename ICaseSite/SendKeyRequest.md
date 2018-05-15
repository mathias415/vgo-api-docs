## Send Key Request

Sends a trade offer to the user requesting some number of keys for uncrating items on a vcase site.

#### HTTP Request

`POST http://api.vgo.gg/ICaseSite/SendKeyRequest/v1`

#### Authorization

Requires an API key with `FLAG_VCASE_SITE`

#### Input

Parameter | Type | Required   | Description
--------- | -----| :--------: | -----------
trade_url | string | + | The trade URL of the user to check
case_id   | int  | + | The case ID the user wants to open
affiliate_eth_address | string | + | The eth address that should receive the commission when the items are uncased.
amount    | int  | - | Number of these cases that should be opened.  Defaults to 1.
    
#### Output

Parameter | Type | Description
--------- | -----| -------- 
offer     | object    | Main to contain data
 - id     | int | Offer id
 - sender | object | Sender's info
 -- uid | int | Sender's userid
 -- items | array-object | List of items which sender receives. All item is standard item format (see in [VGO-API-Documentation](VGO-API-Documentation))
 - recipient | object | Recipient's info
 -- uid | int | Recipient's userid
 -- items | array-object | List of items which recipient receives. All item is standard item format (see in [VGO-API-Documentation](VGO-API-Documentation))
 - state | int | order state, see states are defined in [ITrade](Itrade)
 - state_name | string | Same as state, but readable
 - time_created | int | creation timestamp
 - time_updated | int | last update timestamp
 - time_expires | int | expiration timestamp
 - message | string | message added by sender (probably not used)
 - sent_by_you | bool | whether it was sent by you.  In this case it will always be true.
offer_url | string | Fully-qualified URL to the trade offer. The recipient of this offer can click this link to view the offer and accept it.

