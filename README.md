# Web Device Manager API

## 1. Admission
The Web Device Manager API is allowing the user to expose their devices included in the configuration of the machine in use.
The entire operation of exposing is not going to be invoked without acceptance of the user who is the owner of the local machine in use.

The following API is going to request the user to grant a permission to read the machine's configuration and list of devices and their included setting and properties. If the user didn't grant the permissions for the web browser to read the list of devices included in the configuration of the local machine, the API will throw specific error informing the user that the operation will not be performed without acceptance to access the devices list.

## 2. Usage
