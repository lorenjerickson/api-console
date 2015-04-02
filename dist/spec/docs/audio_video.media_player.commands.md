### GET_ALPHA_LOOKUP
Command that returns the index of the first item in the list that begins with the specified character.

#### Parameters
| Parameter | Description |
|----------------|-------------|
| LETTER | (STRING) | 

#### Example Request URI

        
    PUT /api/v1/categories/audio_video/{id}/commands


Where {id} is the unique identifier of the device to which the command should be sent.

#### Example Request Body

       
    {
        "command": "GET_ALPHA_LOOKUP",
        "tParams": {
            "LETTER": "[value]",
        }
    }
    
### GET_LIST
Command to obtain a the current list.

#### Example Request URI

        
    PUT /api/v1/categories/audio_video/{id}/commands


Where {id} is the unique identifier of the device to which the command should be sent.

#### Example Request Body

       
    {
        "command": "GET_LIST"
    }
    
### GET_NEXT
Command to obtain the next set of items from the current list.

#### Parameters
| Parameter | Description |
|----------------|-------------|
| FIRST | The index of the first item to be returned. | 
| NUM | The number of items to be returned. | 

#### Example Request URI

        
    PUT /api/v1/categories/audio_video/{id}/commands


Where {id} is the unique identifier of the device to which the command should be sent.

#### Example Request Body

       
    {
        "command": "GET_NEXT",
        "tParams": {
            "FIRST": "[value]",
            "NUM": "[value]",
        }
    }
    
### GET_MENU
Command to obtain the list of items in the menu.

#### Example Request URI

        
    PUT /api/v1/categories/audio_video/{id}/commands


Where {id} is the unique identifier of the device to which the command should be sent.

#### Example Request Body

       
    {
        "command": "GET_MENU"
    }
    
### GET_REPEAT_MODES
Command to obtain supported repeat modes.

#### Example Request URI

        
    PUT /api/v1/categories/audio_video/{id}/commands


Where {id} is the unique identifier of the device to which the command should be sent.

#### Example Request Body

       
    {
        "command": "GET_REPEAT_MODES"
    }
    
### GET_SHUFFLE_MODES
Command to obtain supported shuffle modes.

#### Example Request URI

        
    PUT /api/v1/categories/audio_video/{id}/commands


Where {id} is the unique identifier of the device to which the command should be sent.

#### Example Request Body

       
    {
        "command": "GET_SHUFFLE_MODES"
    }
    
### LIST_BACK
Command to return to the previous list.

#### Example Request URI

        
    PUT /api/v1/categories/audio_video/{id}/commands


Where {id} is the unique identifier of the device to which the command should be sent.

#### Example Request Body

       
    {
        "command": "LIST_BACK"
    }
    
### LIST_SELECT
Command to select an item from a list of media on the GenericMediaPlayer. If the item has a child list, that list is sent to the UI. If the item is playable, playback should be started.

#### Parameters
| Parameter | Description |
|----------------|-------------|
| ITEM | The id of the item selected | 
| TYPE | The item type returned in the list. | 
| TITLE | The name of the item. | 

#### Example Request URI

        
    PUT /api/v1/categories/audio_video/{id}/commands


Where {id} is the unique identifier of the device to which the command should be sent.

#### Example Request Body

       
    {
        "command": "LIST_SELECT",
        "tParams": {
            "ITEM": "[value]",
            "TYPE": "[value]",
            "TITLE": "[value]",
        }
    }
    
### MENU_SELECT
Command to select an item from the list of menu items returned with GET_MENU.

#### Parameters
| Parameter | Description |
|----------------|-------------|
| ITEM | The id of the item selected | 
| TYPE | The item type returned in the list. | 
| TITLE | The name of the item. | 

#### Example Request URI

        
    PUT /api/v1/categories/audio_video/{id}/commands


Where {id} is the unique identifier of the device to which the command should be sent.

#### Example Request Body

       
    {
        "command": "MENU_SELECT",
        "tParams": {
            "ITEM": "[value]",
            "TYPE": "[value]",
            "TITLE": "[value]",
        }
    }
    
### PAUSE
Command to pause media playback on the GenericMediaPlayer.

#### Example Request URI

        
    PUT /api/v1/categories/audio_video/{id}/commands


Where {id} is the unique identifier of the device to which the command should be sent.

#### Example Request Body

       
    {
        "command": "PAUSE"
    }
    
### PLAY


#### Example Request URI

        
    PUT /api/v1/categories/audio_video/{id}/commands


Where {id} is the unique identifier of the device to which the command should be sent.

#### Example Request Body

       
    {
        "command": "PLAY"
    }
    
### PLAYPAUSE
Command to start media playback if currently paused or pause media playback if currently playing.

#### Example Request URI

        
    PUT /api/v1/categories/audio_video/{id}/commands


Where {id} is the unique identifier of the device to which the command should be sent.

#### Example Request Body

       
    {
        "command": "PLAYPAUSE"
    }
    
### RESET
Command to reset the GenericMediaPlayer. This command is used to switch between different media types. A new list and menu should be sent to the UI when this command is sent.

