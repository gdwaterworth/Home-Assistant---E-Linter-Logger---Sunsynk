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
