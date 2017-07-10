# ami-lookup

## Example Usage

Resource in CloudFormation. All Properties except for ServiceToken are optional:

```
AMILookup:
  Type: "Custom::AMILookup"
  Properties:
    ServiceToken: !ImportValue "ami-lookup-stack::AMILookupFunctionArn"
    Filters: # Filters match those in the AWS SDK for ec2:DescribeImages
      name: foobar-*
    Owners:
      - 000000000000
    ExecutableUsers:
      - 000000000000
    Region: !Ref AWS::Region
```
