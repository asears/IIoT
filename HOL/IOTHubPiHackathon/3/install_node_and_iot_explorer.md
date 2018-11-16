# Installing node

*Note* iothub-explorer will be retired on November 31st, 2018 and has been replaced by the Azure CLI IoT Extension: https://aka.ms/iotcli

Python v3.5 or higher is required for Azure CLI IoT Extension.

Deprecated NPM modules:  
azure-event-hubs@0.0.8: < 0.2.12  
crypto@0.0.3: Built in module replacement warning.  
[SECURITY] lodash vulnerability recommends upgrading npm, running npm audit"

We will leverage an open source application called "Node Version Manager" (NVM), which will allow you to install various versions of Node in differnt OS environments and be able to switch between Node versions.

1. Install node in your environment
  - go to https://github.com/creationix/nvm#installation and run the install script:  
  ```curl -o- https://raw.githubusercontent.com/creationix/nvm/v0.33.8/install.sh | bash```  
  - You may need to refresh your .bashrc file environment.  From a bash prompt, execute the following:  
    ```source ~/.bashrc```

2. Now you can install a specific version of Node at anytime.  At the time of writing this document, 8.11.1 is the latest stable Long Term Support (LTS) release. For example, to install Node 8.11.1 run the following command:  
```nvm install 8.11.1```  
  - This will install Node 8.11.1
  - If this is your first time running ```nvm install``` it will make ```8.11.1``` your default Node version  
  ```npm``` is automatically installed along with your desired version of ```node```

3. Now you can install ```iothub-explorer``` globally for your OS  
```npm install -g iothub-explorer```
  
You can now continue [Lab 3](README.md) and use iothub-explorer to view our incoming telemetry and send messages to our device via the IoT Hub.


