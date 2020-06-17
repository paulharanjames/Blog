
To restore windows state from minimized to previous state, use the following

_SendMessage(docView.Handle, WM\_SYSCOMMAND, SC\_RESTORE, 0);_

 