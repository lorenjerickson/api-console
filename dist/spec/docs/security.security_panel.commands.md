### BUTTON_LIST
Get the button list from the protocol driver?

#### Example Request URI

        
    PUT /api/v1/categories/security/{id}/commands


Where {id} is the unique identifier of the device to which the command should be sent.

#### Example Request Body

       
    {
        "command": "BUTTON_LIST"
    }
    
### BUTTON_PRESS


#### Parameters
| Parameter | Description |
|----------------|-------------|
| ButtonID | int(button id) | 

#### Example Request URI

        
    PUT /api/v1/categories/security/{id}/commands


Where {id} is the unique identifier of the device to which the command should be sent.

#### Example Request Body

       
    {
        "command": "BUTTON_PRESS",
        "tParams": {
            "ButtonID": "[value]",
        }
    }
    
