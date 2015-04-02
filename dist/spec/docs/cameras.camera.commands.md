### CHECK_ADDRESS_PORT


#### Example Request URI

        
    PUT /api/v1/categories/cameras/{id}/commands


Where {id} is the unique identifier of the device to which the command should be sent.

#### Example Request Body

       
    {
        "command": "CHECK_ADDRESS_PORT"
    }
    
### CHECK_URL


#### Example Request URI

        
    PUT /api/v1/categories/cameras/{id}/commands


Where {id} is the unique identifier of the device to which the command should be sent.

#### Example Request Body

       
    {
        "command": "CHECK_URL"
    }
    
### GET_MJPEG_QUERY
Command that is initiated in Composer Pro and immediately returns a block of XML information. It returns the query string needed to create the URL for MJPEG server push request.

#### Parameters
| Parameter | Description |
|----------------|-------------|
| SIZE_X | he desired resolution x-axis value. | 
| SIZE_Y | The desired resolution y-axis value. | 
| DELAY | The delay in milliseconds between pushed frames | 

#### Example Request URI

        
    PUT /api/v1/categories/cameras/{id}/commands


Where {id} is the unique identifier of the device to which the command should be sent.

#### Example Request Body

       
    {
        "command": "GET_MJPEG_QUERY",
        "tParams": {
            "SIZE_X": "[value]",
            "SIZE_Y": "[value]",
            "DELAY": "[value]",
        }
    }
    
### GET_PROPERTIES
Command called once by a UI entity to learn how to access a camera. It returns a block of XML reporting the properties of the camera

#### Example Request URI

        
    PUT /api/v1/categories/cameras/{id}/commands


Where {id} is the unique identifier of the device to which the command should be sent.

#### Example Request Body

       
    {
        "command": "GET_PROPERTIES"
    }
    
### GET_RTSP_H264_QUERY_STRING
Command that is initiated in Composer Pro and immediately returns a block of XML information. It returns the query string needed to create the URL for RTSP H264 stream request.

#### Parameters
| Parameter | Description |
|----------------|-------------|
| SIZE_X | he desired resolution x-axis value. | 
| SIZE_Y | The desired resolution y-axis value. | 
| DELAY | The delay in milliseconds between pushed frames | 

#### Example Request URI

        
    PUT /api/v1/categories/cameras/{id}/commands


Where {id} is the unique identifier of the device to which the command should be sent.

#### Example Request Body

       
    {
        "command": "GET_RTSP_H264_QUERY_STRING",
        "tParams": {
            "SIZE_X": "[value]",
            "SIZE_Y": "[value]",
            "DELAY": "[value]",
        }
    }
    
### GET_SNAPSHOT_QUERY_STRING
Command that is initiated in Composer Pro and immediately returns a block of XML information. It returns the query string needed to create the URL for HTTP snapshot request.

#### Parameters
| Parameter | Description |
|----------------|-------------|
| SIZE_X | he desired resolution x-axis value. | 
| SIZE_Y | The desired resolution y-axis value. | 

#### Example Request URI

        
    PUT /api/v1/categories/cameras/{id}/commands


Where {id} is the unique identifier of the device to which the command should be sent.

#### Example Request Body

       
    {
        "command": "GET_SNAPSHOT_QUERY_STRING",
        "tParams": {
            "SIZE_X": "[value]",
            "SIZE_Y": "[value]",
        }
    }
    
### HOME
Move the camera to its home position.

#### Example Request URI

        
    PUT /api/v1/categories/cameras/{id}/commands


Where {id} is the unique identifier of the device to which the command should be sent.

#### Example Request Body

       
    {
        "command": "HOME"
    }
    
### MOVE_TO
Have the camera move to location x and y within the specified window.

#### Parameters
| Parameter | Description |
|----------------|-------------|
| WIDTH | (int) | 
| HEIGHT | (int) | 
| X_INDEX | (int) | 
| Y_INDEX | (int) | 

#### Example Request URI

        
    PUT /api/v1/categories/cameras/{id}/commands


Where {id} is the unique identifier of the device to which the command should be sent.

#### Example Request Body

       
    {
        "command": "MOVE_TO",
        "tParams": {
            "WIDTH": "[value]",
            "HEIGHT": "[value]",
            "X_INDEX": "[value]",
            "Y_INDEX": "[value]",
        }
    }
    
### PAN_LEFT
Pan to the left.

#### Example Request URI

        
    PUT /api/v1/categories/cameras/{id}/commands


Where {id} is the unique identifier of the device to which the command should be sent.

#### Example Request Body

       
    {
        "command": "PAN_LEFT"
    }
    
### PAN_RIGHT
Pan to the right.

#### Example Request URI

        
    PUT /api/v1/categories/cameras/{id}/commands


Where {id} is the unique identifier of the device to which the command should be sent.

#### Example Request Body

       
    {
        "command": "PAN_RIGHT"
    }
    
### PAN_SCAN
Have the camera execute a complete scan from left to right.

#### Example Request URI

        
    PUT /api/v1/categories/cameras/{id}/commands


Where {id} is the unique identifier of the device to which the command should be sent.

#### Example Request Body

       
    {
        "command": "PAN_SCAN"
    }
    
### PRESET
Set the camera to preset location.

#### Parameters
| Parameter | Description |
|----------------|-------------|
| INDEX | valid values: 1 � n, where n is max preset defined by capabilities | 

#### Example Request URI

        
    PUT /api/v1/categories/cameras/{id}/commands


Where {id} is the unique identifier of the device to which the command should be sent.

#### Example Request Body

       
    {
        "command": "PRESET",
        "tParams": {
            "INDEX": "[value]",
        }
    }
    