#### Parameters
| Parameter | Description |
|----------------|-------------|
| TYPE | The new media type to be shown. | 

#### Example Request URI

        
    PUT /api/v1/categories/audio_video/{id}/commands


Where {id} is the unique identifier of the device to which the command should be sent.

#### Example Request Body

       
    {
        "command": "RESET",
        "tParams": {
            "TYPE": "[value]",
        }
    }
    
### SCAN_FWD
Command to scan forward through current media.

#### Example Request URI

        
    PUT /api/v1/categories/audio_video/{id}/commands


Where {id} is the unique identifier of the device to which the command should be sent.

#### Example Request Body

       
    {
        "command": "SCAN_FWD"
    }
    
### SCAN_REV
Command to scan backwards through current media.

#### Example Request URI

        
    PUT /api/v1/categories/audio_video/{id}/commands


Where {id} is the unique identifier of the device to which the command should be sent.

#### Example Request Body

       
    {
        "command": "SCAN_REV"
    }
    
### SEARCH
Command to filter items based on the search string.

#### Example Request URI

        
    PUT /api/v1/categories/audio_video/{id}/commands


Where {id} is the unique identifier of the device to which the command should be sent.

#### Example Request Body

       
    {
        "command": "SEARCH"
    }
    
### SELECT_PLAY
Command to select the specified item for playback. (If an album, this will playback all tracks.)

#### Parameters
| Parameter | Description |
|----------------|-------------|
| ITEM | The index of the item to be played. | 

#### Example Request URI

        
    PUT /api/v1/categories/audio_video/{id}/commands


Where {id} is the unique identifier of the device to which the command should be sent.

#### Example Request Body

       
    {
        "command": "SELECT_PLAY",
        "tParams": {
            "ITEM": "[value]",
        }
    }
    
### SET_REPEAT
Command to set the repeat mode on the GenericMediaPlayer

#### Parameters
| Parameter | Description |
|----------------|-------------|
| MODE | One of the modes returned with the <repeat_modes> tag | 

#### Example Request URI

        
    PUT /api/v1/categories/audio_video/{id}/commands


Where {id} is the unique identifier of the device to which the command should be sent.

#### Example Request Body

       
    {
        "command": "SET_REPEAT",
        "tParams": {
            "MODE": "[value]",
        }
    }
    
### SET_SHUFFLE
Command to obtain the shuffle mode for the GenericMediaPlayer.

#### Parameters
| Parameter | Description |
|----------------|-------------|
| MODE | One of the modes returned with the <shuffle_modes> tag | 

#### Example Request URI

        
    PUT /api/v1/categories/audio_video/{id}/commands


Where {id} is the unique identifier of the device to which the command should be sent.

#### Example Request Body

       
    {
        "command": "SET_SHUFFLE",
        "tParams": {
            "MODE": "[value]",
        }
    }
    
### SKIP_FWD
Command that starts playback of the next media item.

#### Example Request URI

        
    PUT /api/v1/categories/audio_video/{id}/commands


Where {id} is the unique identifier of the device to which the command should be sent.

#### Example Request Body

       
    {
        "command": "SKIP_FWD"
    }
    
### SKIP_REV
Command that starts playback of the previous media item.

#### Example Request URI

        
    PUT /api/v1/categories/audio_video/{id}/commands


Where {id} is the unique identifier of the device to which the command should be sent.

#### Example Request Body

       
    {
        "command": "SKIP_REV"
    }
    
### START_SCAN_FWD
Command to start scan forward or fast forward through the current playing media item.

#### Example Request URI

        
    PUT /api/v1/categories/audio_video/{id}/commands


Where {id} is the unique identifier of the device to which the command should be sent.

#### Example Request Body

       
    {
        "command": "START_SCAN_FWD"
    }
    
### STOP_SCAN_FWD
Command to stop scanning forward through the current media.

#### Example Request URI

        
    PUT /api/v1/categories/audio_video/{id}/commands


Where {id} is the unique identifier of the device to which the command should be sent.

#### Example Request Body

       
    {
        "command": "STOP_SCAN_FWD"
    }
    
### START_SCAN_REV
Command to start scan backwards or rewind through the currently playing media item.

#### Example Request URI

        
    PUT /api/v1/categories/audio_video/{id}/commands


Where {id} is the unique identifier of the device to which the command should be sent.

#### Example Request Body

       
    {
        "command": "START_SCAN_REV"
    }
    
### STOP_SCAN_REV
Command to stop scanning backward through the current media.

#### Example Request URI

        
    PUT /api/v1/categories/audio_video/{id}/commands


Where {id} is the unique identifier of the device to which the command should be sent.

#### Example Request Body

       
    {
        "command": "STOP_SCAN_REV"
    }
    
### STOP
Command to stop the playback.

#### Example Request URI

        
    PUT /api/v1/categories/audio_video/{id}/commands


Where {id} is the unique identifier of the device to which the command should be sent.

#### Example Request Body

       
    {
        "command": "STOP"
    }
    
