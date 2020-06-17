
Here is sample code to get last modified file from folder

<span>Dim directory As DirectoryInfo = New DirectoryInfo(&#8220;C:\Temp&#8221;)</span>  
<span>Dim filter As String = txtFileName.Text</span>

<span>If directory.GetFiles(txtFileName.Text).Count > 0 Then</span>  
<span>    Dim myFile As FileInfo = directory.GetFiles(filter).OrderByDescending(Function(f) f.LastWriteTime).First()</span>  
<span>    MsgBox(myFile.Name)</span>  
<span>Else</span>  
<span>    MsgBox(&#8220;No files found&#8221;)</span>  
<span>End If</span>

 