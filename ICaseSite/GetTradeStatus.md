## Get trade status

Returns the trade status and opened case results from an offer created from a case site.

#### HTTP Request

`GET http://api.vgo.gg/ICaseSite/GetTradeStatus/v1`

#### Authorization

Requires an API key with `FLAG_VCASE_SITE`

#### Input

Parameter | Type | Required   | Description
--------- | -----| :--------: | -----------
offer_id  | int  | + | The trade offer ID created by the requesting user.  Offer should have `FLAG_INITIATED_BY_VCASE_SITE`
    
#### Output

Parameter | Type | Description
--------- | -----| -------- 
offer    | object | Standard offer object output
cases     | array | Array of [OpenedCase objects](VGO-API-Documentation)