### SET_ADDRESS
Set the camera address.

#### Parameters
| Parameter | Description |
|----------------|-------------|
| ADDRESS | (str) | 

#### Example Request URI

        
    PUT /api/v1/categories/cameras/{id}/commands


Where {id} is the unique identifier of the device to which the command should be sent.

#### Example Request Body

       
    {
        "command": "SET_ADDRESS",
        "tParams": {
            "ADDRESS": "[value]",
        }
    }
    
### SET_AUTHENTICATION_REQUIRED
Composer Pro command to set whether or not authentication is required. See the DriverWorks API documentation for Webservice API: urlPOST for Authentication information.

#### Parameters
| Parameter | Description |
|----------------|-------------|
| REQUIRED | (Bool) True/False | 

#### Example Request URI

        
    PUT /api/v1/categories/cameras/{id}/commands


Where {id} is the unique identifier of the device to which the command should be sent.

#### Example Request Body

       
    {
        "command": "SET_AUTHENTICATION_REQUIRED",
        "tParams": {
            "REQUIRED": "[value]",
        }
    }
    
### SET_AUTHENTICATION_TYPE
Composer Pro command to set AuthenticationType. Note that as of 2.5.3 only Basic Authentication is supported. See the DriverWorks API documentation for Webservice API: urlPOST for Authentication information

#### Parameters
| Parameter | Description |
|----------------|-------------|
| TYPE | String: BASIC or DIGEST | 

#### Example Request URI

        
    PUT /api/v1/categories/cameras/{id}/commands


Where {id} is the unique identifier of the device to which the command should be sent.

#### Example Request Body

       
    {
        "command": "SET_AUTHENTICATION_TYPE",
        "tParams": {
            "TYPE": "[value]",
        }
    }
    
### SET_USERNAME
Composer Pro command to set the Authentication username.

#### Parameters
| Parameter | Description |
|----------------|-------------|
| USERNAME | (string) - username. | 

#### Example Request URI

        
    PUT /api/v1/categories/cameras/{id}/commands


Where {id} is the unique identifier of the device to which the command should be sent.

#### Example Request Body

       
    {
        "command": "SET_USERNAME",
        "tParams": {
            "USERNAME": "[value]",
        }
    }
    
### SET_HTTP_PORT
Composer Pro command to set the HTTP Port

#### Parameters
| Parameter | Description |
|----------------|-------------|
| PORT | (int) - Port ID | 

#### Example Request URI

        
    PUT /api/v1/categories/cameras/{id}/commands


Where {id} is the unique identifier of the device to which the command should be sent.

#### Example Request Body

       
    {
        "command": "SET_HTTP_PORT",
        "tParams": {
            "PORT": "[value]",
        }
    }
    
### SET_RSTP_PORT


#### Parameters
| Parameter | Description |
|----------------|-------------|
| PORT | (int) - Port ID | 

#### Example Request URI

        
    PUT /api/v1/categories/cameras/{id}/commands


Where {id} is the unique identifier of the device to which the command should be sent.

#### Example Request Body

       
    {
        "command": "SET_RSTP_PORT",
        "tParams": {
            "PORT": "[value]",
        }
    }
    
### SET_PASSWORD
Composer pro command to set the Authentication password.

#### Parameters
| Parameter | Description |
|----------------|-------------|
| PASSWORD | (string): password | 

#### Example Request URI

        
    PUT /api/v1/categories/cameras/{id}/commands


Where {id} is the unique identifier of the device to which the command should be sent.

#### Example Request Body

       
    {
        "command": "SET_PASSWORD",
        "tParams": {
            "PASSWORD": "[value]",
        }
    }
    
### SET_PUBLICLY_ACCESSIBLE
Composer Pro command to set whether or not the camera can be accessed from public Internet.

#### Parameters
| Parameter | Description |
|----------------|-------------|
| PUBLICLY_ACCESSIBLE | (bool): True/False | 

#### Example Request URI

        
    PUT /api/v1/categories/cameras/{id}/commands


Where {id} is the unique identifier of the device to which the command should be sent.

#### Example Request Body

       
    {
        "command": "SET_PUBLICLY_ACCESSIBLE",
        "tParams": {
            "PUBLICLY_ACCESSIBLE": "[value]",
        }
    }
    
### TILT_DOWN
Tilt Camera down.

#### Example Request URI

        
    PUT /api/v1/categories/cameras/{id}/commands


Where {id} is the unique identifier of the device to which the command should be sent.

#### Example Request Body

       
    {
        "command": "TILT_DOWN"
    }
    
### TILT_UP
Tilt Camera up.

#### Example Request URI

        
    PUT /api/v1/categories/cameras/{id}/commands


Where {id} is the unique identifier of the device to which the command should be sent.

#### Example Request Body

       
    {
        "command": "TILT_UP"
    }
    
### TILT_SCAN
Have the camera execute a complete scan from top to bottom.

#### Example Request URI

        
    PUT /api/v1/categories/cameras/{id}/commands


Where {id} is the unique identifier of the device to which the command should be sent.

#### Example Request Body

       
    {
        "command": "TILT_SCAN"
    }
    
### ZOOM_IN
Zoom camera in.

#### Example Request URI

        
    PUT /api/v1/categories/cameras/{id}/commands


Where {id} is the unique identifier of the device to which the command should be sent.

#### Example Request Body

       
    {
        "command": "ZOOM_IN"
    }
    
### ZOOM_OUT
Zoom camera out.

#### Example Request URI

        
    PUT /api/v1/categories/cameras/{id}/commands


Where {id} is the unique identifier of the device to which the command should be sent.

#### Example Request Body

       
    {
        "command": "ZOOM_OUT"
    }
    
