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

<img width="1919" height="907" alt="Screenshot 2026-05-25 171113" src="https://github.com/user-attachments/assets/b0abaf16-f174-4777-a61a-5c645edc0797" />

<img width="1917" height="906" alt="Screenshot 2026-05-25 171140" src="https://github.com/user-attachments/assets/d42d3e46-bc74-4879-9df0-382edff0b36c" />

# Step 7: Configured S3 event trigger for Lambda automation



# Step 8: Uploaded StreamFlow frontend website into S3

# Step 9: Created CloudFront distribution for global CDN delivery

# Step 10: Created EC2 backend application server

# Step 11: Created AMI from configured backend server

# Step 12: Created Launch Template for Auto Scaling

# Step 13: Created Application Load Balancer

# Step 15: Created Auto Scaling Group

# Step 16: Tested complete media processing workflow
