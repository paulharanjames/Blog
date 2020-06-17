
Option **on\_route\_error** defines what to do when an attempt to route a call resulted in an error, which is thrown by the Tserver to URS. If you are used to logs, you will find the EventError after RequestRouteCall. 

Possible choices include:  
default – Route the call to default destination  
ignore – Ignore the error  
delete – Delete the call from URS memory  
reroute – Repeat the request  
try_other – Find another target

Cheers!!  
Gururaj S