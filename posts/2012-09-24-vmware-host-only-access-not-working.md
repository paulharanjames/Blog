
I have VM running Windows Server 2003 configured to use ‘Host-Only’ network connection. After upgrading from VMware player to workstation, I can no longer communicate between the host and the VM. I googled around for this issue and found simple solution as below

  * Go to Edit-> Virtual Network Editor

[<img title="network editor" border="0" alt="network editor" src="http://lh6.ggpht.com/-ycKLRd57tBY/UGCQojWrg3I/AAAAAAAAABE/EK9IwWFfbq8/network%252520editor_thumb%25255B5%25255D.png?imgmax=800" width="575" height="508" />](http://lh5.ggpht.com/-3Yw6PlXQ0Yg/UGCQm_PlvmI/AAAAAAAAAA8/_OjIReM8TRA/s1600-h/network%252520editor%25255B9%25255D.png)

  * Select VMnet1 , uncheck ‘Connect a host virtual adapter to this network’ and click ‘Apply’
  * Check ‘Connect a host virtual adapter to this network’ (basically adding it again…) and click ‘Apply’

 

That’s it. VMnet1 gets static IP address and issue is resolved..