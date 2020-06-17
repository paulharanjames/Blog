
Good example for iterating through dictionary object…

> Dim DictObj As New Dictionary(Of Integer, String)  
> 
> DictObj.Add(1, &#8220;ABC&#8221;)  
> 
> DictObj.Add(2, &#8220;DEF&#8221;)  
> 
> DictObj.Add(3, &#8220;GHI&#8221;)  
> 
> DictObj.Add(4, &#8220;JKL&#8221;)  
> 
> For Each kvp As KeyValuePair(Of Integer, String) In DictObj  
> 
> Dim v1 As Integer = kvp.Key  
> 
> Dim v2 As String = kvp.Value  
> 
>      Debug.WriteLine(&#8220;Key: &#8221; + v1.ToString _  
> 
>             + &#8221; Value: &#8221; + v2)  
> 
> Next

For more information, please refer to [http://msdn.microsoft.com/en-us/library/xfhwa508.aspx](http://msdn.microsoft.com/en-us/library/xfhwa508.aspx "http://msdn.microsoft.com/en-us/library/xfhwa508.aspx")