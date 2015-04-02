### DEC_SETPOINT_COOL
Used to decrease the cool set point by 1. This command is handled by the proxy, and ends up creating a SET_SETPOINT_COOL command to send to the protocol driver, unless the capability can_inc_dec_setpoints is set to true.

#### Example Request URI

        
    PUT /api/v1/categories/thermostats/{id}/commands


Where {id} is the unique identifier of the device to which the command should be sent.

#### Example Request Body

       
    {
        "command": "DEC_SETPOINT_COOL"
    }
    
### SET_PRESET
Runs a Preset regardless if there is an event scheduled for it.

#### Parameters
| Parameter | Description |
|----------------|-------------|
| NAME | (string) the name of the preset to be activated | 

#### Example Request URI

        
    PUT /api/v1/categories/thermostats/{id}/commands


Where {id} is the unique identifier of the device to which the command should be sent.

#### Example Request Body

       
    {
        "command": "SET_PRESET",
        "tParams": {
            "NAME": "[value]",
        }
    }
    
### DEC_SETPOINT_HEAT
Used to decrease the heat set point by 1. This command is handled by the proxy, and ends up creating a SET_SETPOINT_HEAT command to send to the protocol driver, unless the capability can_inc_dec_setpoints is set to true.

#### Example Request URI

        
    PUT /api/v1/categories/thermostats/{id}/commands


Where {id} is the unique identifier of the device to which the command should be sent.

#### Example Request Body

       
    {
        "command": "DEC_SETPOINT_HEAT"
    }
    
### INC_SETPOINT_COOL
Used to increase the cool set point by 1. This command is handled by the proxy, and ends up creating a SET_SETPOINT_COOL command to send to the protocol driver, unless the capability can_inc_dec_setpoints is set to true.

#### Example Request URI

        
    PUT /api/v1/categories/thermostats/{id}/commands


Where {id} is the unique identifier of the device to which the command should be sent.

#### Example Request Body

       
    {
        "command": "INC_SETPOINT_COOL"
    }
    
### INC_SETPOINT_HEAT
Used to increase the heat set point by 1. This command is handled by the proxy, and ends up creating a SET_SETPOINT_HEAT command to send to the protocol driver, unless the capability can_inc_dec_setpoints is set to true.

#### Example Request URI

        
    PUT /api/v1/categories/thermostats/{id}/commands


Where {id} is the unique identifier of the device to which the command should be sent.

#### Example Request Body

       
    {
        "command": "INC_SETPOINT_HEAT"
    }
    
### PRESET_ADD
Adds a new Preset Schedule Preset (If protocol driver has the "can_preset_schedule" capability)

#### Parameters
| Parameter | Description |
|----------------|-------------|
| NAME | (string) (required) the name of the preset to be added | 
| PRESET_FIELDS | (xml) If a UI or Driver sends a bound call with a string that has invalid XML syntax, this field will be set to <preset_field/> and an error message will be logged to director.log when this occurs. Note that only a driver OR UI should specify the _f or c. For example: heat_setpoint_f, cool_setpoint_f, heat_setpoint_c, cool_setpoint_c but not both. The proxy will auto insert the missing _f or _c based on the scales resolution if it detects one side is not supplied. This makes it so UI's and drivers do not need to calculatethecorrectvalueforthescale. However, if a driver or UI does want to calculate it,the proxy will leave the value alone. In the same manner the proxy will not correct or change anything if the _f and _c do not resolve to the equivalent temperature | 

#### Example Request URI

        
    PUT /api/v1/categories/thermostats/{id}/commands


Where {id} is the unique identifier of the device to which the command should be sent.

#### Example Request Body

       
    {
        "command": "PRESET_ADD",
        "tParams": {
            "NAME": "[value]",
            "PRESET_FIELDS": "[value]",
        }
    }
    
### PRESET_DELETE
Deletes a Preset Schedule Preset if protocol driver has the "can_preset_schedule" capability.

#### Parameters
| Parameter | Description |
|----------------|-------------|
| NAME | (string) (required): the name of the preset to be deleted | 

#### Example Request URI

        
    PUT /api/v1/categories/thermostats/{id}/commands


Where {id} is the unique identifier of the device to which the command should be sent.

#### Example Request Body

       
    {
        "command": "PRESET_DELETE",
        "tParams": {
            "NAME": "[value]",
        }
    }
    
