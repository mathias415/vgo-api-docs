## Get Steam OpenID login URL

#### HTTP Request

`GET http://api.vgo.gg/IAuth/GetSteamLoginURL/v1/`

#### Input

Parameter | Type | Required   | Description
--------- | -----| :--------: | -----------
none | | | 
    
#### Output

```json
{
    "status": 1,
    "time": 1525199758,
    "response": {
        "steam_login_url": "https://steamcommunity.com/openid/login?openid.ns=http%3A%2F%2Fspecs.openid.net%2Fauth%2F2.0&openid.mode=checkid_setup&openid.return_to=http%3A%2F%2Fvgo.gg%2Fsteam_signin.php&openid.realm=http%3A%2F%2Fvgo.gg&openid.identity=http%3A%2F%2Fspecs.openid.net%2Fauth%2F2.0%2Fidentifier_select&openid.claimed_id=http%3A%2F%2Fspecs.openid.net%2Fauth%2F2.0%2Fidentifier_select"
    }
}