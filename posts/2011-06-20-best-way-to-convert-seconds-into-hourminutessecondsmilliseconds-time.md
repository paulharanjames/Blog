
Just use the TimeSpan class.

    TimeSpan t = TimeSpan.FromSeconds(secs);<br><br>string answer = string.Format("{0:D2}h:{1:D2}m:{2:D2}s:{3:D3}ms", <br> t.Hours, <br> t.Minutes, <br> t.Seconds, <br> t.Milliseconds);<br>