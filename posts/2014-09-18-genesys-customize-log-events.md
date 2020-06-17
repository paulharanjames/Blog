
Do you know that log events can be customized from version 7.6 in Genesys? Wait, what is this &#8216;log event customization&#8217;?

Simple. Genesys allows you to define log level for each log message and you can customize it per application.

Oh &#8230; but why do I need to customize log events?

To explain this, I will start with real case scenario. Recently, I got an assignment to review Genesys solution as they were getting default routed calls during busy period and implement/recommend methods to improve solution performance.

After identifying and solving configuration, routing strategy, reporting and staffing allocation issues, they were still getting default routed calls. At this point, this is as much as you can do within Genesys standard tools. Next, I developed tool to find &#8216;default routed calls&#8217; for analysis (<a title="Tool to find default routed calls" href="http://www.lakshmikanth.com/tool-to-find-default-routed-calls/" target="_blank" rel="noopener noreferrer">here</a>) , which helped me to identify call patterns and fix issues -both technical and process.

For obvious reasons, customer like to use this tool functionality &#8211;  to identify default routed calls and don&#8217;t need other features like reporting & logging etc. I can develop server application (good for me) but it is overweight solution for this requirement and want to keep it simple.

Analyzing URS logs and log messages, I found that I can configure alarm condition for log message &#8217;15-20003&#8242; which will help to store Conn ID and timestamp for further analysis. Exactly what I want !!

<div id="attachment_4061" style="width: 1212px" class="wp-caption aligncenter">
  <a href="http://localhost/newlakshmikanth3/wp-content/uploads/2014/09/URSDefaultRouting1.png" target="_blank" rel="noopener noreferrer"><img aria-describedby="caption-attachment-4061" class="wp-image-4061 size-full" src="http://localhost/newlakshmikanth3/wp-content/uploads/2014/09/URSDefaultRouting1.png" alt="URS Log Message" width="1202" height="343" srcset="http://localhost/newlakshmikanth3/wp-content/uploads/2014/09/URSDefaultRouting1.png 1202w, http://localhost/newlakshmikanth3/wp-content/uploads/2014/09/URSDefaultRouting1-300x86.png 300w, http://localhost/newlakshmikanth3/wp-content/uploads/2014/09/URSDefaultRouting1-1024x292.png 1024w, http://localhost/newlakshmikanth3/wp-content/uploads/2014/09/URSDefaultRouting1-768x219.png 768w" sizes="(max-width: 1202px) 100vw, 1202px" /></a>
  
  <p id="caption-attachment-4061" class="wp-caption-text">
    URS Log Message
  </p>
</div>

But I dont want to recommend interaction level logging information to be stored in log database for this piece of information. I want to improve overall solution performance and interaction level logging to log database will increase network traffic 🙁

This is an ideal scenario to use &#8216;log event customization&#8217; feature from Genesys. From 7.6 version onwards, we can customize this log event i.e) change level from **&#8216;INTERACTION&#8217;** to &#8216;**STANDARD&#8217;** and configured **&#8216;STANDARD&#8217;** level logging to &#8216;network&#8217;.

Even though, 20003 log level message is &#8216;INTERACTION&#8217; level logging, it will be reassigned dynamically and sent to Message server to store it in log database. For customer notification, I configured alarm condition for this log event and send email notification <a title="Genesys CCPulse – How to send email notification?" href="http://www.lakshmikanth.com/ccpulse-send-email/" target="_blank" rel="noopener noreferrer">(How to send email notification?</a>)

Problem solved 🙂

**Update 24th Sep 2014 :** Please visit post <a title="Genesys – Customize log events" href="http://www.lakshmikanth.com/genesys-customize-log-events/" target="_blank" rel="noopener noreferrer">&#8216;Genesys – How to customize log events?&#8217;</a> for step by step guidance on configuring log event customization,