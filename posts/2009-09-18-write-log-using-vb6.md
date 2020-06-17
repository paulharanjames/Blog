
Function to write log file using Visual Basic 6

Private Sub writeLog(strMessage As String) 

Dim hFile As Long  
Dim sFolder As String  
Dim sFile As String  
Dim sDestination As String  
Dim sLog As String 

On Error GoTo errHandler 

hFile = FreeFile()  
sFolder = App.Path & &#8220;\logs&#8221;  
sFile = sFolder & &#8220;\Softphone.log&#8221; 

sLog = Format(Now(), &#8220;yyyy-mm-dd HH:nn:ss&#8221;) & &#8220;.&#8221; & Right(Format(Timer(), &#8220;0.000&#8221;), 3)  
sLog = sLog & vbTab & strMessage 

If lLineNumber > 60000 Then &#8216;Approx 5 MB  
    lLineNumber = 1  
    sDestination = sFolder & &#8220;\Softphone\_&#8221; & Format(Now(), &#8220;yyyymmdd\_HHnnss&#8221;) & &#8220;.log&#8221;  
    FileCopy sFile, sDestination  
    Kill sFile  
Else  
    lLineNumber = lLineNumber + 1  
End If 

Open sFile For Append As #hFile  
    Print #hFile, sLog  
Close hFile 

Exit Sub 

errHandler: 

If Err.Number = 76 Then &#8216;If folder not exists, create it  
    MkDir sFolder  
    Resume  
End If  
MsgBox Err.Number & &#8220;:&#8221; & Err.Description 

End Sub