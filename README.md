# AWS CloudFormation Templates
My Personal AWS CloudFormation Template samples for when I need to quickly configure an environment.

### vpc-2az-2pubnet-2privnet-2ngate.json
+ 1 private VPC
+ 1 Internet Gateway
+ 2 Public Subnets
+ 2 Private Subnets
+ 2 NAT Gateways
+ RouteTables from PrivateSubnet(s) to PublicSubnets(s)

### bastionhost_adhoc.json
+ Launches an adhoc Linux AMI Bastion hosts into a Public subnet of a VPC
+ Only SSH access is allowed
+ Bastion hosts have a runtime configurable Time To Live duration, after which they will be auto killed.  *Note:* Maximum TTL of 3 days is allowed.
+ Bastion hosts launched via AutoScaling group so as many can be launched as required
