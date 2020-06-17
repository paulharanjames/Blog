
During my current implementation, I faced issues in installing Hyperion with SQL Server 2005. Finally, figured out solution to install Hyperion with SQL Server 2005 

In order to install Hyperion Repository on SQL Server 2005 Hyperion 8.5. (SP3) installer should be used as it contains updated MS SQL JDBC drivers which function correctly with SQL Server 2005. The Hyperion Performance Suite 8.5 SP1 and up does support SQL Server 2005 just the installer does not. There are several workarounds available such as installing Hyperion Repository on SQL Server 2000 then following the procedure migrating it to SQL Server 2005, or to use Hyperion Installer 8.5 SP1 and above with updated JDBC driver in override directory. 

To install HpSu SP3 on SQL Server 2005 repository given the latest Genesys CD availability you needs to use the HpSu 8.5 SP3 installer. 

Please use &#8216;Full Hyperion INTELLIGENCE SERVER 8.5.0.3&#8217; for installation