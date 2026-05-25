# StreamFlow-Cloud-Native-
Built a complete cloud-native media streaming ecosystem using AWS CloudFront, S3, EC2, Auto Scaling, ALB, Lambda, SNS, SQS, CloudTrail, CloudWatch, Glacier, IAM, and KMS.

This project simulates a real-world streaming platform similar to Netflix or Spotify where users upload media, stream content globally, trigger automated processing workflows, receive notifications, and archive older media content while maintaining scalability, observability, and fault tolerance

# Problem Statement
StreamFlow’s platform traffic and media uploads were increasing rapidly.
Problems:

large-scale media uploads
traffic spikes during peak streaming hours
no automated media processing pipeline
backend processing overload risks
increasing long-term storage costs
lack of centralized monitoring and auditing
no scalable backend architecture

# Architecture
Users
   ↓
CloudFront CDN
   ↓
S3 Frontend Hosting
   ↓
Application Load Balancer
   ↓
Auto Scaling EC2 Backend Layer
   ↓
S3 Media Upload Storage
   ↓
Lambda Media Processing
   ↓
SNS Upload Notifications
   ↓
SQS Processing Queue
   ↓
CloudWatch Monitoring
   ↓
CloudTrail Auditing
   ↓
S3 Glacier Media Archival

# AWS Services Used
-IAM
-Amazon S3
-Amazon S3 Glacier
-Amazon CloudFront
-Amazon EC2
-Elastic Load Balancing (ALB)
-EC2 Auto Scaling
-Amazon Machine Image (AMI)
-AWS Lambda
-Amazon SNS
-Amazon SQS
-Amazon CloudWatch
-AWS CloudTrail
-AWS KMS

# Solution
Implemented a complete cloud-native media streaming architecture using AWS infrastructure, serverless services, messaging systems, scalable compute, and monitoring services.

The platform:

hosts frontend assets globally using CloudFront and S3
uses EC2 + Auto Scaling for backend application infrastructure
stores uploaded media securely in S3
archives older content into Glacier
processes media uploads automatically using Lambda
distributes notifications using SNS
buffers backend workflows using SQS
Implemented a complete cloud-native media streaming architecture using AWS infrastructure, serverless services, messaging systems, scalable compute, and monitoring services.

The platform:

hosts frontend assets globally using CloudFront and S3
uses EC2 + Auto Scaling for backend application infrastructure
stores uploaded media securely in S3
archives older content into Glacier
processes media uploads automatically using Lambda
distributes notifications using SNS
buffers backend workflows using SQS
monitors infrastructure activity using CloudWatch and CloudTrail

# Step 1: Created IAM user for StreamFlow cloud administration and enabled MFA

<img width="1909" height="902" alt="Screenshot 2026-05-25 224030" src="https://github.com/user-attachments/assets/f395ecc4-1a9c-42b7-8f21-28095700a2a3" />

# Step 2: Created S3 buckets for frontend hosting and media uploads

<img width="1919" height="911" alt="Screenshot 2026-05-25 144855" src="https://github.com/user-attachments/assets/a9a85143-b558-4a37-a973-5bd9e839c270" />


# Step 3: Created lifecycle rules for Glacier archival

<img width="1919" height="906" alt="Screenshot 2026-05-25 144917" src="https://github.com/user-attachments/assets/a0bf460c-8dd7-429b-88a5-c44ea0e338f3" />

<img width="1912" height="912" alt="Screenshot 2026-05-25 145205" src="https://github.com/user-attachments/assets/7534bf42-770e-4a87-9e7d-72c5d2c90576" />

<img width="1913" height="901" alt="Screenshot 2026-05-25 145226" src="https://github.com/user-attachments/assets/58ac2edf-2fba-45dc-85ed-da2de4749ab6" />

# Step 4: Created CloudTrail audit logging with CloudWatch integration

<img width="1909" height="886" alt="Screenshot 2026-05-25 164515" src="https://github.com/user-attachments/assets/44db05d0-92ba-42a4-9e9f-e12ffc3d3506" />

