
Quick and useful tip..

 

Private Sub MyForm\_Closing(ByVal sender As System.Object, ByVal e As \_  
            System.ComponentModel.CancelEventArgs) Handles MyBase.Closing  
Try  
   Select Case MessageBox.Show(&#8220;Are you sure you want to close this window?&#8221;, _  
      &#8220;Your application&#8221;, MessageBoxButtons.YesNo, MessageBoxIcon.Question)  
    Case MsgBoxResult.Yes  
     &#8216;Do Nothing  
    Case MsgBoxResult.No  
     e.Cancel = True  
   End Select  
Catch ee As Exception  
  Throw ee  
End Try  
End Sub