
Recently, a team member asked me whether the agent can apply the treatment only when he wants to.

Answer for it is **&#8220;YES&#8221;**. From version 7.0.201.05 release, new option is available in Genesys to activate this functionality. We need to configure the following values in &#8216;GAD&#8217; application object to enable the agent to select the treatment

Section             : **outbound**

Option Name   : **treatment**

Value               : **agent-selection**

From the next call onwards, there will be drop-down box near the **&#8220;Mark Done&#8221;** button in GAD to select the treatment.

If you have any more tips, please send it to blakshmikath (@) gmail (dot) com