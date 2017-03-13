SmartThings SmartApp Energy Logger for PlotWatt
=======
<br>
<b>NOTE: Plotwatt will no longer accept API calls from generic meters as of March,
2017, so this is sort of pointless now :(</b>

SmartThings SmartApp to send energy meter data (watts) to
PlotWatt. Testing with HEMv1 but will likely work with any
device that supports EnergyMeter capabilities with SmartThings.

Requirements
------------
- SmartThings HUB
- Device that supports the "EnergyMeter" capability (tested with HEMv1)
- [PlotWatt](http://www.plotwatt.com) account - Free

Installation
--------------------
1. Create a PlotWatt account, create a new house and for your energy meter type
select <b>PlottWatt API</b>
2. Navigate here: https://plotwatt.com/docs/api and retrieve your API ID. 
3. Next you'll need to create a meter using the API. If you have more than 1
meter, you'll adjust this number.  Use a UNIX or Mac system with curl:
<pre>$ curl -X POST -d "number_of_new_meters=1" http://YOURAPIID:@plotwatt.com/api/v2/new_meters</pre>
4. This command, if successful, will return your new meter ID(s). Make note of this for your
installation of the SmartApp.
5. Now, add a [SmartApp](https://graph.api.smartthings.com/ide/apps) and do
from Source Code and copy the RAW data from Github.
6. Save and publish the app. 
7. Go to your phone, +, add Smart App and add the API ID and Meter ID.
8. If you have multiple devices, you'll need to duplicate this again and name
it something different. 

Bugs/Contact Info
-----------------
Bug me on Twitter at [@brianwilson](http://twitter.com/brianwilson) or email me [here](http://cronological.com/comment.php?ref=bubba).


