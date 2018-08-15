# Web Device Manager API
### Working draft, 14th of August 2018

## 1. Admission
The Web Device Manager API is allowing the user to expose their devices included in the configuration of the machine in use.
The entire operation of exposing is not going to be invoked without acceptance of the user who is the owner of the local machine in use.

The following API is going to request the user to grant a permission to read the machine's configuration and list of devices and their included setting and properties. If the user didn't grant the permissions for the web browser to read the list of devices included in the configuration of the local machine, the API will throw specific error informing the user that the operation will not be performed without acceptance to access the devices list.

## 2. Usage
<b>2.1</b>. The user would be able to access the website where they can verify the list of available devices on the local machine and check the status of their drivers. If one of the drivers is not up-to-date, then the website based on APIs properties related to the device is going to offer you a possibility to update to the latest version of the driver. 

<b>What is the current issue with the above statement?</b>
<p>The problem appears often, reportedly it is malware which infects local machines of users because of fake installers or fake websites which hunt users and tells them to click on the button to verify their hardware and download latest drivers which are not the case obviously.</p>

<b>How can we prevent above behaviour from spinning?</b>
<p>The following API, if implemented, will be marking the website that uses it as a trusted source of drivers update, which will not appear on the projects that mean to infects you by malware. You will not be able to implement the API if your project doesn't use HTTPS connection.</p>

<b>2.2</b>. A developers who is going to create a project by using the mentioned Web API will be able to create applications with following purposes:
<ul>
  <li>1. Analyze data</li>
  <li>2. Test games' requirements</li>
  <li>3. Detect outdated drivers on users' machines.</li>
  <li>4. Gaming industry - Developers will be able to match performant game configuration based on the user's hardware</li>
  <li>5. E-commerce usage - create related products sliders that provides more accurate offer based on the user's hardware configuration</li>
  <li>6. Marketing usage - Ads based on current user's machine configuration</li>
  <li>7. Detection of hardware to support World community grid organization</li>
</ul>

## 3. Caution
<p>Even if the browser marks the website as a trustfull source to update the out-dated drivers, it doesn't exclude the user from having antivirus software installed on the local machine. The website even if marked as trustful one, can offer a malware content. The trusful mark doesn't give you a guarantee that the web page doesn't contain malware.</p>


## 4. Syntax
``` JavaScript

const deviceManager = new DeviceManager({
    detailed: false,
    configuration: true
})
.then(response => response.json())
.then(data => data)
.catch(error => error);

```
<p>The API is going to provide a constructor called <b>DeviceManager</b> that is going to take a one parameter which is an object containing two properties, listed below.</p>
<ul>
  <li><b>detailed</b></li>
  <li><b>configuration</b></li>
</ul>

<p>A both properties mentioned above are type of boolean.</p>
<p><b>4.1</b>. detailed property</p>
<p>A detailed property helps the developer to specify and perform filtering in order to bring a significant number of devices needed to run the machine. In the really simple example, if we set the property to <i>true</i> we're going to receive a full list of available user's devices. If we set the property to <i>false</i>, we're going to receive a list of significant parts of the machine needed to run the processes</p>

<p><b>4.2</b>. configuration property</p>
<p>A configuration property is having a lot to offer for developers. The property allows to bring all of the available settings and properties of the devices available on the user's machine. If we set the property to <i>true</i>, we're going to receive a full list of settings for a specific device as a nested object. If we set the property to <i>false</i>, we're going to receive a fundamental list of settings for a specific device as a nested object.</p>

<p>The response returned by API is going to be handled by promises.</p>

## 5. Response