### PRESET_EVENT_ADD
Adds a Preset Schedule Preset Event to be run at the specified day/time (If protocol driver has the "can_preset_schedule" capability). Note: Adding an event at the same time as a different preset event will result in the different preset event being deleted and the new one being put in at that time.

#### Parameters
| Parameter | Description |
|----------------|-------------|
| PRESET | (string): the name of the preset | 
| WEEKDAY | (int): (0-6 with Sunday being 0) | 
| HOUR | (int): (0-23) | 
| MINUTE | (int): (0-60) | 

#### Example Request URI

        
    PUT /api/v1/categories/thermostats/{id}/commands


Where {id} is the unique identifier of the device to which the command should be sent.

#### Example Request Body

       
    {
        "command": "PRESET_EVENT_ADD",
        "tParams": {
            "PRESET": "[value]",
            "WEEKDAY": "[value]",
            "HOUR": "[value]",
            "MINUTE": "[value]",
        }
    }
    
### PRESET_EVENT_DELETE
Deletes a Preset Schedule Preset if the protocol driver has the "can_preset_schedule" capability.  Note:  Using for the Preset or -1 for the weekday, hour or minute might be useful for UI's, Agents or Protocol Drivers as when a matching parameter is used you can delete multiple events at once AND only one Notify of the changes that were made are sent rather than causing a notify for each and every modification if they were done one at a time.

#### Parameters
| Parameter | Description |
|----------------|-------------|
| PRESET | (string): Preset Name ( Using "" (an empty string) will match all presets to make deleting all events of a given preset name easier) | 
| WEEKDAY | (int): (0-6 with Sunday being 0) - Using -1 will match any weekday | 
| HOUR | (int): (0-60) - Using -1 will match any Minute. | 
| MINUTE | (int): (0-60) | 

#### Example Request URI

        
    PUT /api/v1/categories/thermostats/{id}/commands


Where {id} is the unique identifier of the device to which the command should be sent.

#### Example Request Body

       
    {
        "command": "PRESET_EVENT_DELETE",
        "tParams": {
            "PRESET": "[value]",
            "WEEKDAY": "[value]",
            "HOUR": "[value]",
            "MINUTE": "[value]",
        }
    }
    
### PRESET_EVENT_MODIFY
Modifies an existing Preset Schedule Event (If protocol driver has the "can_preset_schedule" capability).  Note: Modifying an event to the same time as a different preset event will result in the different preset event being deleted and the new one being put in at that time.

#### Parameters
| Parameter | Description |
|----------------|-------------|
| PRESET | (string): Preset Name ( Using "" (an empty string) will match all presets to make deleting all events of a given preset name easier) | 
| WEEKDAY | (int): (0-6 with Sunday being 0) | 
| HOUR | (int): (0-60) | 
| MINUTE | (int): (0-60) | 
| NEW_WEEKDAY | (int): (0-6 with Sunday being 0) | 
| NEW_HOUR | (int): (0-60) | 
| NEW_MINUTE | (int): (0-60) | 

#### Example Request URI

        
    PUT /api/v1/categories/thermostats/{id}/commands


Where {id} is the unique identifier of the device to which the command should be sent.

#### Example Request Body

       
    {
        "command": "PRESET_EVENT_MODIFY",
        "tParams": {
            "PRESET": "[value]",
            "WEEKDAY": "[value]",
            "HOUR": "[value]",
            "MINUTE": "[value]",
            "NEW_WEEKDAY": "[value]",
            "NEW_HOUR": "[value]",
            "NEW_MINUTE": "[value]",
        }
    }
    
### PRESET_MODIFY
Modify an existing Preset Schedule Preset (If protocol driver has the "can_preset_schedule" capability)

#### Parameters
| Parameter | Description |
|----------------|-------------|
| NAME | (string) (required): preset name | 
| NEW_NAME | (string): new preset name | 
| HEAT_SETPOINT | (decimal): Must also use SCALE parameter if this parameter is used or it assumes Fahrenheit. | 
| COOL_SETPOINT | (decimal): Must also use SCALE parameter if this parameter is used or it assumes Fahrenheit | 
| SINGLE_SETPOINT | (decimal): Must also use SCALE parameter if this parameter is used or it assumes Fahrenheit | 
| SCALE | (string) C or F. Assumes F if nothing is provided. | 
| HVAC_MODE | (string) | 
| FAN_MODE | (string) | 
| HUMIDITY_MODE | (string) | 
| HUMIDIFY_SETPOINT | (string) | 
| DEHUMIDIFY_SETPOINT | (string) | 
| CUSTOM_FIELDS | (xml) | 

