# AWS_LAB_2-3

# LAB 2
## Creating EC2 instance inside a public subnet and connect it to Internet Gateway and then Create an EC2 in a private subnet and connect it with NAT and install Nginx without SSH.


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



### Nginx installed on EC2 in Private using user data =
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
