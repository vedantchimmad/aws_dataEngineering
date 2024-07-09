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