#### Example Request URI

        
    PUT /api/v1/categories/thermostats/{id}/commands


Where {id} is the unique identifier of the device to which the command should be sent.

#### Example Request Body

       
    {
        "command": "PRESET_MODIFY",
        "tParams": {
            "NAME": "[value]",
            "NEW_NAME": "[value]",
            "HEAT_SETPOINT": "[value]",
            "COOL_SETPOINT": "[value]",
            "SINGLE_SETPOINT": "[value]",
            "SCALE": "[value]",
            "HVAC_MODE": "[value]",
            "FAN_MODE": "[value]",
            "HUMIDITY_MODE": "[value]",
            "HUMIDIFY_SETPOINT": "[value]",
            "DEHUMIDIFY_SETPOINT": "[value]",
            "CUSTOM_FIELDS": "[value]",
        }
    }
    
### QUERY_SCHEDULE
Used for the old ccz and a few older thermostats Scheduling

#### Example Request URI

        
    PUT /api/v1/categories/thermostats/{id}/commands


Where {id} is the unique identifier of the device to which the command should be sent.

#### Example Request Body

       
    {
        "command": "QUERY_SCHEDULE"
    }
    
### QUERY_SCHEDULE_DEFAULTS
Used for the old ccz and a few older thermostats Scheduling

#### Example Request URI

        
    PUT /api/v1/categories/thermostats/{id}/commands


Where {id} is the unique identifier of the device to which the command should be sent.

#### Example Request Body

       
    {
        "command": "QUERY_SCHEDULE_DEFAULTS"
    }
    
### SET_BUTTONS_LOCK
Used to indicate if the buttons on the thermostat should be locked out from controlling the temperature

#### Example Request URI

        
    PUT /api/v1/categories/thermostats/{id}/commands


Where {id} is the unique identifier of the device to which the command should be sent.

#### Example Request Body

       
    {
        "command": "SET_BUTTONS_LOCK"
    }
    
### DEC_SETPOINT_HUMIDIFY
Used to Decrement the Setpoint by one step.

#### Example Request URI

        
    PUT /api/v1/categories/thermostats/{id}/commands


Where {id} is the unique identifier of the device to which the command should be sent.

#### Example Request Body

       
    {
        "command": "DEC_SETPOINT_HUMIDIFY"
    }
    
### DEC_SETPOINT_DEHUMIDIFY
Used to Decrement the Setpoint by one step.

#### Example Request URI

        
    PUT /api/v1/categories/thermostats/{id}/commands


Where {id} is the unique identifier of the device to which the command should be sent.

#### Example Request Body

       
    {
        "command": "DEC_SETPOINT_DEHUMIDIFY"
    }
    
### INC_SETPOINT_DEHUMIDIFY
Used to increment the Setpoint by one step.

#### Example Request URI

        
    PUT /api/v1/categories/thermostats/{id}/commands


Where {id} is the unique identifier of the device to which the command should be sent.

#### Example Request Body

       
    {
        "command": "INC_SETPOINT_DEHUMIDIFY"
    }
    
### INC_SETPOINT_HUMIDIFY
Used to increment the Setpoint by one step.

#### Example Request URI

        
    PUT /api/v1/categories/thermostats/{id}/commands


Where {id} is the unique identifier of the device to which the command should be sent.

#### Example Request Body

       
    {
        "command": "INC_SETPOINT_HUMIDIFY"
    }
    
### SET_CALIBRATION
Used to set the calibration value. The can_calibrate capability must be true for this to work. Changes the CALIBRATION variable.  Note: This command is supported with the release of OS 2.7.0. However, it will will be deprecated in the future.  See the capability: can_calibrate for future development efforts.

#### Example Request URI

        
    PUT /api/v1/categories/thermostats/{id}/commands


Where {id} is the unique identifier of the device to which the command should be sent.

#### Example Request Body

       
    {
        "command": "SET_CALIBRATION"
    }
    
### SET _EVENT
Occurs when the scheduler determines it's time for a new event to be run for Preset Scheduling

