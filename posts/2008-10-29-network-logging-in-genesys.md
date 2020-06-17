
<span><strong>How to configure network logging in Genesys ?</strong></span>

Network logging in Genesys is a multi-step process. First, the application sends the log record to Message Server. Message server sends record to update in DB.

1. Create Log Database 

2  Initialize the database using the scripts in Message Server installation folder

3. In Message Server, add connection to LogDAP

4. In Message Server, set property &#8216;messages\db_storage&#8217; as &#8220;true&#8221;

5. From any application object (like T-Server), add connection to the Message Server

Please note that log level should be set to network for any centralized logging. 

It is simple, isn&#8217;t it?