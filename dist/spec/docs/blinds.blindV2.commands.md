### BLINDS_AT_PRESET
Both command and a protocol notification. When sent to the protocol, blinds are positioned at the preset level. When returned from the protocol it will contain the preset level value.

#### Parameters
| Parameter | Description |
|----------------|-------------|
| Int | 0 - 100 | 

#### Example Request URI

        
    PUT /api/v1/categories/blinds/{id}/commands


Where {id} is the unique identifier of the device to which the command should be sent.

#### Example Request Body

       
    {
        "command": "BLINDS_AT_PRESET",
        "tParams": {
            "Int": "[value]",
        }
    }
    
### BLINDS_CLOSED
Close Blinds

#### Example Request URI

        
    PUT /api/v1/categories/blinds/{id}/commands


Where {id} is the unique identifier of the device to which the command should be sent.

#### Example Request Body

       
    {
        "command": "BLINDS_CLOSED"
    }
    
### BLINDS_GOTO_LEVEL
Position all blinds at a level location.

#### Example Request URI

        
    PUT /api/v1/categories/blinds/{id}/commands


Where {id} is the unique identifier of the device to which the command should be sent.

#### Example Request Body

       
    {
        "command": "BLINDS_GOTO_LEVEL"
    }
    
### BLINDS_GOTO_PRESET
Position blinds to a preset location.

#### Example Request URI

        
    PUT /api/v1/categories/blinds/{id}/commands


Where {id} is the unique identifier of the device to which the command should be sent.

#### Example Request Body

       
    {
        "command": "BLINDS_GOTO_PRESET"
    }
    
### BLINDS_OPEN
Open Blinds

#### Example Request URI

        
    PUT /api/v1/categories/blinds/{id}/commands


Where {id} is the unique identifier of the device to which the command should be sent.

#### Example Request Body

       
    {
        "command": "BLINDS_OPEN"
    }
    
### BLINDS_LEVEL
Command sent to the protocol which returns the current level of the blind.

#### Example Request URI

        
    PUT /api/v1/categories/blinds/{id}/commands


Where {id} is the unique identifier of the device to which the command should be sent.

#### Example Request Body

       
    {
        "command": "BLINDS_LEVEL"
    }
    
### BLINDS_STOP
Stop movement of Blinds

#### Example Request URI

        
    PUT /api/v1/categories/blinds/{id}/commands


Where {id} is the unique identifier of the device to which the command should be sent.

#### Example Request Body

       
    {
        "command": "BLINDS_STOP"
    }
    
### BLINDS_TOGGLE
Toggle blinds Up/Down.

#### Example Request URI

        
    PUT /api/v1/categories/blinds/{id}/commands


Where {id} is the unique identifier of the device to which the command should be sent.

#### Example Request Body

       
    {
        "command": "BLINDS_TOGGLE"
    }
    
### lOUVERS_AT_LEVEL
Command sent to the protocol which returns the current level of the louver.

#### Example Request URI

        
    PUT /api/v1/categories/blinds/{id}/commands


Where {id} is the unique identifier of the device to which the command should be sent.

#### Example Request Body

       
    {
        "command": "lOUVERS_AT_LEVEL"
    }
    
### LOUVERS_AT_PRESET
Both command and a protocol notification. When sent to the protocol, louvers are positioned at the preset level. When returned from the protocol it will contain the preset level value.

#### Parameters
| Parameter | Description |
|----------------|-------------|
| Int | 0 - 100 | 

#### Example Request URI

        
    PUT /api/v1/categories/blinds/{id}/commands


Where {id} is the unique identifier of the device to which the command should be sent.

#### Example Request Body

       
    {
        "command": "LOUVERS_AT_PRESET",
        "tParams": {
            "Int": "[value]",
        }
    }
    
### LOUVERS_CLOSE
Close louvers on blinds.

#### Example Request URI

        
    PUT /api/v1/categories/blinds/{id}/commands


Where {id} is the unique identifier of the device to which the command should be sent.

#### Example Request Body

       
    {
        "command": "LOUVERS_CLOSE"
    }
    
### LOUVERS_GOTO_LEVEL
Position all blinds at a level location.

#### Example Request URI

        
    PUT /api/v1/categories/blinds/{id}/commands


Where {id} is the unique identifier of the device to which the command should be sent.

#### Example Request Body

       
    {
        "command": "LOUVERS_GOTO_LEVEL"
    }
    
### LOUVERS_GOTO_PRESET
Position louvers at a predefined position.

#### Example Request URI

        
    PUT /api/v1/categories/blinds/{id}/commands


Where {id} is the unique identifier of the device to which the command should be sent.

#### Example Request Body

       
    {
        "command": "LOUVERS_GOTO_PRESET"
    }
    
### LOUVERS_OPEN
Open louvers on blinds.

#### Example Request URI

        
    PUT /api/v1/categories/blinds/{id}/commands


Where {id} is the unique identifier of the device to which the command should be sent.

#### Example Request Body

       
    {
        "command": "LOUVERS_OPEN"
    }
    
### LOUVERS_STOP
Stop louvers.

#### Example Request URI

        
    PUT /api/v1/categories/blinds/{id}/commands


Where {id} is the unique identifier of the device to which the command should be sent.

#### Example Request Body

       
    {
        "command": "LOUVERS_STOP"
    }
    
### LOUVERS_TOGGLE


#### Example Request URI

        
    PUT /api/v1/categories/blinds/{id}/commands


Where {id} is the unique identifier of the device to which the command should be sent.

#### Example Request Body

       
    {
        "command": "LOUVERS_TOGGLE"
    }
    