#### Parameters
| Parameter | Description |
|----------------|-------------|
| PRESET | Name of preset to be run. It's up to the protocol driver to apply all the data for that preset, as received from SET_PRESETS | 

#### Example Request URI

        
    PUT /api/v1/categories/thermostats/{id}/commands


Where {id} is the unique identifier of the device to which the command should be sent.

#### Example Request Body

       
    {
        "command": "SET _EVENT",
        "tParams": {
            "PRESET": "[value]",
        }
    }
    
### SET_EVENTS
XML that is provided from the proxy in the case that a protocol driver wants to push the Preset Schedule to hardware

#### Example Request URI

        
    PUT /api/v1/categories/thermostats/{id}/commands


Where {id} is the unique identifier of the device to which the command should be sent.

#### Example Request Body

       
    {
        "command": "SET_EVENTS"
    }
    
### SET_OUTDOOR_TEMPERATURE
Sets the outdoor temperature which is used by some thermostats for the purpose of humidity balancing, fresh air venting, air quality venting, and other HVAC function.

#### Parameters
| Parameter | Description |
|----------------|-------------|
| CELCIUS | FAHRENHEIT | The value is an floating point value (See capabilities for resolution setting) for F or C, and the name of the parameter can be either: CELSIUS or FAHRENHEIT | 

#### Example Request URI

        
    PUT /api/v1/categories/thermostats/{id}/commands


Where {id} is the unique identifier of the device to which the command should be sent.

#### Example Request Body

       
    {
        "command": "SET_OUTDOOR_TEMPERATURE",
        "tParams": {
            "CELCIUS | FAHRENHEIT": "[value]",
        }
    }
    
### SET_REMOTE_SENSOR
Used to indicate if the remote sensor on the thermostat is in use.

#### Parameters
| Parameter | Description |
|----------------|-------------|
| IN_USE | (boolean) indicates whether or not the remote sensor is in use.  Note: This command is supported with the release of OS 2.7.0. However, it will will be deprecated in the future. See the capability: has_remote_sensor for future driver development efforts. | 

#### Example Request URI

        
    PUT /api/v1/categories/thermostats/{id}/commands


Where {id} is the unique identifier of the device to which the command should be sent.

#### Example Request Body

       
    {
        "command": "SET_REMOTE_SENSOR",
        "tParams": {
            "IN_USE": "[value]",
        }
    }
    
### SET_SCALE
Used to set the temperature scale the thermostat should use

#### Parameters
| Parameter | Description |
|----------------|-------------|
| SCALE | (string) One of: KELVIN, CELSIUS or FAHRENHEIT.  Note: the value KELVIN will be deprecated post 2.7.0 and possibly as soon as 2.8.0. | 

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
    
### SET_MODE_FAN
Used to set the current fan mode of the thermostat.

#### Parameters
| Parameter | Description |
|----------------|-------------|
| MODE | (string) the name of the mode the fan should be in. The value inside this ￼string is determined by the protocol driver, when it supplies a list of supported fan modes to the (usually as an entry in its c4i file) | 

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
Used to set the current hold mode of the thermostat.

#### Parameters
| Parameter | Description |
|----------------|-------------|
| MODE | (string) the hold mode such as "Off" "Next Event" "Hold Perm" etc. The value of this string is determined by the protocol driver, when it supplies a list of supported fan modes to the proxy usually as an entry in its c4i file but can also be part of the DYNAMIC_CAPABILITIES. If the hold mode is "Hold Until" then the following parameters are required: YEAR - YY (2000+), MONTH - MM (1-12), DAY - DD (1-31), HOUR - HH (0-23), MINUTE - MM (0-59), SECOND - SS (0-60). | 

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
    
### SET_MODE_HUMIDITY
Used to set the humidification mode in a protocol driver.

#### Parameters
| Parameter | Description |
|----------------|-------------|
| MODE | (string) Examples are Off, Humidify, Dehumidify, Dehumidify Whole Home, Dehumidify by Overcooling, etc. | 

#### Example Request URI

        
    PUT /api/v1/categories/thermostats/{id}/commands


Where {id} is the unique identifier of the device to which the command should be sent.

#### Example Request Body

       
    {
        "command": "SET_MODE_HUMIDITY",
        "tParams": {
            "MODE": "[value]",
        }
    }
    
### SET_MODE_HVAC
Used to set the HVAC mode in a protocol driver.

