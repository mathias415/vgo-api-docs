## Get case schema

#### HTTP Request

`GET http://api.vgo.gg/ICase/GetCaseSchema/v1`

#### Authorization
Doesn't require any authorization

#### Input

Parameter | Type | Required   | Description
--------- | -----| :--------: | -----------
cases | string | - | A comma-separated string of integer case ids. If sent, limit output to these specific cases. Sends all cases otherwise
    
#### Output

Parameter | Type | Description
--------- | -----| -------- 
cases     | array-object | cases list
  - id    | int | case id
  - name  | string | case name
  - image | string | case image url
  - skus  | array | List of integers - item skus in the case

