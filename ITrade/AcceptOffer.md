## Accepts offer sent by another VGo user

#### HTTP Request

`POST http://api.vgo.gg/ITrade/AcceptOffer/v1/`

#### Input

Parameter | Type | Required   | Description
--------- | -----| :--------: | -----------
twofactor_code | string |  <p_required>+</p_required> | 2-factor authentication code
offer_id | int |  <p_required>+</p_required> | Trade offer Id you want to accept

    
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
 - time_created | int | creation timestamp
 - time_updated | int | last update timestamp
 - time_expires | int | expiration timestamp
 - message | string | message added by sender (probably not used)
 - sent_by_you | bool | probably whether it was sent by you
new items | array-object | items, new for the recipient (user that makes this API call). All item is standard item format (see in [VGO-API-Documentation](VGO-API-Documentation))
failed_cases | int | If it was normal p2p offer, then this number is always 0. If it's open case offer then: it's 0 if all open case transaction were successfully published, if there were failed transactions, then number will be positive