#### Parameters
| Parameter | Description |
|----------------|-------------|
| MODE | (string) Examples are: Off, Heat, Cool, Auto, etc. | 

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
    
### SET_PRESET
Occurs when someone selects to run a preset OUTSIDE of its regular schedule. In many cases a thermostat will apply a 2 hour hold or hold until next event if this occurs. Special consideration might need to be added for detecting when a hold is removed and unapplying configuration that this preset may have applied.

#### Parameters
| Parameter | Description |
|----------------|-------------|
| PRESET | (string) the name of the preset to be run | 

#### Example Request URI

        
    PUT /api/v1/categories/thermostats/{id}/commands


Where {id} is the unique identifier of the device to which the command should be sent.

#### Example Request Body

       
    {
        "command": "SET_PRESET",
        "tParams": {
            "PRESET": "[value]",
        }
    }
    
### SET_PRESETS
XML that the Proxy sends down to a protocol driver that contains information about presets. If preset scheduling is a capability of the protocol driver.  Note: Only values that were selected by the user will be sent, which may be a subset of available choices including those of custom fields. 

#### Example Request URI

        
    PUT /api/v1/categories/thermostats/{id}/commands


Where {id} is the unique identifier of the device to which the command should be sent.

#### Example Request Body

       
    {
        "command": "SET_PRESETS"
    }
    
### SET_SETPOINT_DEHUMIDIFY


#### Parameters
| Parameter | Description |
|----------------|-------------|
| SETPOINT | (int) 0-100 | 

#### Example Request URI

        
    PUT /api/v1/categories/thermostats/{id}/commands


Where {id} is the unique identifier of the device to which the command should be sent.

#### Example Request Body

       
    {
        "command": "SET_SETPOINT_DEHUMIDIFY",
        "tParams": {
            "SETPOINT": "[value]",
        }
    }
    
### SET_SETPOINT_COOL
Used to set the cool setpoint.

#### Parameters
| Parameter | Description |
|----------------|-------------|
| CELSIUS | (decimal) the Celsius value, as rounded and within the range defined by the driver | 
| KELVIN | (int) the Fahrenheit value, as rounded and within the range defined by the driver. This is for BACKCOMPAT drivers and any driver using this needs to be updated or it will not function in an upcoming release of the proxy. This parameter will be deprecated post 2.7.0 and possibly as soon as 2.8.0. | 
| FAHRENHEIT | (decimal) the Fahrenheit value, as rounded and within the range defined by the driver | 
| SETPOINT | (int) the setpoint in the "current" scale as defined by the driver. This is for BACKCOMPAT drivers and any driver using this needs to be updated or it will not function in an upcoming release of the proxy. This parameter will be deprecated post 2.7.0 and possibly as soon as 2.8.0. | 

#### Example Request URI

        
    PUT /api/v1/categories/thermostats/{id}/commands


Where {id} is the unique identifier of the device to which the command should be sent.

#### Example Request Body

       
    {
        "command": "SET_SETPOINT_COOL",
        "tParams": {
            "CELSIUS": "[value]",
            "KELVIN": "[value]",
            "FAHRENHEIT": "[value]",
            "SETPOINT": "[value]",
        }
    }
    
### SET_SETPOINT_HEAT
Used to set the heat setpoint.

#### Parameters
| Parameter | Description |
|----------------|-------------|
| CELSIUS | (decimal) the Celsius value, as rounded and within the range defined by the driver | 
| KELVIN | (int) the Fahrenheit value, as rounded and within the range defined by the driver. This is for BACKCOMPAT drivers and any driver using this needs to be updated or it will not function in an upcoming release of the proxy. This parameter will be deprecated post 2.7.0 and possibly as soon as 2.8.0. | 
| FAHRENHEIT | (decimal) the Fahrenheit value, as rounded and within the range defined by the driver | 
| SETPOINT | (int) the setpoint in the "current" scale as defined by the driver. This is for BACKCOMPAT drivers and any driver using this needs to be updated or it will not function in an upcoming release of the proxy. This parameter will be deprecated post 2.7.0 and possibly as soon as 2.8.0. | 

#### Example Request URI

        
    PUT /api/v1/categories/thermostats/{id}/commands


Where {id} is the unique identifier of the device to which the command should be sent.

