
Do you know that you can use JScript language to build custom statistics in Genesys CCPulse application? In my opinion, this is very powerful feature in CCPulse, allowing to customise basic statistics, integrate with external applications/databases and thus, allowing you to build your own performance management solution.

Instead of making use of this feature, I have seen engineers spending many days in modifying routing strategies and developing reports whereas it as simple task of creating CCPulse templates. This article is to help them to develop custom reports in CCPulse ![](/wp-content/uploads/2014/05/wlEmoticon-smile.png)
 
# Using JScript language

* * *

JScript is the Microsoft implementation of the ECMA 262 language specification (ECMAScript Edition 3).  While defining custom statistics, you can use the arithmetic operators and delimiters available in this language, including: + / * – . ? : == ( ) ; != +=

Please refer to the following link [http://msdn.microsoft.com/en-us/library/hbxc2t98(v=vs.84).aspx](http://msdn.microsoft.com/en-us/library/hbxc2t98(v=vs.84).aspx "http://msdn.microsoft.com/en-us/library/hbxc2t98(v=vs.84).aspx")

# Using Predefined Statistics and Objects

* * *

To use this feature, make sure you set **‘ExtendedCurrentStatus’** configuration in CCPulse+ application to **‘true’**

CCPulse+ uses the following syntax for referencing basic statistics in formulas:

_**ccpulse.group(“StatisticGroupName”).statistic(“StatisticName”);**_

The trailing semicolon is optional. CCPulse+ includes the name of the statistic group to distinguish the statistic, in case another statistic of the same name exists in another statistical group. If either StatisticGroupName or StatisticName contains no spaces, CCPulse+ drops the corresponding group  
and statistic delimiters, the parentheses, and the double quotes:

**_ccpulse.StatisticGroupName.StatisticName_**

Using above, you can add calls queued statistics from Inbound Queue, Transfer Queue and CallBack Queue and present it as ONE value so that it is easy to understand and action against it for call center managers.

# Can you connect to Database?

* * *

Yes, as CCPulse+ uses JScript language,  you can easily connect to database to retrieve/update/insert values in database. In the below example, I connect to SQL Server database to list skills associated with the agent in CCPulse.

### CCPulse View

* * *

![](/wp-content/uploads/2014/04/image.png)

![](/wp-content/uploads/2014/04/image_thumb.png)
  
  <p class="wp-caption-text">
    Agent View in CCPulse
  </p>
</div>

### Script to view current skill associated with the agent

* * *

<pre class="font:consolas toolbar:1 toolbar-overlay:false toolbar-hide:false toolbar-delay:false nums-toggle:false whitespace-before:1 whitespace-after:1 lang:vb decode:true" title="Script">var rs = new ActiveXObject("ADODB.Recordset");
var conn= &lt;SQL Server Connection String&gt;;

var strEmpl = state.AgentID;
var query = "select ( b.name + '=' + cast (a.level_ as varchar(25))) as name from cfg_skill_level a inner join cfg_skill b on a.skill_dbid=b.dbid "+
          "where a.person_dbid=(select dbid from cfg_person where employee_id='"+strEmpl+"')";
rs.open(query,conn,0,1,1);
var res = "";
res;

var res = "";
 
if (rs.EOF != true) {
  rs.MoveFirst();
  while (rs.EOF != true) {
    if (rs("name").Value != null) {
      res = (res == "" ? rs("name").Value : res+"; "+rs("name").Value);
    }
    else {
      res = "NULL";
    }
    rs.MoveNext();
  }
}
rs.Close
rs = null;
res;</pre>
