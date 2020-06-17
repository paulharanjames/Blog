
Ever wondered how to remove multiple selected items from list box in VB6? Trick here is loop through listbox in REVERSE.

Here is the sample and enjoy 🙂

_Dim intCount As Integer_

_For intCount = (lstSample.ListCount -1 1) To 0 Step -1_

> _If lstSample.Selected(intCount) Then_

> _lstSample.RemoveItem intCount_

_End If_

_Next_