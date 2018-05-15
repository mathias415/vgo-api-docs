## Get key count

Returns the number of keys a specific user has.

#### HTTP Request

`GET http://api.vgo.gg/ICaseSite/GetKeyCount/v1`

#### Authorization

Requires an API key with `FLAG_VCASE_SITE`

#### Input

Parameter | Type | Required   | Description
--------- | -----| :--------: | -----------
trade_url | string | + | The trade URL of the user to check
    
#### Output

Parameter | Type | Description
--------- | -----| -------- 
key_count | int  | Number of keys this user owns

