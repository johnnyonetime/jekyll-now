Instructions for setting up the V.KEL VK2828U7G5LF GPS (and possibly other GPS modules with a uBlox chipset) using the uCenter S/W.

-To set up the GPS unit in uCenter, make sure the baud rate and com port for both the gps and u-center are the same:

A. Click on Reciever on the Main Toolbar (Menu Bar). From this drop down menu:

1. Click Baudrate and select 9600 (OR whatever baud rate your GPS is currently set to).
2. Click Port and select the correct Serial Port for your TTL adapter/GPS Unit.
3. Put a checkmark beside of Autobauding.

B. From the Main Toolbar, Click View, then select Messages View. In the new window that opens below the Main Toolbar you will open the [+] UBX tree, then open the [+] CFG (Config) tree:

1. Click on RATE (Rates)
2. Set Measurement Period to 200 (this automatically changes the Measurement Frequency to 5Hz).
3. At bottom left of the new window, click the Send button (to the right of the padlock and "x" icons).

1. Click on PRT (Ports)
2. Set baud rate to 57600
3. At bottom left of the open window, click the Send button (to the right of the padlock and "x" icons).

Now here is a confusing part:

C. Under the main Config tree, there is another Config tree! 

1. Click on CFG (Configuration)
2. Highlight ALL four of the devices shown (very important)!
3. Make sure "Save current configuration" option is marked.
4. At bottom left of the open window, click the Send button (to the right of the padlock and "x" icons).
5. Verify that ALL four of the devices are still highlighted and click the Send button a SECOND time.

D. Go back to the Main Toolbar and click Receiver, then click Action, then click Save Config.

E. Exit from uCenter

F. Disconnect the TTL from the computer to power off the GPS unit.

G. Reconnect the TTL/GPS unit to verify that your settings have been saved by using the Mini GPS Tool.
