## Cheatsheet HTTP

`curl`:  Curl is a command line application that can send HTTP requests (like the browser, but with more options). 

`curl localhost:1901 --verbose` shows everything + Setup before HTTP, such as DNS and TCP/IP, Request sent to server, Response sent from server.  

### HTTP METHODS 

`curl localhost:1901 --verbose --request` + `....`

* `OPTIONS`: to find out which HTTP methods ones are supported for a resource (shows only the header, no data is sent back from the server). 

* `DELETE`: used to remove things, but API does not support removing. (`405 Method Not Allowed`)

* `HEAD`: is like GET, but tells the server not to send any data back (so without the body). Checking if something exists. 

* `POST --data '{}'`: is used to add something to a resource. 

* `PUT`: is used to place a resource somewhere, whether it already exists or not. 

* `PATCH`: change only a few things. 

* `GET --header 'Accept: application/xml'`: asking for XML

### Satus Codes

| Status        | A: server | 
| ------------- |:-------------:|
| Information | 1** | 
| Sucess | 2**      |
| Redirect | 3** |  
| Client error | 4** |   
| Server error | 5**      | 

**`201` Created** Success code for new resources 

**`400` Bad Request**

**`401` Unauthorized** Means that the thing you wanted to do may be possible, but only if you are authorized to do so.

**`404` Page Not Found** 

**`405` Method Not Allowed**

**`410` Gone** There used to be something there, but it no longer exists. 

**`422` Unprocessable Entity** Request was valid but there is something wrong with the data being sent to the server. 

