
To permit IIS to serve dynamic content, the administrator must unlock this content in the Web service extensions node in IIS Manager. To do this, the administrator must either enable a pre-existing Web service extension or add a new Web service extension.

**Enable a Pre-existing Web Service Extension in IIS 6.0** 

To permit IIS to serve content that requires a specific ISAPI or CGI extension that is already listed in the Web service extensions list, follow these steps: 

  1. Open IIS Manager, expand the master server node (that is, the <var>Servername</var> node), and then select the **Web service extensions** node. 
  2. In the right pane of IIS Manager, right-click the extension that you want to enable. In this example, this is **Active Server Pages**. 
  3. Click to select the **Allow** check box. 

**Add a New Web Service Extension to IIS 6.0** 

To permit IIS to serve content that requires a specific ISAPI or CGI extension that is not already listed in the Web service extensions list, follow these steps: 

  1. Open IIS Manager, expand the master server node, and then select the **Web service extensions** node. 
  2. In the right pane of the IIS Manager, click **Add a new Web service extension** under **Tasks**. 
  3. In the **Extension name** box, type a friendly name for the extension that you want to add (for example, FrontPage Server Extensions). 
  4. In the **Required files** box, click **Add**, and then select the path and the name of the file that will handle requests for the specific extension. After you select the path and the file name, click **OK**. 
  5. If the extension must be enabled immediately, click to select the **Set extension status to allowed** check box. 
  6. Click **OK** to save your changes. 

For more information, please refer to [http://support.microsoft.com/kb/315122](http://support.microsoft.com/kb/315122 "http://support.microsoft.com/kb/315122")