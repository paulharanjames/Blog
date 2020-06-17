
My search is to find simple way to use Log4Net in .NET application was futile. Finally, I decided to write sample code on my own 🙂

Step 1: Add reference to log4net.dll in your project (Project -> Add Reference -> Browse)  
Step 2: Add application configuration file (Project -> Resources -> Add new item -> app.config)  
Step 3: Add below in your app.config file in tag

The above example shows configuration to the RollingFileAppender to write to the file log.txt. The file written to will always be called log.txt because the StaticLogFileName param is specified. The file will be rolled based on a size constraint (RollingStyle). Up to 10 (MaxSizeRollBackups) old files of 100 KB each (MaximumFileSize) will be kept. These rolled files will be named: log.txt.1, log.txt.2, log.txt.3, etc..

Step 4: Initialize log object as below

dim log as log4Net.ILog

log = log4net.LogManager.GetLogger(&#8220;Emailer&#8221;)  
log4net.Config.XmlConfigurator.Configure()  
log.Debug(&#8220;Debug message&#8221;)

Simple, isn&#8217;t it?