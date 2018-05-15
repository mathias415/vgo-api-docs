## Send a 6-digit email verification code to user

#### HTTP Request

`POST http://api.vgo.gg/IUser/SendEmailCode/v1/`

#### Input

Parameter | Type | Required   | Description
--------- | -----| :--------: | -----------
_none_ | | | 
    
#### Output

```json
{
  "status": 1,
  "time": 1524881473
}
```

```json
{
  "status": 3008,
  "time": 1525113003,
  "message": "Email code already sent. Please try again in 59 seconds."
}
```