<img width="1916" height="812" alt="Screenshot 2026-05-25 164529" src="https://github.com/user-attachments/assets/0541c2a7-541d-410c-840c-77d310ebead4" />

<img width="1682" height="766" alt="Screenshot 2026-05-25 164617" src="https://github.com/user-attachments/assets/a4ab61b6-f051-4519-956c-923e7fe2711d" />

<img width="1916" height="905" alt="Screenshot 2026-05-25 164645" src="https://github.com/user-attachments/assets/ca1deaa2-8f3f-4be9-ba9f-2c9b611bac14" />

# Step 5: Created SNS topic and SQS queue for media processing workflows

<img width="1916" height="915" alt="Screenshot 2026-05-25 165226" src="https://github.com/user-attachments/assets/3b9eb421-cda7-450d-81bd-f1555fae210d" />

<img width="1919" height="904" alt="Screenshot 2026-05-25 165129" src="https://github.com/user-attachments/assets/9fab3893-757f-4e12-9ba7-32cef74918fd" />

# Step 6: Created Lambda function for automated media processing

<img width="1915" height="904" alt="Screenshot 2026-05-25 165726" src="https://github.com/user-attachments/assets/9528075b-ccf1-4a08-80d0-94fdb28a8099" />

<img width="1919" height="911" alt="Screenshot 2026-05-25 165857" src="https://github.com/user-attachments/assets/59bccd75-92fe-4c9e-8707-d83518120269" />

<img width="1916" height="909" alt="Screenshot 2026-05-25 170017" src="https://github.com/user-attachments/assets/9b88cb76-b1df-4f47-a11a-d82f28028a20" />

<img width="1919" height="899" alt="Screenshot 2026-05-25 170026" src="https://github.com/user-attachments/assets/cf7aebb6-4f37-43b8-9bc2-94e7da018644" />

<img width="1915" height="876" alt="Screenshot 2026-05-25 170153" src="https://github.com/user-attachments/assets/c1b336a6-5f7d-4f61-a364-eba5e242bfae" />

# Step 7: Configured S3 event trigger for Lambda automation

<img width="1919" height="907" alt="Screenshot 2026-05-25 171113" src="https://github.com/user-attachments/assets/0b27333e-517e-41a6-9955-55124afd49b8" />

<img width="1917" height="906" alt="Screenshot 2026-05-25 171140" src="https://github.com/user-attachments/assets/c3db7f68-3f1c-4c21-be4b-b86630fb502d" />

<img width="1914" height="915" alt="Screenshot 2026-05-25 171258" src="https://github.com/user-attachments/assets/6a0c4c8b-07d8-4126-a987-5260eaa174e5" />

<img width="1909" height="806" alt="Screenshot 2026-05-25 171312" src="https://github.com/user-attachments/assets/2569113a-1ec4-46b1-bf73-c7c1829ce041" />


# Step 8: Uploaded StreamFlow frontend website into S3

# Step 9: Created CloudFront distribution for global CDN delivery

<img width="1913" height="903" alt="Screenshot 2026-05-25 171554" src="https://github.com/user-attachments/assets/fce45b16-34d7-456c-b63a-91dcc8b856db" />

<img width="1919" height="872" alt="Screenshot 2026-05-25 172716" src="https://github.com/user-attachments/assets/8159101d-a313-45e5-a9bf-7c729c714386" />

<img width="1918" height="903" alt="Screenshot 2026-05-25 173333" src="https://github.com/user-attachments/assets/5bacb1a5-85b8-474c-8221-eb237fd3b9c7" />

# Step 10: Created EC2 backend application server

<img width="1919" height="913" alt="Screenshot 2026-05-25 212308" src="https://github.com/user-attachments/assets/499136a1-6b3a-48f1-8b25-f1f401f74396" />

