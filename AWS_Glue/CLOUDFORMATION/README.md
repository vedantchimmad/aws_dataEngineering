# Cloud formation

---
Infrastructure as a code
* No manual deployment 
* Create and manage collection of aws resources using template in JSON or YML template
* Template should be reusable
* Cloud Formation creates stack based on the template which is the collection of resource and can be deleted or updated 
* Code your infrastructure either YAML or JSON format 
* Upload your template in S3
* CI/CD process will start creating the stack or you can create the using AWS CLI

### Benefits
* Infrastructure as a code
  * No resources are manually created,Which is excellent for control
  * The code can be version controlled using git
  * Changes to the infrastructure are reviewed through code
* cost
  * Each resource within the stack is tagged with an identifier you can easily see how much a stack costs you
  * You can estimate the costs of your resources using the cloud formation templates 
  * Saving strategy, In dev you could automate deletion of templates at 5PM and recreated at 8AM safely 
* Productivity 
  * Ability to destroy and re-create an infrastructure on the cloud ont the fly
  * Automated generation of Diagram for your templates
  * Declarative programming(No need to figure out ordering and orchestration)
* Separation of concern: Create many stacks for many apps,and many layers,
  
  Ex : VPC stack,Network stacks,App stacks
* Don't reinvest the wheel
  * Leverage existing templates on the web
  * Leverage the documentation

### How cloudFormation works
* Templates must be uploaded in S3 and then referenced in cloudformation
* To update template, we can't edit previous ones.we have to re-uplod new version of the template to AWS
* Stacks are identified by name 
* Deleting a stack deletes every single artifact that was created by the CloudFormation
### Understanding the CloudFormation template options
* Tags : Add tags to appear in S3
* Permissions : use role to create and modify and delete resource stack
* Notification options : Add SNS topic and subscribe to get alert based on delete and update 
* Timeout : Wait creating next stack
* Rollback on failure : Rollback all the resource created after failure 
* Rollback configuration(Monitering time and CloudWatch Alarm)
* Stack Policy
* Termination protection : Protect accidental deletion 
* Quick-Start Link
>[!NOTE]
> 
> Application composer service will help you to create aws infrastructure using graphical interface

### CloudFormation building blocks
* AWSTemplateFormatVersion : Identifies the capability of the template 
* Description : Comments about the template 
* Transform : specifies one or more Macros that used to process the template
* Metadata : AWS resource declared in the template 
* Parameters : The dynamic inputs for template 
* Mappings : The static variable for template 
* Outputs : References to what has been created 
* Conditionals : List of conditions to perform resource creation 
* Rules : Validate a parameter during stack creation/update
* 