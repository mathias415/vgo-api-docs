## Verify 6-digit email code provided by user

After successful verification, user's session will be considered verified for 5 minutes.
Front-end implementation should take this into account. This is so that we do not repeatedly ask the user for email code verification. If this endpoint is called within the 5 minute window, it will return a success state, without any code validation.

#### HTTP Request

`POST http://api.vgo.gg/IUser/VerifyEmailCode/v1/`

#### Input

Parameter | Type | Required   | Description
--------- | -----| :--------: | -----------
code | int | + | 6-digit email code
    
#### Output

```json
{
  "status": 1,
  "time": 1524881473
}
```

There is a 15-second feature rate limit for this endpoint to prevent brute force attacks.
```json
{
  "status": 3008,
  "time": 1525111886,
  "message": "Rate limit exceeded."
}
```