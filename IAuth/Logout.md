## Logout

Requires cookie-based authentication.  Errors on other auth type or if you're not logged in.

#### HTTP Request

`GET|POST http://api.vgo.gg/IAuth/Logout/v1/`

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
        "logged_out": true
    }
}
```