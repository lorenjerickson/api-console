### BACK


#### Example Request URI

        
    PUT /api/v1/categories/audio_video/{id}/commands


Where {id} is the unique identifier of the device to which the command should be sent.

#### Example Request Body

       
    {
        "command": "BACK"
    }
    
### CANCEL


#### Example Request URI

        
    PUT /api/v1/categories/audio_video/{id}/commands


Where {id} is the unique identifier of the device to which the command should be sent.

#### Example Request Body

       
    {
        "command": "CANCEL"
    }
    
### DASH


#### Example Request URI

        
    PUT /api/v1/categories/audio_video/{id}/commands


Where {id} is the unique identifier of the device to which the command should be sent.

#### Example Request Body

       
    {
        "command": "DASH"
    }
    
### DISCONNECT_OUTPUT


#### Parameters
| Parameter | Description |
|----------------|-------------|
| OUTPUT | (INT)nOutputBindingID | 

#### Example Request URI

        
    PUT /api/v1/categories/audio_video/{id}/commands


Where {id} is the unique identifier of the device to which the command should be sent.

#### Example Request Body

       
    {
        "command": "DISCONNECT_OUTPUT",
        "tParams": {
            "OUTPUT": "[value]",
        }
    }
    
### SET _LOUDNESS


#### Parameters
| Parameter | Description |
|----------------|-------------|
| OUTPUT | (INT)nOutputBindingID | 
| LEVEL | (INT)nLevel | 

#### Example Request URI

        
    PUT /api/v1/categories/audio_video/{id}/commands


Where {id} is the unique identifier of the device to which the command should be sent.

#### Example Request Body

       
    {
        "command": "SET _LOUDNESS",
        "tParams": {
            "OUTPUT": "[value]",
            "LEVEL": "[value]",
        }
    }
    
