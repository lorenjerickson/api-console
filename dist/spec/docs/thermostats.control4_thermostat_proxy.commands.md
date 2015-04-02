### SET_SCALE
Command received from the proxy to establish the scale used in the HVAC system Fahrenheit or Celsius.

#### Parameters
| Parameter | Description |
|----------------|-------------|
| SCALE | (string) Fahrenheit or Celsius | 

#### Example Request URI

        
    PUT /api/v1/categories/thermostats/{id}/commands


Where {id} is the unique identifier of the device to which the command should be sent.

#### Example Request Body

       
    {
        "command": "SET_SCALE",
        "tParams": {
            "SCALE": "[value]",
        }
    }
    
### SET_SETPOINT_HEAT


#### Parameters
| Parameter | Description |
|----------------|-------------|
| KELVIN | (string) ex: 3042.61 | 

#### Example Request URI

        
    PUT /api/v1/categories/thermostats/{id}/commands


Where {id} is the unique identifier of the device to which the command should be sent.

#### Example Request Body

       
    {
        "command": "SET_SETPOINT_HEAT",
        "tParams": {
            "KELVIN": "[value]",
        }
    }
    
### SET_SETPOINT_COOL


#### Parameters
| Parameter | Description |
|----------------|-------------|
| KELVIN | (string) ex: 3042.61 | 

#### Example Request URI

        
    PUT /api/v1/categories/thermostats/{id}/commands


Where {id} is the unique identifier of the device to which the command should be sent.

#### Example Request Body

       
    {
        "command": "SET_SETPOINT_COOL",
        "tParams": {
            "KELVIN": "[value]",
        }
    }
    
### SET_MODE_HVAC
Command received from the proxy to establish the mode of the HVAC system

#### Parameters
| Parameter | Description |
|----------------|-------------|
| MODE | (string): Off, Heat, Cool, Auto, Emergency HeatThe parameters listed above are example values. The correct parameters for this command will be the ones provided in the capabilities section of your driver. | 

#### Example Request URI

        
    PUT /api/v1/categories/thermostats/{id}/commands


Where {id} is the unique identifier of the device to which the command should be sent.

#### Example Request Body

       
    {
        "command": "SET_MODE_HVAC",
        "tParams": {
            "MODE": "[value]",
        }
    }
    
### SET_MODE_FAN
Command received from the proxy to establish the mode of the fan.

#### Parameters
| Parameter | Description |
|----------------|-------------|
| MODE | (string): Auto, On.  The parameters listed above are example values. The correct parameters for this command will be the ones provided in the capabilities section of your driver | 

#### Example Request URI

        
    PUT /api/v1/categories/thermostats/{id}/commands


Where {id} is the unique identifier of the device to which the command should be sent.

#### Example Request Body

       
    {
        "command": "SET_MODE_FAN",
        "tParams": {
            "MODE": "[value]",
        }
    }
    
### SET_MODE_HOLD
Command received from the proxy to establish the mode of the hold function.

#### Parameters
| Parameter | Description |
|----------------|-------------|
| MODE | (string): For example: Off, 2 Hours, Permanent | 

#### Example Request URI

        
    PUT /api/v1/categories/thermostats/{id}/commands


Where {id} is the unique identifier of the device to which the command should be sent.

#### Example Request Body

       
    {
        "command": "SET_MODE_HOLD",
        "tParams": {
            "MODE": "[value]",
        }
    }
    
### SET_BUTTONS_LOCK
Command used to indicate if the buttons on the tHermostat should be locked out from controlling the temperature

#### Parameters
| Parameter | Description |
|----------------|-------------|
| LOCKED | (string): On or Off | 

#### Example Request URI

        
    PUT /api/v1/categories/thermostats/{id}/commands


Where {id} is the unique identifier of the device to which the command should be sent.

#### Example Request Body

       
    {
        "command": "SET_BUTTONS_LOCK",
        "tParams": {
            "LOCKED": "[value]",
        }
    }
    
### SET_VACATION_MODE
Command received from the proxy to establish or exclude �vacation mode� for the HVAC system.

#### Parameters
| Parameter | Description |
|----------------|-------------|
| MODE | (string): On or Off | 

#### Example Request URI

        
    PUT /api/v1/categories/thermostats/{id}/commands


Where {id} is the unique identifier of the device to which the command should be sent.

#### Example Request Body

       
    {
        "command": "SET_VACATION_MODE",
        "tParams": {
            "MODE": "[value]",
        }
    }
    
### INC_SETPOINT_HEAT


#### Example Request URI

        
    PUT /api/v1/categories/thermostats/{id}/commands


Where {id} is the unique identifier of the device to which the command should be sent.

#### Example Request Body

       
    {
        "command": "INC_SETPOINT_HEAT"
    }
    
### DEC_SETPOINT_HEAT


#### Example Request URI

        
    PUT /api/v1/categories/thermostats/{id}/commands


Where {id} is the unique identifier of the device to which the command should be sent.

#### Example Request Body

       
    {
        "command": "DEC_SETPOINT_HEAT"
    }
    
### INC_SETPOINT_COOL


#### Example Request URI

        
    PUT /api/v1/categories/thermostats/{id}/commands


Where {id} is the unique identifier of the device to which the command should be sent.

#### Example Request Body

       
    {
        "command": "INC_SETPOINT_COOL"
    }
    
### DEC_SETPOINT_COOL


#### Example Request URI

        
    PUT /api/v1/categories/thermostats/{id}/commands


Where {id} is the unique identifier of the device to which the command should be sent.

#### Example Request Body

       
    {
        "command": "DEC_SETPOINT_COOL"
    }
    
