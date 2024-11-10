# VPC
AWS Console -> Services -> Networking & Content Delivery -> VPC -> Your VPCs
VPC Name: MyVPC
IPv4 CIDR Block: 10.0.0.0/16
Click Create
![90](https://github.com/user-attachments/assets/10343b81-c870-420f-a2a5-63036d73c386)


NOW CREATE 4 SUBNETS - 2 PVT 2 PUBLIC WITH ADDRESS 10.0.1.0/24 , 10.0.2.0/24 , 10.0.3.0/24 , 10.0.4.0/24 
![subnet](https://github.com/user-attachments/assets/20e39867-6cf0-4b63-928d-edb4da49fc32)

THEN CREATE INTERNET GATEWAY AND CONNECT VPC TO IT AND THEN CREATE VGW AND CONNECT(ATTACH) VPC TO IT. NOW GO TO ROUTE TABLES AND CREATE 2 ROUTE TABLE - R1-IGW , R2-VGW AND EDIT ROUTES WITH 0.0.0.0/0 AND 192.168.0.0/16 RESPECTIVELY AND TARGET IGW AND VGW RESPECTIVELY.
![rr](https://github.com/user-attachments/assets/0cd8bf7a-17d0-48e8-a9b8-72ce479a79a1)



Now create 2 instances of same type with select VPC which you created and using putty download apache-2 on both and edit like test-1 and test-2 respectively for better understanding.Like
![tt23](https://github.com/user-attachments/assets/c0a20bf6-b54d-4c9c-af59-320ec88f2f23)

![1t](https://github.com/user-attachments/assets/fe4e0efe-142a-4f6e-900b-66eab17f5cf5)
![2t](https://github.com/user-attachments/assets/6131bb31-4180-462c-941f-bc006fb79e08)

Now to create LOAD BALANCER (WE NAMED server-computer HERE ) OF APPLICTION TYPE , WE NEED TO CREATE TARGET GROUP AND ATTACH BOTH EC2 INSTANCES WE CREATED AND EDIT HEALTH CHECK-UPS AS-
![HELTH](https://github.com/user-attachments/assets/91af3b9a-95fe-49a7-a3c9-dc953323cf7a)


AND NOW SELECT THIS TARGET (WE NAMED AS T-1 HERE)
AND CREATE LOAD BALANCER , NOW COPY YOUR LOAD BALANCER'S DNS NAME AND PASTE IT IN OTHER TAB AND RELOAD TWICE TO SEE ITS WORKING AS-
![L1](https://github.com/user-attachments/assets/7e1f0064-09f3-4d22-aff1-37d836682dab)
![L2](https://github.com/user-attachments/assets/dde85906-1283-41df-bc05-38091c2564d8)
