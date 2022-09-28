# EC601Product-Design
*IOT Based Smart Home Automation System*

## Problem Statement/Application
An IoT involves extending Internet connectivity beyond standard devices, such as desktops, laptops, smart phones which is Embedded with technology, these devices make communication over the Internet, and user can be remotely monitored and controlled. Existing smart home automation systems are uniquely designed to suit specific consumers home environments and requirements [1]. These systems are complex in design, not flexible enough to meet the custom requirements, and are often embedded into the physical structures of the home.
In existing smart home automation systems, safety and security is an important consideration for the consumer and end users. Repeatedly, studies have revealed that devices designed to automate the home have serious vulnerabilities. Many devices have weak password policies and do not protect against man-in-the-middle attacks, according to an HP survey of 10 off-the-shelf home security systems [2]. Others do not prevent access to the device’s debugging interface, which could allow easy hacking of the device, according to an April study by code-security firm Veracode. And, if an attacker is able to gain access to the device, almost all devices could be easily compromised and turned into a Trojan Horse, according to a study by security firm Synack [2]. In fact, it only took between 5 and 20 minutes to find a way to compromise each device once the researchers unpacked the hardware.

 



## Existing Methodologies
A.	low-cost Wi-Fi based automation system: Arduino Mega microcontroller along with WI-FI module ESP8266 in HAS is specially used for controlling the home appliances. A local control system over Wi-Fi and a remote control is established based on IoT. A suitable Wi-Fi-based android application which is Virtuoso is utilized because it has a user-friendly interface and it can work efficiently with Arduino Mega to control and monitor via smart phone [3]. The Wi-Fi module, buzzer, temperature and humidity sensor is connected directly to Arduino Mega microcontroller. The relay board receive its input signals from Arduino Mega, while the bulbs and fan which are only samples for real home appliances are connected to the relay outputs.
B.	By symmetric encryption scheme: The proposed architecture of the SHS consists of four groups of entities: 
1) appliance group 
2) monitor group 
3) central controller 
4) user interfaces Appliance group contains the home appliances including TV set, stove, oven, thermostat, etc. Each member of the group has individual ID so that it can be uniquely identified by the central controller. The entities in appliance group can perform particular operations, such as switching on/off, turning up/down, reporting status, etc. Monitor group is formed by sensors and detectors, such as smoke sensor, motion sensor, electricity meter, and home security monitoring sensor. The sensors always sends the data and periodically send the data to the central controller.

C.	Home automation using set of sensors: The TI CC3200 Launchpad consists of Applications Microcontroller, Wi-Fi Network Processor, and Power-Management subsystems. It performs with the ARM Cortex M4 Core Processor at 80 MHz. It has embedded memory including RAM (256 KB). The dedicated ARM micro-controller also has a network processing subsystem in it [4].

D.	Ethernet based system: The Ethernet based system connected to the app is android based which is connected to the internet through either Wi-Fi or mobile data. It is make connection to the Intel Galileo based server over the internet and lets the users to monitor with the help of an internal mobile timer and toggles the switching by tap-to-touch or voice using Google API speech recognition tool.

## Conclusion
In Conclusion, home automation systems involve making homes even smarter. Homes can be interfaced with sensors including motion sensors, light sensors and temperature sensors and provide automated toggling of devices based on conditions. Internet of things-based home automation system can only work in the presence of internet. The rapid growth of IoT devices brings concerns and benefits. Even though Wi-Fi is not available we can go to 3G or 4G services. This is one big advantage of IOT In this project, the use of a camera connected to the microcontroller might help the user in taking decision whether to welcome the guest after receiving the captured picture of the guest or intruder, If the user identifies he is an unknown person then the user can further forward the same photograph to the police station by explaining his situation.




## References

[1] 	M. H. N. S. A. a. S. K. M. Waheb A. Jabbar, "“Design and Implementation of," 19 June 2018.

[2] 	R. L. B. M. J. Y. X. X. a. X. C. Tianyi Song, "A Privacy Preserving Communication Protocol for IoT Applications in Smart Homes," IEEE, Vols. VOL. 4, NO. 6, 23 May 2017. 

[3] 	V. J. S. B. a. L. B. Ravi Kishore Kodali, "IoT Based Smart Security and Home Automation," 29 April 2016. 

[4] 	J. P. Gupta, "IoT based Smart Home Design using Power and Security Management," 3 February 2016. 



