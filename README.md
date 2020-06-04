# Udagram

## Description
This project deploys a high-availability web app using CloudFormation. It is 
part of the course Deploy Infrastructure as Code (IAC), which belongs to 
the Cloud DevOps Engineer Nanodegree Program from Udacity.

## Setup

### Network Infrastructure
This script creates a VPC, two public and two private subnets, along 
with the Internet and NAT gateways: 
```
./create.sh UdagramNetwork udagram-net.yml udagram-net-params.json
```

### Bastion Hosts
This script creates two bastion hosts that allow SSH access into
the private subnet servers:
```
./create.sh BastionHost bastion-host.yml bastion-host-params.json 
```

### Web App Servers
This script deploys the web app across four web servers in two Availability Zones, 
an Autoscaling group, and a Load Balancer:
```
./create.sh UdagramWebApp udagram-app.yml udagram-app-params.json 
```
