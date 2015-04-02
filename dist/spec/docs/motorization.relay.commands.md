### CLOSE


#### Example Request URI

        
    PUT /api/v1/categories/motorization/{id}/commands


Where {id} is the unique identifier of the device to which the command should be sent.

#### Example Request Body

       
    {
        "command": "CLOSE"
    }
    
### OPEN


#### Example Request URI

        
    PUT /api/v1/categories/motorization/{id}/commands


Where {id} is the unique identifier of the device to which the command should be sent.

#### Example Request Body

       
    {
        "command": "OPEN"
    }
    
### TOGGLE


#### Example Request URI

        
    PUT /api/v1/categories/motorization/{id}/commands


Where {id} is the unique identifier of the device to which the command should be sent.

#### Example Request Body

       
    {
        "command": "TOGGLE"
    }
    
### TRIGGER
Pulse relay closed for a specified time

#### Parameters
| Parameter | Description |
|----------------|-------------|
| TIME | INT)nMilliseconds | 

#### Example Request URI

        
    PUT /api/v1/categories/motorization/{id}/commands


Where {id} is the unique identifier of the device to which the command should be sent.

#### Example Request Body

       
    {
        "command": "TRIGGER",
        "tParams": {
            "TIME": "[value]",
        }
    }
    
