# infra-deployment-challenge-udacity
This is my solution to the challenges on Udacity Nano Degree Program

This is for the module titled Deploy Infrastructure as Code (IAS)

To deploy or update a stack, run the create.sh or update.sh script

The stacks are configured to deploy infrastructures in us-west-2 region. To change the region to deploy these
infrastructure, set the --region flag in  the create.sh and update.sh file to the region of your choice.

The create.sh and update.sh files are to be run in your AWS CLI and require three parameters each to run. 
First parameter is your chosen stack-name. Second parameter is the location of the template-body file. Third parameter is 
the location of the parameters file. For example, to deploy a network stack, in your AWS CLI, run the command;
create.sh networkStack networkDeploy.yml networkDeploy-params.json
 
Note:
The networkDeploy.yml file is the main file, containing the stack definition code.
The networkDeploy-params.json file is the main file, containing the parameters for the networkDeploy.yml file

To delete a stack, in your AWS CLI, run the command; 
AWS cloudformation delete-stack --stack-name <stack-name> --region=<AWS region where stack is deployed>
