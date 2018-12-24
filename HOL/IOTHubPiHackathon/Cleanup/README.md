# Cleanup and Rollback

At the end of the Hands on Labs, you should clean up your Azure account so that the resources provisioned do not continue to consume funds from your account. There are two options that we suggest you follow:

### Option 1 - Delete the Solution Accelerator Completely

If you did not create a solution accelerator skip this step.

1. Remove any functions you created. <br>
    - Click on "Function Apps" in the Azure portal  https://ms.portal.azure.com/
    - Click on the function that you created
    - Click on "Manage"
    - Click on the "Delete" button

1. Delete the Remote Monitoring Solution Accelerator completely if you are not planning to continue to work on the labs in your own time. <br />
  - Best way to remove all the resources is through the www.azureiotsuite.com microsite
    - Navigate to www.azureiotsuite.com
    - Click the tile for your solution accelerator: 
    
      <p align="center">
         <img src="/HOL/IOTHubPiHackathon/images/SolutionReady.jpg" width="50%" height="50%"/> 
      </p> 
    - Once the blade that appears, click the "Delete solution" button
    
      <p align="center">
         <img src="/HOL/IOTHubPiHackathon/images/DeletePCS.jpg" width="40%" height="40%"/> 
      </p> 
      
### Option 2 - Delete the Resource Group

If you did not create the free IoT Hub skip this step.

1. Open the [Azure Portal](https://portal.azure.com/).
1. Select your resource group from the "Resource groups" blade.
1. Select your resource group.
1. Select "Delete resource group"
1. Enter the name of the resource group.  <b>Be sure not to delete any resource groups you did not create!</b>
1. Click "Delete".

<!--
### Option 3 - Reduce the size of the running Azure services
If you plan on using the PCS after this lab, you can leave it running but it's recommended that you reduce the size/scale of some of the resources so that the services consume less from your subscription. 

1. Change the App Service plans from S1 - Standard to B1 – Basic. Note that you cannot go down to the F1 - Free tier as we need the custom domain feature that is available with the B1 tier. Note that there’s two app services to scale down. 
   - Click on the app service plans that were provisioned as part of the solution accelerator
   - Under Settings -> Scale Up (App Service Plan), select the B1 - Basic plan and click "Select"
   - Do the same for the *-jobhost* service plan
     <p align="center">
         <img src="/HOL/IOTHubPiHackathon/images/reduceAppService.jpg" width="90%" height="90%"/> 
      </p>   
      
2. Pause the simulated devices. The simulated devices run in a web job. To completely halt generation of new data when not in use, you can stop the web job in which the simulated devices are running.
  - From within the jobhost service plan, select Settings -> Webjobs. 
  - Right-click the "DeviceSimulator-Webjob" webjob. Click "Stop". 

      <p align="center">
         <img src="/HOL/IOTHubPiHackathon/images/pauseSimulatedDevices.jpg" width="90%" height="90%"/> 
      </p> 
-->

