# Write-up Template

### Analyze, choose, and justify the appropriate resource option for deploying the app.

<table>
  <tr>
    <th>citeria</th>
    <th>Virtual Machine</th>
    <th>App Service</th>
    
  </tr>
  <tr>
    <td>cost</td>
    <td>Higher Costs at the beginning - including hidden costs for maintenance of the OS</td>
    <td>Lower Costs at the beginning - usage driven costs</td>
  </tr>
  <tr>
    <td>scalability</td>
    <td>Access possible to server configuration - Higher resposibility for configuration</td>
    <td>Not possible to get access to server configurations to analyze performance issues - no multideployments - vertical scaling</td>
  </tr>
  <tr>
    <td>availability</td>
    <td>Much availability,  downtime for patching should be taken into account if multiple are not loadbalanced</td>
    <td>less availability, no downtime for patching</td>
  </tr>
   <tr>
    <td>workflow</td>
    <td>requires more maintainace and efforts to integrate in development workflow</td>
    <td>easy integrated in ci/cd of git and requires less maintaince</td>
  </tr>
</table>

The app service has a lower cost compared to the virtual machine and it requires much less managerial efforts in comparison to vms. 
I used the app service because of its lightweight and low cost.

### Detail how the app and any other needs would have to change for you to change your decision in the last section.

- If there is a need to run a specific operating system or runtime stack that is not supported by App Service. Also if the application would include processing that requires heavy compute resources and than using a virtual machine for this, I would consider other services like Azure Functions or Azure Batch to spin up on-demand.
