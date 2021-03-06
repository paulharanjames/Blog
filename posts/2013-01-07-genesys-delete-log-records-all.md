
As we all know, Genesys applications can be configured to store log records in database. Unfortunately, there is no automatic maintenance option and have to purge data either manually or schedule script for this.

<h3 dir="ltr">
  Delete logs manually
</h3>

* * *

<h3 dir="ltr">
</h3>

You can use ‘Log Database Maintenance Wizard’ from Genesys SCI to maintain database. If there are large number of records in database, SCI application will become unresponsive and we have to kill it forcefully.

### Delete logs &#8211; Schedule it

* * *

### 

You can use steps below to automate the process. Fortunately, we don’t have to dig deep for this as SQL scripts are available from the wizard itself. You can easily find that log records are stored in two tables as below

  * G\_LOG\_MESSAGES
  * G\_LOG\_ATTRS

and to delete logs which are older than 15 days, use script below

<div>
  <div>
    <pre class="font:consolas toolbar:1 toolbar-overlay:false toolbar-hide:false nums-toggle:false whitespace-before:1 whitespace-after:1 lang:tsql decode:true">delete from G_LOG_ATTRS where LRID not in (select G_LOG_MESSAGES.ID from G_LOG_MESSAGES)

delete from G_LOG_ATTRS where LRID in (select G_LOG_MESSAGES.ID from G_LOG_MESSAGES where TIMEGENERATED &lt; DATEADD(DAY, -15, GETDATE()))

delete from G_LOG_MESSAGES where TIMEGENERATED &lt; DATEADD(DAY, -15, GETDATE())</pre>
  </div>
</div>

You need to run this in the same order as above and recommend to schedule to run every 24 hours. You can configure this as SQL Server Agent job or run this sql as scheduled task from windows.