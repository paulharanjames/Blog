
Whenever I raise SR with Genesys, they request for DB Version (exact version) to troubleshoot the problem. Here, I listed one easy way to find SQL Server 2005 version 🙂

To determine which version of Microsoft SQL Server 2005 is running, connect to SQL Server 2005 by using SQL Server Management Studio, and then run the following Transact-SQL statement.

SELECT  SERVERPROPERTY(&#8216;productversion&#8217;), SERVERPROPERTY (&#8216;productlevel&#8217;), SERVERPROPERTY (&#8216;edition&#8217;)

The following results are returned: 

  * The product version (for example, 9.00.1399.06) 
  * The product level (for example, RTM) 
  * The edition (for example, Enterprise Edition)

Reference: [http://support.microsoft.com/kb/321185](http://support.microsoft.com/kb/321185 "http://support.microsoft.com/kb/321185")