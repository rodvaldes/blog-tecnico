#Weblogic Document#

##Overview#

Deployment en linea de commandos

```
cyberlaptop:DeploymentPlanSample rvaldes$ java -cp ../fmw_12.2.1.2.0_wls_quick_Disk1_1of1/wls12212/wlserver/server/lib/weblogic.jar  weblogic.Deployer -adminurl t3://localhost:7001 -user weblogic -password 453r21v2 -redeploy -name PlanExampleApp -source PlanExampleApp.ear
weblogic.Deployer invoked with options:  -adminurl t3://localhost:7001 -user weblogic -redeploy -name PlanExampleApp -source PlanExampleApp.ear
<27-02-2017 00:50:27 Hora de Chile> <Info> <J2EE Deployment SPI> <BEA-260121> <Initiating redeploy operation for application, PlanExampleApp [archive: /Users/rvaldes/Downloads/DeploymentPlanSample/PlanExampleApp.ear], to configured targets.>
Task 5 initiated: [Deployer:149026]deploy application PlanExampleApp on AdminServer.
Task 5 completed: [Deployer:149026]deploy application PlanExampleApp on AdminServer.
Target state: redeploy completed on Server AdminServer
cyberlaptop:DeploymentPlanSample rvaldes$
```
