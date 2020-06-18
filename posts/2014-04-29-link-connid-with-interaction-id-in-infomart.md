
<font size="3" face="Calibri">In Genesys environment, most of us are still used to track call information using Connection Id (ConnID). However, Genesys Infomart (GIM), core subject areas are linked with interaction id and this post will help you to get interaction id using connid or vice versa.</font>

### To get interaction id using conn id

  * <font size="3" face="Calibri">Login into Genesys Icon database and query ‘g_call’ table using your conn id as below. </font>

<font color="#008000" face="Calibri">select&nbsp; id, callid, connid, irid, rootirid from g_call where connid = <strong><em>< your conn id here></em></strong></font>

<font face="Calibri">From the results, take note of rootirid. A call can have multiple conn id due to transfers and column ‘rootirid’ links call records like below</font>

![](/wp-content/uploads/2014/04/clip_image001.jpg)

![](/wp-content/uploads/2014/04/clip_image001_thumb2.jpg)

![](/wp-content/uploads/2014/04/clip_image0012.jpg)

  * <font face="Calibri">Now, login into Genesys Infomart database and query ‘interaction_fact’ using query below</font>

<font color="#008000" face="Calibri">select * from interaction_fact where media_server_ixn_guid = <strong><em><your root irid here></em></strong></font>

![](/wp-content/uploads/2014/04/image_thumb.png)

![](/wp-content/uploads/2014/04/image.png)
