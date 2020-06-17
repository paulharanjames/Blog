
<span><strong>&#8220;verification_time&#8221;</strong></span> specifies the amount of time that must elapse to consider the agent as available in Genesys to receive interactions from URS (even when the agent is in available mode in PBX).

For ex, consider the verification time as **15 seconds.**

</p> 

  * Agent (agent1) logs into the softphone and make himself available at **10:00:00 AM**


  * PBX will show the agent state as &#8220;Ready&#8221;


  * When the verification time elapses **i.e) 10:00:15 AM**, URS will consider the agent as &#8220;Ready&#8221; to receive interactions.
</ul> 

This allows agent to prepare for the next call. Please note that this applies every time the agent moves into ready state.

Special thanks to **Reinoud, Accenture** for making corrections.