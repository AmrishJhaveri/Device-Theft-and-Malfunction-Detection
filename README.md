# Device-Theft-and-Malfunction-Detection

<img src="flow.png" height="500"></img>

## What it does?

Implemented IoT  devices which prevents damage or theft of sensitive information. We integrated the temperature and the light sensor with IoT device. This will help prevent theft by checking light exposure if it's within the original limits it means the objects are at their own place. The system also prevents damage of the object by sensing the temperature and determining whether the object has caught fire or exposed to heat this is done by emission of temperature sensor on the device.

## How we built it 
We used the Dragonbooard 410c as an IoT device to run a python application for collecting location data. This python application makes a REST API call to the monitoring app.

Arduino101 was used as a IoT. Arduino collects data from light and temperature sensors and makes a REST API call to monitoring app.

The monitoring app is designed in Node.js with an Express server running to receive the REST API calls. The UI was built using HTML, Bootstrap and jQuery to show real time data of the sensors recieved from various devices.

## Challenges we ran into 
Arduino 101 was very old so the commands we could use and interface were limited.
The Dragon devices had network issues as they were in PEAP encrypted wifi.As these were IoT devices dragonboard went to power saving mode and henc not reachable.

## Accomplishments that we are proud of 
Coming up with the Hackathon for Security using the new technolgies like Dragonboard, Kubernetes, Docker, Spark(Big Data)


For Quick  Demo -

https://www.youtube.com/watch?v=3Jg3FfQGt1s&feature=youtu.be


## Steps to run the Malfunction and device theft application:

1.) Set up the Dragonboard 49c using linux os. Once done with this store the python script dragonboard.py present inside the Client folder into the Dragonboard memory. 

2.) Once you run the python script on the dragonboard the location of the dragonboard gets transmitted using a python post request on to the node js backend which is displayed over the front end application which can be found inside the MonitoringApp folder.

3.) Now setup the light sensing and temperature sensing in Arduino 101 using the code present inside the Client folder under Lightsensor.ino. This sends an alarm to the Monitoring app above and starts beeping in case of excessive light sensitivity then what is supposed to be there or excessive temperature change.
