
As we all know, agent can handle calls from multiple queues in Genesys and is tricky to find EWT (Estimate Wait Time) for call during routing. I find that Genesys algorithm to be smart and most appropriate.

### How it is calculated?

* * *

Please find the details below (from Stat Server deployment guide)

**Estimated Wait Time (EWT) =  AHT \* ( CIQU / (AA \* EP))**

where

  * **AHT (Average Handle Time)** is calculated as **TotalTime(Mask1, Interval)/TotalNumber(Mask2, Interval)** 
      * Mask1 includes ACW time i.e. _CallReleased, ACWCompleted, CallMissed, ACWMissed_ events are used for calculation.
      * Mask2 is for call i.e.) _CallReleased_ and _CallMissed_ events only
      * If no calls are handled by agent for this queue, AHT is assumed to be 90 seconds
  * **CIQU (Calls in Queue Unassigned) –** Calls waiting in queue (CIQ) waiting for agent 
      * CIQU = 0 if agents in ready state (AR) > CIQ
      * CIQU = CIQ if no agents are currently ready
      * CIQU = CIQ – AR if some agents are in ready state
  * **AA (Active Agents)** – Agent logged in and is busy or not ready to take calls. If AA = 0, 0.0001 is used
  * **EP (Effective Portion) –** Total time spent by agent to process calls from the queue divided by total time spent by agent to process all calls. Default value : 1