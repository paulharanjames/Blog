
If you are getting errors connecting to SQL Server Express 2005 via remote client software and don&#8217;t have any problem connecting to it from the local machine, this post might be useful to you

If you are getting the error messages listed below, then we might have solution for you 🙂

<ul type="disc">
  </p> 
  
  <li>
    sql server does not allow remote connections
  </li>
  <p>
  </p>
  
  <li>
    SQL Network Interfaces, error: 26 &#8211; Error Locating Server/Instance Specified
  </li>
  <p>
  </p>
  
  <li>
    An error has occured while establishing a connection to the server. When connecting to SQL Server 2005,this failure may be caused by the fact that under the default settings SQL Server does not allow remote connections.(provider:Named Pipes Provider,error:40-Could not open connection to SQL Server))
  </li>
  <p>
  </p>
  
  <li>
    Server does not exist or access denied
  </li>
  <p>
    </ul> 
    
    <p>
      This issue occurs because SQL Server Express 2005 is not automatically configured for remote access and have to enabled  manually 🙁
    </p>
    
    <p>
      Follow the steps below to enable remote access in SQL Server Express 2005
    </p>
    
    <ol type="1">
      </p> 
      
      <li>
        Enable the TCP/IP protocol using the Surface Area Configuration Utility for remote connections
      </li>
      <p>
      </p>
      
      <li>
        Enable the TCP/IP protocol in the SQL Server Configuration Utility
      </li>
      <p>
      </p>
      
      <li>
        Make sure the SQL Server browser is started
      </li>
      <p>
      </p>
      
      <li>
        Restart the system for changes to take effect
      </li>
      <p>
        </ol> 
        
        <p>
          If you have any other suggestions, please let me know via comments and will update the post accordingly.
        </p>