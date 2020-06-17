
VB6 Snippet to delete old log files

Private Sub deleteOldFiles() 

Dim sFileName As String  
Dim sFileSplit() As String  
Dim sFileSpec As String  
Dim sDir As String  
Dim iCount As Integer  
Dim iCtr As Integer  
Dim dCompDate As Date  
Dim dFileDate As Date 

On Error GoTo errHandler 

sFileSpec = App.Path & &#8220;\logs\*.log&#8221;  
sFileName = Dir(sFileSpec) 

dCompDate = Format(Now, &#8220;mm/dd/yyyy&#8221;) 

Do  
    If sFileName = &#8220;&#8221; Then Exit Do  
        If InStr(sFileSpec, &#8220;\&#8221;) > 0 Then  
            sFileSplit = Split(sFileSpec, &#8220;\&#8221;)  
            iCount = UBound(sFileSplit) &#8211; 1  
                For iCtr = 0 To iCount  
                    sDir = sDir & sFileSplit(iCtr) & &#8220;\&#8221;  
                Next  
            sFileName = sDir & sFileName  
        End If  
        dFileDate = Format(FileDateTime(sFileName), &#8220;mm/dd/yyyy&#8221;)  
        If DateDiff(&#8220;d&#8221;, dFileDate, dCompDate) >= 3 Then  
         &#8216;Get File Attributes  
          If GetAttr(sFileName) = 33 Then  
             SetAttr sFileName, 32  
          End If  
         Kill sFileName  
        End If  
    sFileName = Dir  
    sDir = &#8220;&#8221;  
Loop 

Exit Sub 

errHandler: 

MsgBox Err.Number & &#8220;:&#8221; & Err.Description 

End Sub