### SET_SPA_MODE


#### Parameters
| Parameter | Description |
|----------------|-------------|
| SPAMODE | ON, OFF | 

#### Example Request URI

        
    PUT /api/v1/categories/pools/{id}/commands


Where {id} is the unique identifier of the device to which the command should be sent.

#### Example Request Body

       
    {
        "command": "SET_SPA_MODE",
        "tParams": {
            "SPAMODE": "[value]",
        }
    }
    
### SET_PUMP_MODE


#### Parameters
| Parameter | Description |
|----------------|-------------|
| PUMPMODE | ON, OFF | 

#### Example Request URI

        
    PUT /api/v1/categories/pools/{id}/commands


Where {id} is the unique identifier of the device to which the command should be sent.

#### Example Request Body

       
    {
        "command": "SET_PUMP_MODE",
        "tParams": {
            "PUMPMODE": "[value]",
        }
    }
    
### SET_POOL_SETPOINT


#### Parameters
| Parameter | Description |
|----------------|-------------|
| SETPOINT | int (temp value to send to protocol driver) | 

#### Example Request URI

        
    PUT /api/v1/categories/pools/{id}/commands


Where {id} is the unique identifier of the device to which the command should be sent.

#### Example Request Body

       
    {
        "command": "SET_POOL_SETPOINT",
        "tParams": {
            "SETPOINT": "[value]",
        }
    }
    
### SET_SPA_SETPOINT


#### Parameters
| Parameter | Description |
|----------------|-------------|
| SETPOINT | int (temp value to send to protocol driver) | 

#### Example Request URI

        
    PUT /api/v1/categories/pools/{id}/commands


Where {id} is the unique identifier of the device to which the command should be sent.

#### Example Request Body

       
    {
        "command": "SET_SPA_SETPOINT",
        "tParams": {
            "SETPOINT": "[value]",
        }
    }
    
### BUTTON_LIST


#### Example Request URI

        
    PUT /api/v1/categories/pools/{id}/commands


Where {id} is the unique identifier of the device to which the command should be sent.

#### Example Request Body

       
    {
        "command": "BUTTON_LIST"
    }
    
### BUTTON_PRESS
Received from the proxy when an Aux button has been pressed. This may include the Aux Buttons assigned to the Pool and Spa Heaters, in the capabilities section of the driver.  See API Items - Get Capabilities

#### Parameters
| Parameter | Description |
|----------------|-------------|
| MODE | ON, OFF | 
| ButtonID | int(button id ) | 

#### Example Request URI

        
    PUT /api/v1/categories/pools/{id}/commands


Where {id} is the unique identifier of the device to which the command should be sent.

#### Example Request Body

       
    {
        "command": "BUTTON_PRESS",
        "tParams": {
            "MODE": "[value]",
            "ButtonID": "[value]",
        }
    }
    
### CURRENT_SETTINGS
Received from the proxy the UI needs to get the current settings for the pool. This command should be responded to via sending a CURRENT_SETTINGS notify to the proxy, with the current values for all pool controller settings.

#### Example Request URI

        
    PUT /api/v1/categories/pools/{id}/commands


Where {id} is the unique identifier of the device to which the command should be sent.

#### Example Request Body

       
    {
        "command": "CURRENT_SETTINGS"
    }
    
