## Get current user's profile

#### HTTP Request

`GET http://api.vgo.gg/IUser/GetProfile/v1/`

#### Input

Parameter | Type | Required   | Description
--------- | -----| :--------: | -----------
with_extra | bool | - | Should we send extra user data, such as SMS phone and username?  Defaults to false
    
#### Output

Parameter | Type | Description
--------- | -----| -------- 
user     | object | Holds user info
- id | int | Internal user ID
- steam_id | string | Steam id64 integer as a string
- display_name | string | Display name
- avatar | string | URL to avatar
- twofactor_enabled | boolean | Whether or not user has Two-Factor Auth enabled.
- api_key_exists | boolean | See whether user has API Key
- username | string/null | (Optional via `with_extra`) Account username
- sms_phone | string/null | (Optional via `with_extra`) Phone number used for SMS verification
- contact_email | string/null | (Optional via `with_extra`) Email address
- inventory_is_private | boolean | (Optional via `with_extra`) Set whether inventory is private (nobody can see it, even with token)

#### Output Example

```json
{
    "status": 1,
    "time": 1524873227,
    "response": {
        "user": {
            "id": 1,
            "steam_id": "123456",
            "display_name": "Shifty",
            "avatar": null,
            "twofactor_enabled": false,
            "username": null,
            "sms_phone": null,
            "contact_email": null,
            "inventory_is_private": false,
            "api_key_exists": false
        }
    }
}
```