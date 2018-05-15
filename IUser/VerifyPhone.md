## Verify 6-digit SMS code provided by user

If a user attempts too many incorrect SMS codes (default 20, subject to change), they will be locked out from future attempts for 1 hour (default value, subject to change).

#### HTTP Request

`POST http://api.vgo.gg/IUser/VerifyPhone/v1/`

#### Input

Parameter | Type | Required   | Description
--------- | -----| :--------: | -----------
code      | int  | + | 6-digit SMS code
    
#### Output

```json
{
  "status": 1,
  "time": 1524881473
}
```