## Get Contract Token From Steam Id

Gets the contract token for a user from their SteamID.  This contract token is used as a user ID inside the Ethereum contract.

All users should have a `contract_token` value.  In the event of a bug, `user_exists` can be used to determine if the user exists on VGO.gg even without a generated contract token.

#### HTTP Request

`GET http://api.vgo.gg/IUser/GetContractTokenFromSteamId/v1/`

#### Input

Parameter | Type | Required   | Description
--------- | -----| :--------: | -----------
steam_id | int | + | Steam 64-bit ID
    
#### Output

```json
{
    "status": 1,
    "time": 1525215888,
    "response": {
        "user_exists": true,
        "contract_token": 12345678901234567
    }
}
```

```json
{
    "status": 1,
    "time": 1525215888,
    "response": {
        "user_exists": false,
        "contract_token": null
    }
}
```