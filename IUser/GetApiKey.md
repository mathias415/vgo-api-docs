## Get API Key

#### HTTP Request

`GET http://api.vgo.gg/IUser/GetApiKey/v1/`

#### Input

Parameter | Type | Required   | Description
--------- | -----| :--------: | -----------
twofactor_code | int | + | 
    
#### Output

```json
{
    "status": 1,
    "time": 1525192486,
    "response": {
        "api_key": "z"
    }
}
```

```json
{
    "status": 1010,
    "time": 1525192425,
    "message": "Invalid two-factor code."
}
```