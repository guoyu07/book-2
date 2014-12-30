# Import CloudFormation template (Preview)

You can import CloudFormation templates into the IDE to visualize.

![](https://raw.githubusercontent.com/MadeiraCloud/docs-image/master/ide_stack_import_cfn.png)

## Prerequisite

The current release has some prerequisite so that CloudFormation templates can be imported:
- the template must not include any reference to an existing VPC, Subnet or Security Group
- These components must be defined as completely new resources

To meet these requirements, you can edit your template as follows:

## Example
Here is the example in AWS, it's named Template_1_SharePoint_2013.template.

![](https://raw.githubusercontent.com/MadeiraCloud/docs-image/master/ide_stack_import_cfn_sharepoint.png)


As the templete exists already, the VPC and subnets are defined in the ‘Parameters’ section which causes them to reference to the existing VPC and subnets. To allow the template to be imported to VisualOps IDE you need to move this to the ‘Resources’ section and convert it into a new resource like so:

![](https://raw.githubusercontent.com/MadeiraCloud/docs-image/master/ide_stack_import_cfn_sharepoint2.png)

