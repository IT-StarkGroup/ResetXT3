# RESET XT3
Stark Reset for Jenbacher Dia.ne XT3 engine controller.

## About
The Stark RESET application allows for remote monitoring of and interacting with the Jenbacher DIA.NE XT3 gas engine controller.
The extended version of the application also allows to remotely acknowledge and reset alarm conditions as well as operate the engine (see below).

This application is based on Apace Guacamole™ and licenced under Apache Licence 2.0.  
Version: 1.0 – 2021, Stark Engineering Engineering Consulting Pty Ltd

## Installation
### Installation requirements
To run the application you require a Java runtime environment (JRE), available for Windows, MacOs or Linux. Only Java 1.8 is supported.

### Running the application
Once the JRE is installed, copy the application 'StarkResetXT3.jar' to a folder of choice and run the application from the command prompt with 
> />java –jar StarkResetXT3.jar

### Connecting to Dia.ne XT3 controller
The application needs an Ethernet connection to the Dia.ne XT3 controller. The IP address of the controller should be set under ‘Configuration’ (see below).

The application connects to two VNC servers on the Dia.ne XT3 controller. The VNC ports should be set under ‘Configuration’ (see below).

For troubleshooting we recommend using any VNC viewer software.

### Overriding physical panel selector switches
The RESET application provides the option to visualise and operate/override the selector switches on the Jenbacher XT3 control panel. However, this cannot be achieved by the RESET application alon. For this purpose the app must communicate with a controller that can interact with physical wiring in the control panel. The app communicates with the controller through WebSockets. Please contact our support team for further details. A recommended hardware platform is the Revolution Pi from Kunbus (https://revolutionpi.com/revpi-connect/) 

## Logging in
URL of the login page: http://\<your-ip-address\>/StarkResetXT3
  
The application allows for two levels of log-in:
- Administrator *(Default: admin / password)*
- User *(Default: user / password)*

An administrator can manage users and credentials in the 'Users' menu.

## Configuration
### Plant Identification
- Plant Name: fill out as desired. The name is displayed on the Main screen.
- J-number: this is the engine identifiction number, fill out as desired. The number is displayed on the Main screen.

### VNC Server (B&R)
- IP address: enter the DIA.NE XT3 engine controller IP address. *(Default: 192.168.123.11)*
- VNC Password: enter the DIA.NE XT3 VNC password. *(Default: RemoteOP)*
- VNC Port 1: enter the DIA.NE XT3 VNC port #1. *(Default: 5900)*
- VNC Port 2: enter the DIA.NE XT3 VNC port #2. *(Default: 5901)*

### RESET – Selector Switches
Disable or enable the functionality of the Service, Demand and Sync Selector Switch.

**Note**  
Implementation of this functionality requires additional software and hardware to be implemented. Please contact our Support team for further information.

## Use of Selector Switches
The use of the selector switches depends on the implementation. Contact our Support team to discuss your options.

A typical implementation allows to acknowledge and reset alarm and fault conditions on the Dia.ne XT3 engine controller as follows:
1.	Ensure the engine is not running
2.	Click the ‘OFF’ button under ‘Service Selection’
3.	Select ‘Reset’ on the Dia.ne XT3 controller

## Support
Please contact our support team:
- http://www.starkgroup.com.au
- enquiries@starkgroup.com.au
