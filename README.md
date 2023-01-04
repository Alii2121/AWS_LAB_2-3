# AWS_LAB_2-3

# LAB 2
## Creating EC2 instance inside a public subnet and connect it to Internet Gateway and then Create an EC2 in a private subnet and connect it with NAT and install Httpd without SSH.


### Creating a VPC
![Screenshot from 2023-01-04 19-00-32](https://user-images.githubusercontent.com/103090890/210628769-566b3feb-42c6-49e1-8517-b5463618c746.jpg)


### Creating 2 Subnets Private,Public
 
![Screenshot from 2023-01-04 19-01-37](https://user-images.githubusercontent.com/103090890/210628861-5beb43b4-2eb1-4434-9399-3f92f4286d0f.jpg)





![Screenshot from 2023-01-04 19-07-13](https://user-images.githubusercontent.com/103090890/210628874-fb52a0fb-2bbc-4cc4-81c0-41b94514454b.png)


### EC2 in Public Subnet


![Screenshot from 2023-01-04 19-11-53](https://user-images.githubusercontent.com/103090890/210628898-0f8b9cb6-d978-4de5-a318-de33e72891f8.png)


### NAT gateway

![Screenshot from 2023-01-04 19-13-03](https://user-images.githubusercontent.com/103090890/210628902-b6c0da68-256d-44b2-8769-8a6ca4405b66.png)


### Route Table from private subnet to NAT
![Screenshot from 2023-01-04 19-19-41](https://user-images.githubusercontent.com/103090890/210628907-5045deff-5f4d-490c-b2b1-df8ef8722a36.png)

### Internet Gateway


![Screenshot from 2023-01-04 19-25-44](https://user-images.githubusercontent.com/103090890/210630149-cb02c802-d9c6-40fc-a39a-d980d8b5af8f.png)



### Httpd installed on EC2 in Private using user data =
```bash
#!/bin/bash
yum update -y
yum install -y httpd.x86_64
systemctl start httpd.service
systemctl enable httpd.service
```
![Screenshot from 2023-01-04 20-14-52](https://user-images.githubusercontent.com/103090890/210631519-1d5e01a8-bb29-4d5c-87e0-4276a92a6811.png)



### NAT Gateway Details

![Screenshot from 2023-01-04 20-16-43](https://user-images.githubusercontent.com/103090890/210631545-4a4c6716-6328-438f-ae62-87fb6dc09daa.png)


### Public EC2 Details

![Screenshot from 2023-01-04 19-11-53](https://user-images.githubusercontent.com/103090890/210630891-5c39a078-5137-4889-9702-4a8d6895a0aa.png)

### Routing Public Subnet with Internet Gateway

![Screenshot from 2023-01-04 19-25-44](https://user-images.githubusercontent.com/103090890/210631023-9dd5eb24-2c89-47bb-bfeb-18b68cc5585f.png)


![Screenshot from 2023-01-04 20-17-28](https://user-images.githubusercontent.com/103090890/210631094-30c18b2f-93ab-4c00-92ba-2b1274585e11.png)

### Private Subnet Routing

![Screenshot from 2023-01-04 20-17-12](https://user-images.githubusercontent.com/103090890/210631164-f75e9138-0d73-4b53-bacd-8e262c3f60c6.png)

# LAB 3

### Creating 2 Subnets Private and Public

![Screenshot from 2023-01-04 21-49-14](https://user-images.githubusercontent.com/103090890/210637302-6b7c28c3-ff84-4c74-b6da-f97add83bd0b.png)
![Screenshot from 2023-01-04 21-49-21](https://user-images.githubusercontent.com/103090890/210637316-5727025e-7e9a-47e2-9239-3e49399cfb4b.png)

### Creating 2 NACL 
![Screenshot from 2023-01-04 21-45-49](https://user-images.githubusercontent.com/103090890/210637471-d8e9c918-f05f-4e32-a6c2-7039acd070bf.png)



![Screenshot from 2023-01-04 21-45-49](https://user-images.githubusercontent.com/103090890/210637506-93782aa7-567f-46cb-9854-ff97cc20567b.png)

### Creating 2 EC2 one as A jump host 
![Screenshot from 2023-01-04 21-45-05](https://user-images.githubusercontent.com/103090890/210637678-509c49a4-5195-40c2-8bba-f0985dc64ca6.png)
![Screenshot from 2023-01-04 21-45-09](https://user-images.githubusercontent.com/103090890/210637688-4f58fbcd-b1e5-4096-8177-44f1f46e7337.png)

### Creating Security Groups![Screenshot from 2023-01-04 21-46-27](https://user-images.githubusercontent.com/103090890/210637751-66ebef54-547b-46e1-af72-3fcf41889003.png)

![Screenshot from 2023-01-04 21-46-13](https://user-images.githubusercontent.com/103090890/210637744-80a4c61e-953d-4c5b-b581-2c76f3174c6f.png)

![Screenshot from 2023-01-04 21-30-09](https://user-images.githubusercontent.com/103090890/210637785-16b64c14-4ede-47c7-9731-1ede520754bb.png)


![Screenshot from 2023-01-04 21-29-18](https://user-images.githubusercontent.com/103090890/210637772-3d6946d1-cf04-491b-9887-dbbbbcf51e30.png)


## Then SSH into the Jump Host with the key then use the Jump host to SSH to another


# Thank You !
