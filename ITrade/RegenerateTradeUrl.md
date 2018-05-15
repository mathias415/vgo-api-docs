## Regenerate your account's trade URL for p2p trading, invalidating the old one.

#### HTTP Request

`POST http://api.vgo.gg/ITrade/RegenerateTradeURL/v1/`

#### Input

Parameter | Type | Required   | Description
--------- | -----| :--------: | -----------
_none_ | | | 
    
#### Output

Parameter | Type | Description
--------- | -----| -------- 
uid       | int    | Your VGO account's user ID
token     | string | Your new VGO trade token
long_url  | string | The actual URL you should go to in order to send VGO trade offer to your account.
short_url | string | A shortened alias for `long_url` of the type "http://vgo.gg/t/1/gr3asm11". This redirects to the long URL. 

