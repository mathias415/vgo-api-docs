## Get your account's trade URL, allowing p2p trading.

#### HTTP Request

`GET http://api.vgo.gg/ITrade/GetTradeURL/v1/`

#### Input

Parameter | Type | Required   | Description
--------- | -----| :--------: | -----------
_none_ | | | 
    
#### Output

Parameter | Type | Description
--------- | -----| -------- 
uid       | int    | Your VGO account's user ID
token     | string | Your VGO trade token
long_url  | string | The actual URL you should go to in order to send a VGO trade offer to your account.
short_url | string | A shortened alias for `long_url` of the type "http://vgo.gg/t/1/gr3asm11". This redirects to the long URL. 


