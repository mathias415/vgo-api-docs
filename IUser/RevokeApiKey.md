## Revoke API Key

#### HTTP Request

`POST http://api.vgo.gg/IUser/RevokeApiKey/v1/`

#### Input

Parameter | Type | Required   | Description
--------- | -----| :--------: | -----------
twofactor_code | int | + | 
    
#### Output

```json
{
    "status": 1,
    "time": 1525192486
}
```

```json
{
    "status": 1010,
    "time": 1525192425,
    "message": "Invalid two-factor code."
}
```