#### Example Request Body

       
    {
        "command": "SET_SETPOINT_HEAT",
        "tParams": {
            "CELSIUS": "[value]",
            "KELVIN": "[value]",
            "FAHRENHEIT": "[value]",
            "SETPOINT": "[value]",
        }
    }
    
### SET_SETPOINT_HUMIDIFY
Used to set the humidify setpoint.

#### Parameters
| Parameter | Description |
|----------------|-------------|
| MODE | (int) 0-100 | 

#### Example Request URI

        
    PUT /api/v1/categories/thermostats/{id}/commands


Where {id} is the unique identifier of the device to which the command should be sent.

#### Example Request Body

       
    {
        "command": "SET_SETPOINT_HUMIDIFY",
        "tParams": {
            "MODE": "[value]",
        }
    }
    
### SET_SETPOINT_SINGLE
Used to set the single setpoint value.  Provide either CELSIUS or FAHRENHEIT, not both.

#### Parameters
| Parameter | Description |
|----------------|-------------|
| CELSIUS | (decimal) the Celsius value, as rounded and within the range defined by the driver. | 
| FAHRENHEIT | (decimal) the Celsius value, as rounded and within the range defined by the driver. | 

#### Example Request URI

        
    PUT /api/v1/categories/thermostats/{id}/commands


Where {id} is the unique identifier of the device to which the command should be sent.

#### Example Request Body

       
    {
        "command": "SET_SETPOINT_SINGLE",
        "tParams": {
            "CELSIUS": "[value]",
            "FAHRENHEIT": "[value]",
        }
    }
    
### SET_VAC_SETPOINT_COOL
Used to set the cool setpoint when it vacation mode

#### Parameters
| Parameter | Description |
|----------------|-------------|
| KELVIN | (int) an integer indicating the temperature in kelvin. Only changes the future value, will not update the thermostat to this value if it's already in vacation mode. | 

#### Example Request URI

        
    PUT /api/v1/categories/thermostats/{id}/commands


Where {id} is the unique identifier of the device to which the command should be sent.

#### Example Request Body

       
    {
        "command": "SET_VAC_SETPOINT_COOL",
        "tParams": {
            "KELVIN": "[value]",
        }
    }
    
### SET_VAC_SETPOINT_HEAT
Used to set the heat setpoint when it vacation mode

#### Parameters
| Parameter | Description |
|----------------|-------------|
| KELVIN | (int) an integer indicating the temperature in kelvin. Only changes the future value, will not update the thermostat to this value if it's already in vacation mode. | 

#### Example Request URI

        
    PUT /api/v1/categories/thermostats/{id}/commands


Where {id} is the unique identifier of the device to which the command should be sent.

#### Example Request Body

       
    {
        "command": "SET_VAC_SETPOINT_HEAT",
        "tParams": {
            "KELVIN": "[value]",
        }
    }
    
### SET_VACATION_MODE
Used to indicate if the thermostat is in vacation mode or not

#### Parameters
| Parameter | Description |
|----------------|-------------|
| MODE | (string) either "On" or "Off" | 

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
    
### SET_BUTTONS_LOCK
Command used to indicate if the buttons on the tHermostat should be locked out from controlling the temperature :

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
    
### SET_CALIBRATION
Used to set the calibration value. can_calibrate capability must be set to true for this to work.

#### Example Request URI

        
    PUT /api/v1/categories/thermostats/{id}/commands


Where {id} is the unique identifier of the device to which the command should be sent.

#### Example Request Body

       
    {
        "command": "SET_CALIBRATION"
    }
    
### SET_REMOTE_SENSOR
Command received from the proxy to establish a remote sensor within the HVAC system.

#### Parameters
| Parameter | Description |
|----------------|-------------|
| IN_USE | (boolean): True or False. True designates a remote sensor within the system. False designates the thermostat's onboard sensor as being in use. | 

#### Example Request URI

        
    PUT /api/v1/categories/thermostats/{id}/commands


Where {id} is the unique identifier of the device to which the command should be sent.

#### Example Request Body

       
    {
        "command": "SET_REMOTE_SENSOR",
        "tParams": {
            "IN_USE": "[value]",
        }
    }
    
### SET_SCALE
Command received from the proxy to establish the scale used in the HVAC system: Fahrenheit or Celsius.

#### Parameters
| Parameter | Description |
|----------------|-------------|
| SCALE | (string): F or C - The first letter of "Fahrenheit" or "Celsius" depending on the scale used in the HVAC system. | 

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
Used to set the temperature that the heating unit should ensure the temperature reflects._It requires one parameter, the name of which can vary depending on the units. The value is an integer, and the name of the parameter can be:

