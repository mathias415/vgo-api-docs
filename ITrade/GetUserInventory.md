## Get trade offer recipient's inventory.

#### HTTP Request

`GET http://api.vgo.gg/ITrade/GetUserInventory/v1/`

#### Input

Parameter | Type | Required   | Description
--------- | -----| :--------: | -----------
uid | int |  <p_required>+</p_required> | User ID of user whose inventory you want to see 
token | string |  <p_required>+</p_required> | Trade token of user whose inventory you want to see offer to
page | int | - | page number in response (starting with 1, default to 1) 
per_page | int | - | number of items per_page in response (no more then 100)
search | string | - | additional search by item's name 
    
#### Output

Parameter | Type | Description
--------- | -----| -------- 
total     | int    | Total number of items (filtered, if search parameter is passed)
items | array-object | items list, based on pagination and search filters. All items are in standard item format (see in [VGO-API-Documentation](VGO-API-Documentation))
user_data | array-object | Public information of user whose inventory you want to see. (see format in [IUser](IUser))



