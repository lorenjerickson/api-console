### BUTTON_ACTION
Used to perform a button action on the device. Useful if you want to do user dependent hold/release functionality

#### Parameters
| Parameter | Description |
|----------------|-------------|
| BUTTON_ID | integer. ACTION (see events for the values for action) replaces the old click_toggle_button, hold_top_button, etc. commands from the v1 light proxy and rolls them into one command | 
| ACTION | (see events for Actions) | 

#### Example Request URI

        
    PUT /api/v1/categories/lights/{id}/commands


Where {id} is the unique identifier of the device to which the command should be sent.

#### Example Request Body

       
    {
        "command": "BUTTON_ACTION",
        "tParams": {
            "BUTTON_ID": "[value]",
            "ACTION": "[value]",
        }
    }
    
### GET_CONNECTED_STATE
Used to determine if a device is online/offline

#### Example Request URI

        
    PUT /api/v1/categories/lights/{id}/commands


Where {id} is the unique identifier of the device to which the command should be sent.

#### Example Request Body

       
    {
        "command": "GET_CONNECTED_STATE"
    }
    
### GET_LIGHT_LEVEL
Gets the current level of the light.

#### Example Request URI

        
    PUT /api/v1/categories/lights/{id}/commands


Where {id} is the unique identifier of the device to which the command should be sent.

#### Example Request Body

       
    {
        "command": "GET_LIGHT_LEVEL"
    }
    
### GET_PROPERTIES


#### Example Request URI

        
    PUT /api/v1/categories/lights/{id}/commands


Where {id} is the unique identifier of the device to which the command should be sent.

#### Example Request Body

       
    {
        "command": "GET_PROPERTIES"
    }
    
### OFF
Used to the turn light off

#### Example Request URI

        
    PUT /api/v1/categories/lights/{id}/commands


Where {id} is the unique identifier of the device to which the command should be sent.

#### Example Request Body

       
    {
        "command": "OFF"
    }
    
### ON
Turns the light on. If it is a dimmer, it will move to the preset_level

#### Example Request URI

        
    PUT /api/v1/categories/lights/{id}/commands


Where {id} is the unique identifier of the device to which the command should be sent.

#### Example Request Body

       
    {
        "command": "ON"
    }
    
### RAMP_TO_LEVEL
Ramps a light to a particular level in a defined amount of time

#### Parameters
| Parameter | Description |
|----------------|-------------|
| LEVEL | (0-100) | 
| TIME | (in ms. 0 is instant) | 

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
    
### SET_ALL_LED
Sets the LED color of all the buttons on the device to one color (both on/off colors)

#### Parameters
| Parameter | Description |
|----------------|-------------|
| COLOR | (str- 6 character hex) Optional, representing an RGB value | 

#### Example Request URI

        
    PUT /api/v1/categories/lights/{id}/commands


Where {id} is the unique identifier of the device to which the command should be sent.

#### Example Request Body

       
    {
        "command": "SET_ALL_LED",
        "tParams": {
            "COLOR": "[value]",
        }
    }
    
### SET_BUTTON_COLOR
Used to set the color for a particular button for when the light is on/off

#### Parameters
| Parameter | Description |
|----------------|-------------|
| BUTTON_ID | (int) Number representing the button. | 
| ON_COLOR | (str-6 character hex) Optional, representing an RGB value | 
| OFF_COLOR | (str-6 character hex) Optional, representing an RGB value | 

#### Example Request URI

        
    PUT /api/v1/categories/lights/{id}/commands


Where {id} is the unique identifier of the device to which the command should be sent.

#### Example Request Body

       
    {
        "command": "SET_BUTTON_COLOR",
        "tParams": {
            "BUTTON_ID": "[value]",
            "ON_COLOR": "[value]",
            "OFF_COLOR": "[value]",
        }
    }
    
### SET_CLICK_RATE_UP
Sets the click rate up for the device

#### Parameters
| Parameter | Description |
|----------------|-------------|
| RATE | (int) - In milliseconds | 

#### Example Request URI

        
    PUT /api/v1/categories/lights/{id}/commands


Where {id} is the unique identifier of the device to which the command should be sent.

#### Example Request Body

       
    {
        "command": "SET_CLICK_RATE_UP",
        "tParams": {
            "RATE": "[value]",
        }
    }
    
### SET_CLICK_RATE_DOWN
Set the click rate down for the device

#### Parameters
| Parameter | Description |
|----------------|-------------|
| RATE | (int) - In milliseconds | 

