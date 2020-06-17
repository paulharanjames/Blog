
The Configuration Server Application object is preconfigured in the Configuration Database. You need to make the below changes in the Configuration  
Server Application in CME for Management Layer to control Configuration Server:

  1. Open Configuration Manager aka CME
  2. Create a ‘**Host’** object for the computer on which Configuration Server runs
  3. Open the Properties dialog box of the ‘**Configuration Server’** Application (named **‘confserv’**)
  4. Click the **‘Server Info’** tab
  5. Click Browse to select the Host that you created in **Step 2**
  6. On the ‘**Start Info’** tab, define the **‘Working Directory’** and **‘Command Line’** properties for the primary Configuration Server
  7. Click **OK** to save the changes.