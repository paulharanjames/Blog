
After spending few days, finally able to figure socket disconnect detection in .NET 🙂 

 

Public Shared Function IsConnected(ByVal socket As Socket) As Boolean  
        Try  
            Return Not (socket.Poll(1, SelectMode.SelectRead) AndAlso socket.Available = 0)  
        Catch generatedExceptionName As SocketException  
            Return False  
        End Try  
End Function

In Timer_tick event, keep checking for connection status.  If return value is ‘false’, we can say that socket is disconnected now 🙂