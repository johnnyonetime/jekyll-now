There are a few possible scenarios:

1. Your reciever is digital (i.e. S.Bus) and can signal failsafe to the FC on it's own.

Just set a failsafe behavior in Failsafe tab - no need for special action.

2. Your receiver goes to "no pulses" and stops sending signal in case of RC link loss

Just set a failsafe behavior in Failsafe tab - no need for special action.

3. Your receiver can't signal failsafe but you can configure it to go to pre-set channel values.

Configure Roll, Pitch, Yaw to middle, Throttle to zero, one of the AUX channels to activate FAILSAFE mode. Set a failsafe behavior in Failsafe tab.
WARNING! Don't configure your receiver to go into RTH mode - explanation below.

5. Your receiver can drop one of the channels below zero (considerably below 1000)

Adjust rx_min_usec so in case of RC link loss signal will be considered invalid. Leave some margin for error. Make sure failsafe don't activate by ANY manual activity. Set a failsafe behavior in Failsafe tab.

6. Your receiver doesn't care about failsafe and holds all channels to their last known values

Throw your receiver out of the window and go get yourself a better one.

Why activating RTH on receiver-side is a BAD idea

In general you may wish to activate NAV RTH mode by a pre-set failsafe values on your receiver. From FC point of view - there is nothing out of ordinary and pilot wants to activate RTH manually. FC is unaware that RC link is lost. While this will work in most cases - here are a few that may lead to a fly-away or crash:

1. Flying with no GPS or no HOME available. This may be temporary loss of GPS, or you have extra safety off and started flying before GPS lock. In this case manual RTH won't activate at all and machine will continue flying as it was. Failsafe RTH will enter emergency landing and land the machine close to the place where link was lost leaving you a chance to recover the machine somewhere close to last known GPS coordinates.

2. Receiving wire disconnecting. This will be treated by FC as a RC signal loss even if the real radio link is still good. If you didn't configure failsafe behavior in Failsafe tab it will by default drop throttle to idle and fall out of the sky (in case of a multirotor) or spiral down (in case of a fixed wing).
