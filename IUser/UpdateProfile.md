## Update User Profile Data

Updates the current user's public profile data.

#### HTTP Request

`POST http://api.vgo.gg/IUser/UpdateProfile/v1/`

#### Input

Parameter | Type | Required   | Description
--------- | -----| :--------: | -----------
display_name | string  | - | Name to display on trade offers
inventory_is_private | boolean | - | Whether inventory is private (nobody can see it, even with token)
    
#### Output

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
            "username": null,
            "sms_phone": null,
            "contact_email": null,
            "inventory_is_private": false
        }
    }
}
```
