
Yes.. This could be a rare scenario as you think. But if you have used T-server with switch simulator,chances are more that you could have encountered this problem.

In this case, the T-server disconnects from the switch and status changes to &#8220;**_Service Unavailable_**&#8220;.But after a while, the switch &#8211; Tserver connection is restored and the status becomes &#8220;started&#8221;. Again, this doesn&#8217;t last for much time. Just wait for some 45 seconds and the link goes down. And this game continues to give the same trouble.

**Solution**: In T-server, the option **ts-tp-enabled** should be set to **false** and this will fix the problem if you are as lucky as i am.. 🙂