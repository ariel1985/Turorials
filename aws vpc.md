# AWS VPC

## COST OF PROJECT

_Within Free tier limits_

  

## Preapare your VPC

  

### Create VPC

In the menu search for VPC, on left navigation find `your vpc's ** -> create VPC -> Name : Whatever you like -> IP - 10.0.0.0/16 or any other valid CIDR`

  
![VPC console image](https://github.com/Ananyojha/spare-images/raw/main/IMG_20211128_181433.png)
  

- You can also select the region on top right corner in (red block).

- The centre shows every VPC component deployed.

  

### Create Subnets

WE WILL CREATE TOTAL 3 SUBNETS :

Repeat the process below 3 times, each time entering the diffrent IP address given below

In the left pane :` Subnets -> Create Subnets -> Choose The __VPC__ you created before -> subnet name: Whatever you like -> IP Ranges (Refer below) -> availabilty zone : different for each subnet `

IP Ranges :

- 10.0.1.0/24 : Public Subnet

- 10.0.2.0/24 : Private Subnet 1

- 10.0.3.0/24 : Private subnet 2

  

-  __NOTE__ : After creating the Public Subnet, select it -> actions -> edit -> check the box for Auto-assign IP settings.

  
![](https://github.com/Ananyojha/spare-images/raw/main/IMG_20211128_182146.png)
  

### Create Internet Gateway

Left navigation menu -> `Internet Gateway -> create -> Name Tag: Whatever name You Like -> Create Gateway`

__After Creating it, select the Gateway you created -> actions -> attach to VPC -> __The VPC YOU CREATED__

  
![](https://github.com/Ananyojha/spare-images/raw/main/IMG_20211128_181953.png)
  

### Create a Route Table

Left navigation menu -> `Routes -> Name: whatever -> VPC: The VPC YOU CREATED -> add route -> Destination 0.0.0.0/0 -> Target: Internet Gateway -> create`

#### NOTE: after created, select the route -> subnet associations -> associate it to YOUR PUBLIC SUBNET

  
![Route Table Screenshot](https://github.com/Ananyojha/spare-images/raw/main/IMG_20211128_181847.png)