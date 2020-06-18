
To enable longer call recordings in GVP, you need to change the configuration value in GVP and procedure is as follows:

1. Open IIS.  
2. Right-click the server, and then select Properties.  
3. Select the **Enable Direct Metabase Edit** check box, and then click OK.  
4. Open the MetaBase.xml file, which is located in “**C:\WINNT\System32\Inetsrv**”  
5. Locate the line **AspMaxRequestEntityAllowed**, and change it to 524288000. 

Please note that the above steps was tested in IIS 6.0 version and above
