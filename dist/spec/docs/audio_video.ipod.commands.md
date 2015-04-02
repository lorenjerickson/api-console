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
    
### GET_ELAPSED_TIME
Command to obtain amount time media has been playing. Returns amount of time media has played.

#### Example Request URI

        
    PUT /api/v1/categories/audio_video/{id}/commands


Where {id} is the unique identifier of the device to which the command should be sent.

#### Example Request Body

       
    {
        "command": "GET_ELAPSED_TIME"
    }
    
### GET_FIRMWARE_VERSION
Command to obtain the current firmware version of the iPod dock.

#### Example Request URI

        
    PUT /api/v1/categories/audio_video/{id}/commands


Where {id} is the unique identifier of the device to which the command should be sent.

#### Example Request Body

       
    {
        "command": "GET_FIRMWARE_VERSION"
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
    
### GET_PROGRESS
Command to obtain the progress of the current media being played by the iPod.

#### Example Request URI

        
    PUT /api/v1/categories/audio_video/{id}/commands


Where {id} is the unique identifier of the device to which the command should be sent.

#### Example Request Body

       
    {
        "command": "GET_PROGRESS"
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
    
### GET_REPEAT
Command to obtain supported repeat modes.

#### Example Request URI

        
    PUT /api/v1/categories/audio_video/{id}/commands


Where {id} is the unique identifier of the device to which the command should be sent.

#### Example Request Body

       
    {
        "command": "GET_REPEAT"
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
    
### OFF
Command to turn the iPod off.

#### Example Request URI

        
    PUT /api/v1/categories/audio_video/{id}/commands


Where {id} is the unique identifier of the device to which the command should be sent.

#### Example Request Body

       
    {
        "command": "OFF"
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
Command to play media on the iPod.

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
    
### QUERY_CURRENT_SETTINGS
Command to retrieve all of the iPod settings including; online status, room id, now playinginfo, elapsed time, coverart, etc.

#### Example Request URI

        
    PUT /api/v1/categories/audio_video/{id}/commands


Where {id} is the unique identifier of the device to which the command should be sent.

#### Example Request Body

       
    {
        "command": "QUERY_CURRENT_SETTINGS"
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
    
### REQUEST_CURRENT_MEDIA_INFO
Command to obtain information about the currently playing media.

#### Example Request URI

        
    PUT /api/v1/categories/audio_video/{id}/commands


Where {id} is the unique identifier of the device to which the command should be sent.

#### Example Request Body

       
    {
        "command": "REQUEST_CURRENT_MEDIA_INFO"
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
    
### SELECT_TOP_INDEX
Command to select a top item list of current list type.

#### Parameters
| Parameter | Description |
|----------------|-------------|
| RESET_DOCK | if = 1 then ResetDock | 
| ITEM_ID | Top index seclected | 

#### Example Request URI

        
    PUT /api/v1/categories/audio_video/{id}/commands


Where {id} is the unique identifier of the device to which the command should be sent.

#### Example Request Body

       
    {
        "command": "SELECT_TOP_INDEX",
        "tParams": {
            "RESET_DOCK": "[value]",
            "ITEM_ID": "[value]",
        }
    }
    
### SELECT_TOP_MUSIC_ITEM
Command to select top music item.

#### Example Request URI

        
    PUT /api/v1/categories/audio_video/{id}/commands


Where {id} is the unique identifier of the device to which the command should be sent.

#### Example Request Body

       
    {
        "command": "SELECT_TOP_MUSIC_ITEM"
    }
    
### SELECT_TOP_VIDEO_ITEM
Command to select top video item

#### Example Request URI

        
    PUT /api/v1/categories/audio_video/{id}/commands


Where {id} is the unique identifier of the device to which the command should be sent.

#### Example Request Body

       
    {
        "command": "SELECT_TOP_VIDEO_ITEM"
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
    
### SET_LIST_TYPE
Command to set current list type (Music or Video)

#### Parameters
| Parameter | Description |
|----------------|-------------|
| TYPE | 0 music 1 video | 

#### Example Request URI

        
    PUT /api/v1/categories/audio_video/{id}/commands


Where {id} is the unique identifier of the device to which the command should be sent.

#### Example Request Body

       
    {
        "command": "SET_LIST_TYPE",
        "tParams": {
            "TYPE": "[value]",
        }
    }
    
### SET_VIDEO_OUT
Command to obtain the video output type of the iPod.

#### Parameters
| Parameter | Description |
|----------------|-------------|
| OUTPUT_TYPE | 0 � None 1 � Composite 3 � Component | 

#### Example Request URI

        
    PUT /api/v1/categories/audio_video/{id}/commands


Where {id} is the unique identifier of the device to which the command should be sent.

#### Example Request Body

       
    {
        "command": "SET_VIDEO_OUT",
        "tParams": {
            "OUTPUT_TYPE": "[value]",
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
    
### TOGGLE_COVERART
Turn coverart on or off

#### Example Request URI

        
    PUT /api/v1/categories/audio_video/{id}/commands


Where {id} is the unique identifier of the device to which the command should be sent.

#### Example Request Body

       
    {
        "command": "TOGGLE_COVERART"
    }
    