#### Example Request URI

        
    PUT /api/v1/categories/lights/{id}/commands


Where {id} is the unique identifier of the device to which the command should be sent.

#### Example Request Body

       
    {
        "command": "SET_CLICK_RATE_DOWN",
        "tParams": {
            "RATE": "[value]",
        }
    }
    
### SET_COLD_START_LEVEL
Sets the cold start level for the device

#### Parameters
| Parameter | Description |
|----------------|-------------|
| LEVEL | (0-100) | 

#### Example Request URI

        
    PUT /api/v1/categories/lights/{id}/commands


Where {id} is the unique identifier of the device to which the command should be sent.

#### Example Request Body

       
    {
        "command": "SET_COLD_START_LEVEL",
        "tParams": {
            "LEVEL": "[value]",
        }
    }
    
### SET_COLD_START_TIME
Sets the cold start time for the device

#### Parameters
| Parameter | Description |
|----------------|-------------|
| TIME | (int) - In milliseconds. | 

#### Example Request URI

        
    PUT /api/v1/categories/lights/{id}/commands


Where {id} is the unique identifier of the device to which the command should be sent.

#### Example Request Body

       
    {
        "command": "SET_COLD_START_TIME",
        "tParams": {
            "TIME": "[value]",
        }
    }
    
### SET_HOLD_RATE_DOWN
Sets the hold rate down for the device

#### Parameters
| Parameter | Description |
|----------------|-------------|
| RATE | (int) - In milliseconds | 

#### Example Request URI

        
    PUT /api/v1/categories/lights/{id}/commands


Where {id} is the unique identifier of the device to which the command should be sent.

#### Example Request Body

       
    {
        "command": "SET_HOLD_RATE_DOWN",
        "tParams": {
            "RATE": "[value]",
        }
    }
    
### SET_HOLD_RATE_UP
Sets the hold rate up for the device

#### Parameters
| Parameter | Description |
|----------------|-------------|
| RATE | (int) - In milliseconds | 

#### Example Request URI

        
    PUT /api/v1/categories/lights/{id}/commands


Where {id} is the unique identifier of the device to which the command should be sent.

#### Example Request Body

       
    {
        "command": "SET_HOLD_RATE_UP",
        "tParams": {
            "RATE": "[value]",
        }
    }
    
### SET_LEVEL
Sets the current level of the light. There is no ramping, this is an instant movement.

#### Parameters
| Parameter | Description |
|----------------|-------------|
| LEVEL | (int) - (0-100) For a switch, it should be 0 or 100 only. | 

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
    
### SET_MAX_ON_LEVEL
Used to set the maximum on level for the device

#### Parameters
| Parameter | Description |
|----------------|-------------|
| LEVEL | (int) - (0-100) | 

#### Example Request URI

        
    PUT /api/v1/categories/lights/{id}/commands


Where {id} is the unique identifier of the device to which the command should be sent.

#### Example Request Body

       
    {
        "command": "SET_MAX_ON_LEVEL",
        "tParams": {
            "LEVEL": "[value]",
        }
    }
    
### SET_MIN_ON_LEVEL
Used to set the minimum on level for the device

#### Parameters
| Parameter | Description |
|----------------|-------------|
| LEVEL | (int) - 0-100 | 

#### Example Request URI

        
    PUT /api/v1/categories/lights/{id}/commands


Where {id} is the unique identifier of the device to which the command should be sent.

#### Example Request Body

       
    {
        "command": "SET_MIN_ON_LEVEL",
        "tParams": {
            "LEVEL": "[value]",
        }
    }
    
### SET_PRESET_LEVEL
Sets preset level for the device

#### Parameters
| Parameter | Description |
|----------------|-------------|
| LEVEL | (int) - 0-100 | 

#### Example Request URI

        
    PUT /api/v1/categories/lights/{id}/commands


Where {id} is the unique identifier of the device to which the command should be sent.

#### Example Request Body

       
    {
        "command": "SET_PRESET_LEVEL",
        "tParams": {
            "LEVEL": "[value]",
        }
    }
    
### TOGGLE
Toggles the light. If it is a dimmer and it is off, toggling it should set its level to preset_level

#### Example Request URI

        
    PUT /api/v1/categories/lights/{id}/commands


Where {id} is the unique identifier of the device to which the command should be sent.

#### Example Request Body

       
    {
        "command": "TOGGLE"
    }
    
