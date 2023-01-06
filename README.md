# Deploy a high-availability web app using CloudFormation
This projects requires a CloudFormation script to deploy a dummy application. The script first deploys the network infrastructure required to run the application. I used a  Launch Configuration to deploy four webservers, 2 located in each of the private subnets. The launch configuration is used by an autoscaling group.

## Script Deployment
I created three bash scripts to easily deploy my script:
* ./create.sh - to create the cloudformation stack
* ./update.sh - to update the stack
* ./delete.sh - to delete the stack

```
./create.sh <stack-name> <template-body>.yml <parameters>.json
```
Example:
```
./create.sh demo-app1 network-infra.yml server-parameters.json
```
(LoadBalancer URL) - [http://demo-webap-13ytvtdlalo2x-1580369252.us-east-1.elb.amazonaws.com/]