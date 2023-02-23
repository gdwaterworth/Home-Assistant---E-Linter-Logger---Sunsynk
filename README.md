# Home-Assistant---SunSynk-Logger
Home Assistant - SunSynk Logger 


 Hi All...

This is something I have been working on for a while based on my own work with some information gathered from others on this forum and probing what is available.
I have spent the last few days cleaning things up so that they can be easily imported into new environments 
There is a node red flow and a set of templates provided. 
Most plant/inverter information is available as a few main sensors with a lot of attributes on each 
Files etc are available on: Home · gdwaterworth/Home-Assistant---SunSynk-Logger Wiki · GitHub
I have a seperate set of flows for updating the Sunsynk Settings, but will look at making those available when they have been cleaned up.
I have mainly been using those to ensure I always have battery soc available etc with the huge load shedding we have.


The current SunSynk Dongle is currently rebranded from e-linter.com.
http://e-linter.com/smart-energy/magpie 

The quickest way to check would be to try login to https://pv.inteless.com/ and see if you can login to there. It may be you are actually using a rebranded dongle.
If so then this set of flows should get your invertor stats. 

Currently you will need 
1. Node Red for home assistant 
    Additional palette : node-red-contrib-hass
    
Installation : 
a. Add the sensors templates (Templates.txt) into your configuration.yaml

b. Import the Node-Red Flows (SunSynk Gather.json) into Node Red

c. Configure the node-red-contrib-hass addon 

Documentation : 
Documentation for that addon is here : https://flows.nodered.org/node/node-red-contrib-hass

Information of getting a long lived token is here : https://community.home-assistant.io/t/how-to-get-long-lived-access-token/162159

Sample Card To Show Events 
-----------------------------

Errors Seen When Implementing 
-----------------------------
In the debug window there are messages with an error code 401. 

![image](https://user-images.githubusercontent.com/87119523/218646245-75114dea-4fdc-4578-b3d0-dce25908312c.png)

This is an invalid token in the additional palette loaded in node red

Follow the instructions here to get one : https://community.home-assistant.io/t/how-to-get-long-lived-access-token/162159

To apply it open one of these:
![image](https://user-images.githubusercontent.com/87119523/218645683-1021e79e-fbae-4ba9-a634-8d5f1d72dd28.png)

Click on 

![image](https://user-images.githubusercontent.com/87119523/218645778-884a839b-d2d7-4ab3-91d0-f42dfd7d8b11.png)

Put in long life token 

![image](https://user-images.githubusercontent.com/87119523/218645838-62b05bde-f985-4457-a2c5-36afa69aeda8.png)

and deploy

![image](https://user-images.githubusercontent.com/87119523/218646037-307de739-a71c-4872-92a7-c888c021cfe4.png)



