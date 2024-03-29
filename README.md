# MCRP
## What is it?
We are proposing a completely automated vehicle tracking system which has the capability to trace a vehicle by its license plate using the surveillance and security cam feeds used by the police. We are also planning to create a platform for the public to register vehicle missing cases, theft, abductions or any kind of issues that involves a vehicle. Once a case is registered, an incident is generated by the platform which will be notified to the core surveillance system that can trace the vehicle mentioned in the same and then will generate a report for the respective authorities which could be followed by appropriate actions, thus easing and reducing the overall effort in such scenarios.

## System Architecture
![](https://github.com/HacKP-CyberDome/coderscafe-web/blob/master/core/surveillance-centre/openalpr/src/Architecture.jpg)

The system consists of 2 parts,

**1. The Core**

Suppose there are 'n' control centres or surveillance centres working in the state. We will provide a stand-alone software (based on ALPR AI) which have the potential to monitor the live cam feeds streamed to the centre (this is restricted to some potential limitations of computational power and resource requirements) which continuously recognises all the license plate numbers passing through the cam feed. The license plate numbers recognised by the software and is connected  to a centralized server. Let's call this system as the core.

**2. The Interface**

The user interface (preferably a website or a mobile application) is a place where both public and police interact with the centralized server. Public can register the cases related to vehicles and the police can keep track of the cases through this interface.

## Working
A user can register a case [here](http://coderscafe.hackp.cyberdome.org.in/) with all relevant details.

Once a case is registered through the user platform, the relevant details like license plate number is passed to the core. The core then initiates a search through the logged data and checks if it has any trace of the vehicle appearing in the case. If found, it will generate a report with location and time details. 

The assigned police officer can access the report [here](http://coderscafe.hackp.cyberdome.org.in/admin/login) ( using default credentials ```firstsuperadmin:password``` ) which could be followed by appropriate actions. The process continues every hour and the report is frequently updated until the case is closed.

## Advantages

1. Since the complaint is registered online there is no possibility of a delay between registration of the complaint and the commencement of the investigation.
2. Since all the number plates are logged, it is easy to handle multiple cases using the same software.
3. If police has a software to recognize number plates, the current solution is easily integrable.

## Demo

View the video demo [here](https://www.youtube.com/watch?v=2gXH-qaUrF8)
