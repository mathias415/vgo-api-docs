## Login using Steam OpenID callback data

Note that this method checks authentication with Steam again after OpenID signin.

#### HTTP Request

`POST http://api.vgo.gg/IAuth/ExecuteSteamLogin/v1/`

#### Input

- If user has 2FA & Steam login was successful, status code will be `1005`, and user's authenticated id64 will be saved in the session. A `2FA input` should popup for the user, once they enter, you may post to this endpoint once again with only the `twofactor_code` and it should log them in.

Parameter | Type | Required   | Description
--------- | -----| :--------: | -----------
twofactor_code | int | if has 2FA |
openid_ns | string | x |
openid_mode | string | x |
openid_op_endpoint | string | x |
openid_claimed_id | string | x |
openid_identity | string | x |
openid_return_to | string | x |
openid_response_nonce | string | x |
openid_assoc_handle | int | x |
openid_signed | string | x |
openid_sig | string | x |
   
#### Output

