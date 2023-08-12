# Virtual-Coffee-Shop-Launch
   AWS COMPUTE AND VPC

## To Do: Virtual Coffee Shop Launch
Problem statement: You are the cloud engineer for a virtual coffee shop chain that wants to move to their operations to the cloud. They need a scalable and cost effective solution to ensure their website and backend are always up and running

Solution
1. Setting up the infra
   a. create VPC with the details
       IP 10.0.0.0/16
<img width="214" alt="image" src="https://github.com/faraid/Virtual-Coffee-Shop-Launch/assets/46371646/420e55ee-abdc-4c24-a20c-8dfc65eb53b6">

created newly Coffeeshop VPC
![image](https://github.com/faraid/Virtual-Coffee-Shop-Launch/assets/46371646/0c7a3786-04b4-4ae4-923f-52927e7abd97)

## Creation of Subnets
I have created 2 Public Subnets and 2 Private Subnets

   10.0.1.0/24 -- Public Subnet 1
   10.0.2.0/24 -- Public Subnet 2
   10.0.3.0/24 -- Private Subnet 1
   10.0.4.0/24 -- Private Subnet 2
   
![image](https://github.com/faraid/Virtual-Coffee-Shop-Launch/assets/46371646/61226b5c-c3c7-407e-b539-be9bebd84fa8)

![image](https://github.com/faraid/Virtual-Coffee-Shop-Launch/assets/46371646/07d2053b-c85d-4069-8dce-63a34bcabdee)

![image](https://github.com/faraid/Virtual-Coffee-Shop-Launch/assets/46371646/32734aa7-9b83-4bab-a1bc-bae34d030539)

![image](https://github.com/faraid/Virtual-Coffee-Shop-Launch/assets/46371646/2ebde69c-2c52-425e-acfa-d943e4937ce2)

![image](https://github.com/faraid/Virtual-Coffee-Shop-Launch/assets/46371646/8a94937b-7041-4827-acf7-29fa0e6f47a6)

## Creation of Internet Gateway IGW

![image](https://github.com/faraid/Virtual-Coffee-Shop-Launch/assets/46371646/fb4bc7d0-6e48-414a-b140-634d73f88c56)

Attaching IGW to VPC
![image](https://github.com/faraid/Virtual-Coffee-Shop-Launch/assets/46371646/2458fc41-b61a-4586-9f7e-f6a4244b8e79)
![image](https://github.com/faraid/Virtual-Coffee-Shop-Launch/assets/46371646/25366cac-3c97-46b2-b6df-492d44f69291)

## Allocation of EIP to Public Sunets

![image](https://github.com/faraid/Virtual-Coffee-Shop-Launch/assets/46371646/8fed5f36-36d0-4937-91b5-9a57d0cd9406)

## Creation of Route Table and Subnet Association

Public Route Table
![image](https://github.com/faraid/Virtual-Coffee-Shop-Launch/assets/46371646/8a3f8229-3939-4eab-aebb-2875dea9af21)

Association of Public Subnets
![image](https://github.com/faraid/Virtual-Coffee-Shop-Launch/assets/46371646/d9e932e9-c355-416a-95f9-0ec874b93bc1)


Private Route Table
![image](https://github.com/faraid/Virtual-Coffee-Shop-Launch/assets/46371646/41069c72-d7b9-405a-b6fb-1a7384a25f1d)

## Editing of Routes
Routes in Public Route table to be editted and add route 0.0.0.0/0 to igw 
![image](https://github.com/faraid/Virtual-Coffee-Shop-Launch/assets/46371646/835878af-54f2-46a2-8409-480c28dd2665)

## Creation of NAT gateway for the Private Subnets Instances
NAT aateway
![image](https://github.com/faraid/Virtual-Coffee-Shop-Launch/assets/46371646/3ab739a4-5b7b-48a2-9037-42be2716e9a0)

Private Routes associated to NAT gateway 
![image](https://github.com/faraid/Virtual-Coffee-Shop-Launch/assets/46371646/10efabfa-3288-4233-87df-35a6ebd194e2)

## launch EC2 Instances

### coffeeshop Webserver1 in Public Subnet 1

![image](https://github.com/faraid/Virtual-Coffee-Shop-Launch/assets/46371646/aed24089-3264-4bd3-be82-49abc844b649)
![image](https://github.com/faraid/Virtual-Coffee-Shop-Launch/assets/46371646/a55dce1f-464d-479f-baa7-6b6f427a700a)
![image](https://github.com/faraid/Virtual-Coffee-Shop-Launch/assets/46371646/a1072db1-4a62-42e3-9769-c821fc80349b)

#### coffeeshop Webserver2 in Public Subnet 2
![image](https://github.com/faraid/Virtual-Coffee-Shop-Launch/assets/46371646/6b3c611e-8e28-4f16-abc0-5c4a241f4904)
![image](https://github.com/faraid/Virtual-Coffee-Shop-Launch/assets/46371646/759fe9fa-7eef-45a5-9bd0-3c5c6f9319c8)

### 2 webservers in 2 different AZ 
![image](https://github.com/faraid/Virtual-Coffee-Shop-Launch/assets/46371646/fd4cfd24-cc55-4e92-83a5-a34c89e2fc74)

### coffeeshop dbservers in private subnet 1
![image](https://github.com/faraid/Virtual-Coffee-Shop-Launch/assets/46371646/9e634e72-54f3-4fd2-8aaa-5f9d68239c00)
![image](https://github.com/faraid/Virtual-Coffee-Shop-Launch/assets/46371646/0da306e1-f390-4b4c-8f11-1a6187e2a007)
![image](https://github.com/faraid/Virtual-Coffee-Shop-Launch/assets/46371646/a6b9b866-78bb-4b44-b589-8da96675808c)

### coffeeshop dbservers in private subnet 2
![image](https://github.com/faraid/Virtual-Coffee-Shop-Launch/assets/46371646/64c90139-9cbd-4362-8c65-c0f1b0b71dbf)
![image](https://github.com/faraid/Virtual-Coffee-Shop-Launch/assets/46371646/8aad0bc7-6273-4918-8cfd-0f7caab9a4ef)
![image](https://github.com/faraid/Virtual-Coffee-Shop-Launch/assets/46371646/45633dc7-f212-46f0-87be-ef3832878582)

