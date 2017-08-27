# life360-python
A simple python life360 client

I built this because I couldn't find a straight forward life360 client that wasn't based on some curl commands. It works. 

## Usage

It is pretty straight forward and should be easy to integrate with any project. 


    # basic authorization hash (base64 if you want to decode it and see the sekrets)
    authorization_token = "cFJFcXVnYWJSZXRyZTRFc3RldGhlcnVmcmVQdW1hbUV4dWNyRUh1YzptM2ZydXBSZXRSZXN3ZXJFQ2hBUHJFOTZxYWtFZHI0Vg=="
    
    # your username and password (hope they are secure!)
    username = "email@address.com"
    password = "super long password"

    #instantiate the API
    api = life360(authorization_token=authorization_token, username=username, password=password)
    
    #Authenticate! 
    if api.authenticate():
        
        #Grab some circles returns json
        circles =  api.get_circles()
        
        #grab id
        id = circles[0]['id']
        
        #Let's get your circle!
        circle = api.get_circle(id)
        
## Next? 

Would love to see this integrated into some home assistant projects. Maybe pushing the updates to MQTT. 

## HMU

harper@nata2.org

@harper
