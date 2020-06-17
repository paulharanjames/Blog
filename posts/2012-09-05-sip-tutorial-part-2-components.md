
SIP elements are as below

_**User Agent:**_ The user agent resides in every SIP end station. It acts in two roles:

  * **User Agent Client (UAC):** Issues SIP requests
  * **User Agent Server (UAS)**: Receives SIP requests and generates a response that accepts, rejects, or redirects the request

Examples:  Softphone application, Messaging Client

_**Redirect Server:**_ The redirect server is used during session initiation to determine the address of the called device. The redirect server returns this information to the calling device, directing the UAC to contact an alternate _Universal Resource Identifier_ (URI). A URI is a generic identifier used to name any resource on the Internet. The URL used for Web addresses is a type of URI. See RFC 2396 [1] for more detail.

_****_ 

_**Proxy Server:**_ The proxy server is an intermediary entity that acts as both a server and a client for the purpose of making requests on behalf of other clients. A proxy server primarily plays the role of routing, meaning that its job is to ensure that a request is sent to another entity closer to the targeted user. Proxies are also useful for enforcing policy (for example, making sure a user is allowed to make a call). A proxy interprets, and, if necessary, rewrites specific parts of a request message before forwarding it.

_****_ 

_**Registrar:**_ A registrar is a server that accepts REGISTER requests and places the information it receives (the SIP address and associated IP address of the registering device) in those requests into the location service for the domain it handles.

_****_ 

_**Location Service:**_ A location service is used by a SIP redirect or proxy server to obtain information about a callee&#8217;s possible location(s). For this purpose, the location service maintains a database of SIP-address/ IP-address mappings.

 

In the next tutorial, we will review SIP command requests with more detail.