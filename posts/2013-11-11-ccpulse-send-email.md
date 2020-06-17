
  * Create threshold using Genesys CCPulse threshold wizard

  * Download &#8216;vbSendEmail.dll&#8217; from <http://www.freevbcode.com/ShowCode.Asp?ID=109> and copy it in CCPulse+ folder (typically, &#8216;GCTI\CCPulse+&#8217;)
  * Using command prompt, navigate to CCPulse+ folder and register dll using the following command

> **regsvr32** vbSendMail.dll

  * Create action script as below

<pre class="lang:vb decode:true">Set poSendMail = CreateObject("vbSendMail.clsSendMail")
poSendMail.SMTPHost = ""
poSendMail.From = ""
poSendMail.FromDisplayName = ""
poSendMail.Recipient = ""
poSendMail.RecipientDisplayName = ""
poSendMail.ReplyToAddress = ""
poSendMail.Subject = "CCPulse Notification"
poSendMail.Attachment = ""
poSendMail.Message = ""
poSendMail.Send
Set poSendMail = Nothing</pre>

&nbsp;