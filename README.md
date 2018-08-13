# Web Device Manager API

## 1. Admission
The Web Device Manager API is allowing the user to expose their devices included in the configuration of the machine in use.
The entire operation of exposing is not going to be invoked without acceptance of the user who is the owner of the local machine in use.

The following API is going to request the user to grant a permission to read the machine's configuration and list of devices and their included setting and properties. If the user didn't grant the permissions for the web browser to read the list of devices included in the configuration of the local machine, the API will throw specific error informing the user that the operation will not be performed without acceptance to access the devices list.

## 2. Usage
<b>2.1</b>. The user would be able to access the website where they can verify the list of available devices on the local machine and check the status of their drivers. If one of drivers is not up-to date, then the website based on APIs properties related to the device is going to offer you possibility to update to the latest version of the driver. 

<b>What is the current issue with the above statement?</b>
The problem appears often, reportedly it is malware which infects local machines of users because of fake installers or fake websites which hunt users and tells them to click on the button to verify their hardware and download latest drivers which is not the case obviously.

<b>How can we prevent above behaviour from spinning?</b>
The following API if implemented will be marking the website that uses it as a trusted source of drivers update, which will not appear on the projects that mean to infects you by malware. You will not be able to implement the API if your project doesn't use HTTPS connection.

<b>2.2</b>. 
