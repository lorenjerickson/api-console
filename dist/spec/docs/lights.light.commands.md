### ON


#### Example Request URI

        
    PUT /api/v1/categories/lights/{id}/commands


Where {id} is the unique identifier of the device to which the command should be sent.

#### Example Request Body

       
    {
        "command": "ON"
    }
    
### OFF


#### Example Request URI

        
    PUT /api/v1/categories/lights/{id}/commands


Where {id} is the unique identifier of the device to which the command should be sent.

#### Example Request Body

       
    {
        "command": "OFF"
    }
    
### TOGGLE


#### Example Request URI

        
    PUT /api/v1/categories/lights/{id}/commands


Where {id} is the unique identifier of the device to which the command should be sent.

#### Example Request Body

       
    {
        "command": "TOGGLE"
    }
    
### SET_LEVEL


#### Parameters
| Parameter | Description |
|----------------|-------------|
| LEVEL | int (0-100) | 

#### Example Request URI

        
    PUT /api/v1/categories/lights/{id}/commands


Where {id} is the unique identifier of the device to which the command should be sent.

#### Example Request Body

       
    {
        "command": "SET_LEVEL",
        "tParams": {
            "LEVEL": "[value]",
        }
    }
    
### RAMP_TO_LEVEL


#### Parameters
| Parameter | Description |
|----------------|-------------|
| LEVEL | int (0-100) | 
| TIME | int (n ms) | 

#### Example Request URI

        
    PUT /api/v1/categories/lights/{id}/commands


Where {id} is the unique identifier of the device to which the command should be sent.

#### Example Request Body

       
    {
        "command": "RAMP_TO_LEVEL",
        "tParams": {
            "LEVEL": "[value]",
            "TIME": "[value]",
        }
    }
    
