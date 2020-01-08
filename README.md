# maprover--webapp-aws-infrastructure


You can host a static website on Amazon S3. On a static website, individual webpages include static content.
They might also contain client-side scripts. By contrast, a dynamic website relies on server-side 
processing, including server-side scripts such as PHP, JSP, or ASP.NET. Amazon S3 does not support 
server-side scripting. AWS also has resources for hosting dynamic websites.

The goal of the project is to automate static website s3 bucket creation and configuration. 
There are two cloud formation scripts files:
  - s3-staticweb.yaml - script creates s3 bucket only
  - s3-staticweb-r53.yaml - script creates s3 bucket and configures route53


## Deployment

1. Checkout the project from repository
2. Login to the AWS Console
3. Navigate to the CloudFormation
4. Click Create stack in top right corner
  - select "With new resources (standard)
5. In the "Create stack":
  - keep "Templeate is ready" default selection in Prerequisite section
  - Select "Upload a template file" in "Specify template" section
  - Choose the one of the templates: 
    - s3-staticweb.yaml
    - s3-staticweb-r53.yaml
6. Click "Next"

### For the s3-staticweb-r53.yaml selection

7. In the "Specify stack details"
  - Name the stack 
  - Provide full domain name as it is registered in the route53
8. Click "Next"
9. In the "Configure stack options" keep everything default
10. Click "Next"
11. Review all options and select "Create stack"
12. You will see CREATE_IN_PROGRESS status 
