
We recently migrated our servers to Windows 2012 and it doesn&#8217;t have windows security option to change your password (like in Windows 2008). In this post, I will explain two options to change password in Windows 2012 on RDP session

## Option 1 : Change password in Remote Desktop Session (RDP)

* * *

  * Press CTRL + ALT + END on remote session. This is equivalent to CTRL + ALT + DEL on your local machine and you will be able to change password.

## Option 2: Change password in RDP session through jump server

* * *

It is common that customer provide access to servers (For example : APPSERVER01) through jump server (Example: GATEWAYSERVER01) . In these scenarios, CTRL + ALT + END will not work as you RDP into jump server &#8216;GATEWAYSERVER01&#8217; and from jump server, RDP into application server &#8216;APPSERVER01&#8217;. In this case, use below steps to change your password

  * Press Windows Key + R and type &#8216;OSK&#8217; to bring onscreen keyboard
  * Press &#8216;CTRL&#8217; + &#8216;ALT&#8217; in your keyboard and using mouse,  press &#8216;DEL&#8217; button on on-screen keyboard
  * It will bring &#8216;Change Passsword&#8217; option

If you know about any other options, share it in your comments

&nbsp;