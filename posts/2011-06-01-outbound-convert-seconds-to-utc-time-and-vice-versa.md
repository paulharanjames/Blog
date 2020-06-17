
To convert date from export file to seconds passed after 01/01/1970 in Genesys format)

<span><em>       Dim sDate As String = &#8220;01/06/2011 16:46:44&#8221;</em></span>  
<span><em>       Dim date1 As Date = #1/1/1970#</em></span>

<span><em>       Dim date2 As Date = DateTime.Parse(sDate).ToUniversalTime</em></span>

<span><em>       inSeconds = DateDiff(&#8220;s&#8221;, date1, date2))</em></span>

<span>To convert seconds from database to date and time</span>

<span>        Dim localTime As Date</span>

<span>        Dim date1 As Date = #1/1/1970#</span>

<span>        localTime = date1.AddSeconds(1306943204).ToLocalTime</span>

<span>        Debug.Print localtime.ToString</span>