
The Primary/Backup Config Server configuration is absolutely transparent for all client applications. When a client connects to Primary Config Server, it requests information if there is a Backup instance configured. If there is, the client (here IVR Driver) gets all necessary attributes, like Host and Port. When the Primary config server fails the client will be trying to reconnect to Primary, then to Backup, until succeeds.

Actually, the same rule could be applied for Primary/Backup pairs of any Genesys servers – (they are transparent for their clients)

The bottom line is that as long as one config server of the pri/back pair is up and running there will be no problem getting the IVR Driver up and connected. If it cannot connect to either one, then there will be a problem. Otherwise it will be fine. Also, once it starts running you can take both config servers down and have no issues&#8230;it is just on start-up where it is key to get the config parameters.

**Note:** Got this info for Genesys support and really helped me to talk to Nortel IVR Engineers..