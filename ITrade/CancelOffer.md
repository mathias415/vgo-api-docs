## Cancels a trade offer

If cancelled by the sender it will go into `STATE_CANCELLED` (6) and if cancelled by the receiver it will go into `STATE_DECLINED` (7).

#### HTTP Request

`POST http://api.vgo.gg/ITrade/CancelOffer/v1/`

#### Input

Parameter | Type | Required   | Description
--------- | -----| :--------: | -----------
offer_id | int |  <p_required>+</p_required> | Offer ID that you're a party to (sender or receiver)

    
#### Output

Parameter | Type | Description
--------- | -----| -------- 
offer     | object    | Offer data
 - id     | int | Offer id
 - sender | object | Sender's info
 -- uid | int | Sender's userid
 -- items | array-object | List of items which sender receives. All item is standard item format (see in [VGO-API-Documentation](VGO-API-Documentation))
 - recipient | object | Recipient's info
 -- uid | int | Recipient's userid
 -- items | array-object | List of items which recipient receives. All item is standard item format (see in [VGO-API-Documentation](VGO-API-Documentation))
 - state | int | order state, see states are defined in [ITrade](Itrade)
 - time_created | int | creation timestamp
 - time_updated | int | last update timestamp
 - time_expires | int | expiration timestamp
 - message | string | message added by sender (probably not used)
 - sent_by_you | bool | Optionally param.  Whether or not this offer was sent by you.  Will not show up in unauthenticated endpoints.
new items | array-object | items, new for the recipient (user that makes this API call). All item is standard item format (see in [VGO-API-Documentation](VGO-API-Documentation))