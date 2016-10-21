#HTTP API 0.01 alpha

Protocol: HTTP port 80
Request: GET (action, value)
Response: plain-text

#Actions             

show-home
value: null
response: OK

show-browser
value: url web page to show
response: OK

get-power 
value: null 
response: motor power (0=off, 1, 2, 3)

set-power 
value: motor power (0=off, 1, 2, 3) 
response: OK / ERR

get-light 
value: null 
response: light power (0=off, 1, 2, 3)

set-light 
value: light power (0=off, 1, 2, 3) 
response: OK / ERR

get-mirror 
value: null 
response: mirror status (0=monitor, 1=mirror)

set-mirror 
value: stato specchio (0=monitor, 1=mirror) 
restituisce: OK 

browser-up 
value: null 
response: OK

browser-down 
value: null 
response: OK

show-image (* obsolete)
value: index image
restituisce: OK / ERR

get-image 
value: null 
response: index image actually showed

show-slider 
value: ID slider
restituisce: OK

image-prev 
value: null 
restituisce: OK

image-next 
value: null 
restituisce: OK

get-sensors 
value: null 
response: array ID of sensors divided by “|”

get-sensor-info 
value: ID sensor (obtained by get-sensors) 
response: <name>|<um>|<value>|<alarm>

set-sensor-info
value: <ID>|<name>|<um>|<value>|<alarm>
response: OK
<ID> is unique, not use 1 to 150

get-output 
value: ID
response: <name>|<um>|<value>

set-output 
value: <ID>|<value>
response: OK / ERR

register-output 
value: <ID>|<name>|<um>|<url>
response: OK / ERR
<url> is the url of the GET to notify device after a “set-output”. The system start a GET using the url follower by
“action=set-output&value=<ID>|<value>”
<ID> is unique, not 1 to 10
