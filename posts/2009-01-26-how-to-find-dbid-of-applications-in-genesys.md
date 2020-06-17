
In Genesys, you need to know DBID of applications to configure alarms/blocking logs from Message Server.  Ever wondered to find out DBID of the application&#8230; Here is the trick&#8230;

Open configuration manager (CME) from command prompt, using the **-d** command line parameter. For example, &#8220;D:\GCTI\SCE.exe -d&#8221;.. That&#8217;s it 🙂

Now you will find the application DBID in the Application Properties Dialog box.

If you want to view the DBID by default, right click the CME shortcut and add &#8220;-d&#8217; in target text box.