<img width="1917" height="903" alt="Screenshot 2026-05-25 212320" src="https://github.com/user-attachments/assets/dd223344-83de-46fa-813c-cdec16d45f56" />

<img width="1906" height="977" alt="Screenshot 2026-05-25 213221" src="https://github.com/user-attachments/assets/ca9c4a38-c44f-4c1c-9643-44dd28e1fd98" />

<img width="1918" height="151" alt="Screenshot 2026-05-25 213305" src="https://github.com/user-attachments/assets/de4039fe-18c5-4f10-9d9a-7d78d9615cbe" />

<img width="1912" height="964" alt="Screenshot 2026-05-25 213532" src="https://github.com/user-attachments/assets/76169609-c108-4b9f-a425-5239481588b8" />

# Step 11: Created AMI from configured backend server

<img width="1915" height="952" alt="Screenshot 2026-05-25 215635" src="https://github.com/user-attachments/assets/267dbd5f-cb08-4990-b62f-e2315392fbc1" />

<img width="1919" height="904" alt="Screenshot 2026-05-25 215842" src="https://github.com/user-attachments/assets/d05db423-66c2-446a-98d2-b41bca4e4d61" />

# Step 12: Created Launch Template for Auto Scaling

<img width="1919" height="908" alt="Screenshot 2026-05-25 215856" src="https://github.com/user-attachments/assets/684bcecd-5c38-4f33-8f04-4c39fc69d9a6" />

<img width="1919" height="902" alt="Screenshot 2026-05-25 220112" src="https://github.com/user-attachments/assets/bdbd4723-c84c-4065-a623-f3e2c8571d66" />

# Step 13: Created Application Load Balancer

<img width="1672" height="896" alt="Screenshot 2026-05-25 220410" src="https://github.com/user-attachments/assets/4b32e438-b789-4426-b785-26d46c043c14" />


<img width="1903" height="775" alt="Screenshot 2026-05-25 220421" src="https://github.com/user-attachments/assets/aea6cfa2-3643-4d6e-ae12-628f79e2f218" />

<img width="1919" height="908" alt="Screenshot 2026-05-25 220446" src="https://github.com/user-attachments/assets/6a1ec7a0-3188-4230-a690-74feb7eb0def" />


# Step 15: Created Auto Scaling Group

<img width="1914" height="909" alt="Screenshot 2026-05-25 221010" src="https://github.com/user-attachments/assets/e0121684-499a-463d-82cf-14725bfead5c" />

<img width="1915" height="904" alt="Screenshot 2026-05-25 220701" src="https://github.com/user-attachments/assets/abba40e8-9dd3-41a3-a00b-e7079b9bf034" />

<img width="1910" height="906" alt="Screenshot 2026-05-25 220734" src="https://github.com/user-attachments/assets/128dd25f-adeb-4e34-9d65-793333e0f2cf" />

<img width="1905" height="905" alt="Screenshot 2026-05-25 221106" src="https://github.com/user-attachments/assets/cffb69b3-7cd2-4e34-bf6f-7533f4000d30" />

<img width="1905" height="905" alt="Screenshot 2026-05-25 221106" src="https://github.com/user-attachments/assets/f48a4447-c207-4467-9077-a2b9619feced" />

<img width="1917" height="897" alt="Screenshot 2026-05-25 221140" src="https://github.com/user-attachments/assets/fd6c8aeb-7a89-497a-98a4-ce3647e9f72c" />

# Step 16: Tested complete workflow:

<img width="1909" height="806" alt="Screenshot 2026-05-25 171312" src="https://github.com/user-attachments/assets/9d1c2871-7645-48ff-88dd-63cbb5e3b055" />

<img width="1918" height="968" alt="Screenshot 2026-05-25 221532" src="https://github.com/user-attachments/assets/eddf37f7-0541-44de-9e14-291192374e8d" />

<img width="1908" height="971" alt="Screenshot 2026-05-25 221441" src="https://github.com/user-attachments/assets/d7101f24-1fbd-4977-b5c5-8cb7349e3606" />




