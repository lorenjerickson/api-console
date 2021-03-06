### ON
Turn the fan on to the designated preset level. Another possible behavior would be to turn it back on to the most recent on speed.

#### Example Request URI

        
    PUT /api/v1/categories/lights/{id}/commands


Where {id} is the unique identifier of the device to which the command should be sent.

#### Example Request Body

       
    {
        "command": "ON"
    }
    
### OFF
Turns the fan off.

#### Example Request URI

        
    PUT /api/v1/categories/lights/{id}/commands


Where {id} is the unique identifier of the device to which the command should be sent.

#### Example Request Body

       
    {
        "command": "OFF"
    }
    
### TOGGLE
If the fan is on, turn it off. If the fan is off, do the same behavior as the ON command.

#### Example Request URI

        
    PUT /api/v1/categories/lights/{id}/commands


Where {id} is the unique identifier of the device to which the command should be sent.

#### Example Request Body

       
    {
        "command": "TOGGLE"
    }
    
### DESIGNATE_PRESET
Specifies which fan preset value should be the default one to go to when an ON or TOGGLE command is sent.

#### Parameters
| Parameter | Description |
|----------------|-------------|
| PRESET | valid values: 1 � N | 

#### Example Request URI

        
    PUT /api/v1/categories/lights/{id}/commands


Where {id} is the unique identifier of the device to which the command should be sent.

#### Example Request Body

       
    {
        "command": "DESIGNATE_PRESET",
        "tParams": {
            "PRESET": "[value]",
        }
    }
    
### SET_SPEED
Setthecurrentspeedofthefantothedesignatedlevel. Settingto0willturnthefanoff.

#### Parameters
| Parameter | Description |
|----------------|-------------|
| SPEED | valid values: 0 � N | 

#### Example Request URI

        
    PUT /api/v1/categories/lights/{id}/commands


Where {id} is the unique identifier of the device to which the command should be sent.

#### Example Request Body

       
    {
        "command": "SET_SPEED",
        "tParams": {
            "SPEED": "[value]",
        }
    }
    
### CYCLE_SPEED_UP
Bump the fan up to the next higher speed from its current setting. It would be up to the protocol driver to decide if it wraps or stops when we're already at the highest speed

#### Example Request URI

        
    PUT /api/v1/categories/lights/{id}/commands


Where {id} is the unique identifier of the device to which the command should be sent.

#### Example Request Body

       
    {
        "command": "CYCLE_SPEED_UP"
    }
    
### CYCLE_SPEED_DOWN
Bump the fan down to the next lower speed from its current setting. It would be up to the protocol driver to decide if it wraps or stops when the fan is currently off.

#### Example Request URI

        
    PUT /api/v1/categories/lights/{id}/commands


Where {id} is the unique identifier of the device to which the command should be sent.

#### Example Request Body

       
    {
        "command": "CYCLE_SPEED_DOWN"
    }
    
### SET_DIRECTION
Tell the fan which direction to spin. This command would only be valid if the can_reverse capability is set to true in the C4i file.

#### Parameters
| Parameter | Description |
|----------------|-------------|
| DIRECTION | Valid values: Forward/Reverse | 

#### Example Request URI

        
    PUT /api/v1/categories/lights/{id}/commands


Where {id} is the unique identifier of the device to which the command should be sent.

#### Example Request Body

       
    {
        "command": "SET_DIRECTION",
        "tParams": {
            "DIRECTION": "[value]",
        }
    }
    
### TOGGLE_DIRECTION
Reversethedirectionwhichthefaniscurrentlyspinning. Thiscommandwouldonlybevalidifthe can_reverse capability is set to true in the C4i file.

#### Example Request URI

        
    PUT /api/v1/categories/lights/{id}/commands


Where {id} is the unique identifier of the device to which the command should be sent.

#### Example Request Body

       
    {
        "command": "TOGGLE_DIRECTION"
    }
    
### GET_CURRENT_STATE
Tell the protocol to report its current values. This wouldn't be available through programming, but generated by the proxy to get its initial settings.

#### Example Request URI

        
    PUT /api/v1/categories/lights/{id}/commands


Where {id} is the unique identifier of the device to which the command should be sent.

#### Example Request Body

       
    {
        "command": "GET_CURRENT_STATE"
    }
    
### GET_STATE
Command handled by the proxy driver. Immediately returns a block of XML information to the caller. Reports the current state of the device.

#### Example Request URI

        
    PUT /api/v1/categories/lights/{id}/commands


Where {id} is the unique identifier of the device to which the command should be sent.

#### Example Request Body

       
    {
        "command": "GET_STATE"
    }
    
### GET_SETUP


#### Example Request URI

        
    PUT /api/v1/categories/lights/{id}/commands


Where {id} is the unique identifier of the device to which the command should be sent.

#### Example Request Body

       
    {
        "command": "GET_SETUP"
    }
    
