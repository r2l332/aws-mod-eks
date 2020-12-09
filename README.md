## VPC Module

![Unit Tests](https://github.com/r2l332/aws-mod-vpc/workflows/Unit%20Tests/badge.svg)
![Release Creation](https://github.com/r2l332/aws-mod-vpc/workflows/Release%20Creation/badge.svg)

Module to VPC plus 6 subnets; 3 private and 3 public.

* VPC
* 3 Private Subnets
* 3 Public Subnets
* NAT Gateway
* Routes for each subnet and Route Table 

## Providers

| Name | Version |
|------|---------|
| aws | n/a |

## Inputs

| Name | Description | Type | Default | Required |
|------|-------------|------|---------|:-----:|
| data\_subnet\_cidrs | List of data subnets to create | `list(string)` | n/a | yes |
| name | Name of VPC stack - This will also be used in subnet names and other network related components | `string` | n/a | yes |
| priv\_subnet\_cidrs | List of private subnets to create | `list(string)` | n/a | yes |
| pub\_subnet\_cidrs | List of public subnets to create | `list(string)` | n/a | yes |
| region | Where to deploy VPC | `string` | n/a | yes |
| vpc\_cidr | VPC Cidr to create e.g `10.0.0.0/16` | `string` | n/a | yes |

## Outputs

| Name | Description |
|------|-------------|
| data\_subnet | Returns data subnet ids |
| private\_subnet | Returns private subnet ids |
| public\_subnet | Returns public subnet ids |
| route\_table\_ids | Returns route table ids |
| vpc\_id | Returns VPC id |

## Go Test

Make sure Go is installed and GOPATH/GOROOT have been set correctly. 
  
From the root of the module run the following commands...

*`$ go mod tidy` 

*`$ go test ./test -test.timeout 0 -v`