#### Parameters
| Parameter | Description |
|----------------|-------------|
| KELVIN | (number): Heating setpoint temperature. Kelvin (str).  Kelvin value in form of 2996.61 | 

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
Used to set the temperature that the cooling unit should ensure the temperature reflects._It requires one parameter, the name of which can vary depending on the units. The value is an integer, and the name of the parameter can be:

#### Parameters
| Parameter | Description |
|----------------|-------------|
| KELVIN | (number): Heating setpoint temperature. Kelvin (str).  Kelvin value in form of 2996.61 | 

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
    
### SET_VAC_SETPOINT_COOL
Command received from the proxy to establish a cooling setpoint for vacation mode. Parameters

#### Parameters
| Parameter | Description |
|----------------|-------------|
| SETPOINT | (number): Temperature designated to start cooling when in vacation mode. | 
| SCALE | (string):F or C � The first letter of �Fahrenheit� or �Celsius� depending on the scale used in the HVAC system.  Note: When using SET_VAC_SETPOINT_COOL a value must also be set for SET_VAC_SETPOINT_HEAT | 

#### Example Request URI

        
    PUT /api/v1/categories/thermostats/{id}/commands


Where {id} is the unique identifier of the device to which the command should be sent.

#### Example Request Body

       
    {
        "command": "SET_VAC_SETPOINT_COOL",
        "tParams": {
            "SETPOINT": "[value]",
            "SCALE": "[value]",
        }
    }
    
### SET_VAC_SETPOINT_HEAT
Command received from the proxy to establish a heating setpoint for vacation mode.

#### Parameters
| Parameter | Description |
|----------------|-------------|
| SETPOINT | (number): Temperature designated to start cooling when in vacation mode. | 
| SCALE | (string):F or C - The first letter of "Fahrenheit" or "Celsius" depending on the scale used in the HVAC system.  Note: When using SET_VAC_SETPOINT_COOL a value must also be set for SET_VAC_SETPOINT_HEAT | 

#### Example Request URI

        
    PUT /api/v1/categories/thermostats/{id}/commands


Where {id} is the unique identifier of the device to which the command should be sent.

#### Example Request Body

       
    {
        "command": "SET_VAC_SETPOINT_HEAT",
        "tParams": {
            "SETPOINT": "[value]",
            "SCALE": "[value]",
        }
    }
    
### SET_VACATION_MODE
Command received from the proxy to establish or exclude "vacation mode" for the HVAC system.

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
    
### UPDATE_SCHEDULE_ENTRIES
Command received from the proxy to modify the thermostat heating/cooling schedule.

#### Parameters
| Parameter | Description |
|----------------|-------------|
| Entries | (arr) - holds an entry (or a set of entries) in XML:  Example data for the Entries parameter:<ScheduleUpdate><ScheduleEntryUpdate DayOfWeek="1" EntryIndex="0" EntryTime="375" IsEnabled="1" HeatSetpoint="2942" CoolSetpoint="2987"/></ScheduleUpdate>  DayofWeek(number): Number representing day of week: 0= Sunday, 1=Monday.   EntryIndex(number): 0 to the number of entries the day can support. 0 = the first entry, 1 = the second entry.   EntryTime(number): Number of minutes past midnight for the schedule change. For example, 360= 6:00AM.    IsEnabled(boolean): Enables or disables a schedule. By default, the first four schedules are enabled.   HeatSetpoint(number): Temperature designated to start the heating system.   HeatSetpoint(number): Temperature designated to start the heating system.   CoolSetpoint(number): Temperature designated to start the cooling system. | 

#### Example Request URI

        
    PUT /api/v1/categories/thermostats/{id}/commands


Where {id} is the unique identifier of the device to which the command should be sent.

#### Example Request Body

       
    {
        "command": "UPDATE_SCHEDULE_ENTRIES",
        "tParams": {
            "Entries": "[value]",
        }
    }
    
### QUERY_SETTINGS


#### Example Request URI

        
    PUT /api/v1/categories/thermostats/{id}/commands


Where {id} is the unique identifier of the device to which the command should be sent.

#### Example Request Body

       
    {
        "command": "QUERY_SETTINGS"
    }
    
