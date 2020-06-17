
In last week, I received nearly 10 queries from users to configure SCS to use SMTP to send emails. It is very simple and straight-forward configuration and requires restart of SCS

Open or Create  **&#8216;mailer&#8217;** section in SCS and configure the following values

</p> 

  * **smtp_host**: host name of the SMTP Server


  * **smpt_por**t: port number of the SMTP Server


  * **smtp_from**: From email address
</ul> 

Any changes to smtp\_host and smtp\_port requires SCS restart for changes to take effect.  Changes to smtp_from effects immediately and no restart required.