
This is only an example. You will need to test this to see if it satisfies your requirements&#8230;

All variables in the example below are of type &#8220;Integer&#8221; (not Float) except for the &#8220;**StartTime**&#8221; variable in the example below which is of type String. 

A Multi-Assign object in the IR Designer could be used as follows to obtain the timestamp in the format you are looking for (hh:mm:ss): 

Variable name: Value: 

> _TimeStarted => TimeStamp[] / 1000  
> TimeHour => TimeStarted / 3600  
> TimeMinute => (TimeStarted &#8211; (TimeHour * 3600)) / 60  
> TimeSecond => TimeStarted &#8211; (TimeHour \* 3600) &#8211; (TimeMinute \* 60)  
> StartTime => Cat[Cat[Cat[Cat[TimeHour,&#8217;:&#8217;],TimeMinute],&#8217;:&#8217;],TimeSecond]_
> 
>  
> 
> Update (attach) the value of the StartTime variable to the call as userdata.