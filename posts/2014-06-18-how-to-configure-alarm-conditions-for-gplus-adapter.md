
<span style="color: #000000;">GPlus Adapter for Aspect eWFM supports alarm codes for major errors, so that it can be monitored on SCI or Genesys Administrator. For this feature to work correctly, alarm codes must match up with log event id defined in the alarm condition.</span>

<div style="color: #000000;">
  In my environment, I configured GPlus Adapter to send alarm codes as below
</div>

<div style="color: #000000;">
</div>

<div style="color: #000000;">
  
  ![](/wp-content/uploads/2014/06/GPlusAdapterOptions.png)
  
</div>

<div style="color: #000000;">
</div>

<div style="color: #000000;">
   Now, you need to create alarm condition to match alarm codes as below
</div>

<div style="color: #000000;">
  <div>
    <p>
      In Genesys Administrator, you can create a new Alarm Condition:
    </p>
    <ol>
      <li>
        Go to Provisioning > Environment > Alarm Conditions.
      </li>
      <li>
        If required, navigate to the folder in which you want to store the new Alarm Condition.
      </li>
      <li>
        Click 
            
  ![](/wp-content/uploads/2014/06/NewAC.png)
         
  </li>
      <li>
        On the Configuration tab, enter or modify information as required.
      </li>
      <li>
        On the Options tab, enter or modify information as required.
      </li>
      <li>
        To save the new Alarm Condition and register it in the Configuration Database, do one of the following: <ul>
          <li>
            Click 
            
   ![](/wp-content/uploads/2014/06/SaveAC.png)
            
 to continue configuring the Alarm Condition.
          </li>
        </ul>
      </li>
    </ol>   
    <div>
      In the screenshot below, I created &#8216;diskWriteFailure&#8217; alarm with log event Id as 9001 and cancel log event id as 9002. You can fine tune this by setting &#8216;Detect Selection Mode&#8217; to &#8216;Select by Application&#8217; and selecting &#8216;GPlusAdapter&#8217; application in &#8216;Detect Application&#8217;.
    </div>
  </div>
  
  <div>
  </div>
  
  <div>
    Two main items to note here
  </div>
  
  <div>
    <ul>
      <li>
        9001 &#8211; I selected 90XX number series to configure custom alarms as other series are used by other components
      </li>
      <li>
        9002 &#8211; Another custom alarm configured for &#8216;diskWriteSuccess&#8217;
      </li>
    </ul>
  </div>
  
  <div>
  
   ![](/wp-content/uploads/2014/06/Alarm-Condition1.png)
  
  </div>
  
  <div>
  </div>
  
  <div>
    By following above steps, you can configure alarm conditions and assign reaction scripts to get notifications 🙂
  </div>
  
  <p>
    &nbsp;
  </p>
</div>
