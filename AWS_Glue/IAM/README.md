# IAM

---
Identity and access management 
* Regulates access to AWS resources
* ### Two key concepts
  * **Authentication** : Providing the identify for who is performing the action
     
    Ex : Users, User group and Roles
  * **Authorization** : Granting specific actions such as read,write,put etc
    * IAM policies are used for authorization
     ```json
      {
        "Version": "2012-10-17",
        "Statement":[
           {
            "Effect": "Allow",
            "Action": "s3:*",
            "Resource": "arn:aws:iam::234567123456:role/GlueJobRole"
           }
          ]
      }
     ```
### Policies creation and management
* AWS managed policies : AWS created polices  
  * Manged policies : AWS created policies and managed by them over a time
* Costumer managed policies : Costumer created polices
  * Inline policies:Can be attached to particular identity
  * Manged policies:Can be attached to multiple identities

#### Policy types
* Identity based policies : Can be attached to identity to grant permissions and identities are users,groups and roles
* Resource based policies : Can be attached to resources such as S3,KMS,DynamoDB etc