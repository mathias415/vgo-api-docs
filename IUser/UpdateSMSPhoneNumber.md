## Update SMS phone number

#### HTTP Request

`POST http://api.vgo.gg/IUser/UpdateSMSPhoneNumber/v1/`

#### Input

Parameter | Type | Required   | Description
--------- | -----| :--------: | -----------
sms_phone | string | + | SMS phone number
phone_login_verification | bool | - | Use phone login verification
    
#### Output

```json
{
    "status": 1,
    "time": 1525193680,
    "response": {
        "sms_phone": "+171412312324",
        "phone_login_verification": false,
        "validation_sms_sent": true
    }
}
```
