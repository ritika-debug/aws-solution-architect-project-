# AWS Solution Architect Project - Scalable Web Application

This project demonstrates the design and deployment of a scalable, secure, and high-availability web application on AWS. The infrastructure is provisioned using AWS services such as EC2, RDS, VPC, S3, IAM, and CloudWatch.

## **Architecture Overview**

This architecture uses the following AWS services:
- **VPC**: Custom VPC with public and private subnets.
- **EC2**: Auto Scaling EC2 instances for the backend application.
- **RDS**: Multi-AZ setup for a highly available database.
- **S3**: Static file storage (images, CSS, JS).
- **CloudFront**: CDN for caching and serving static files globally.
- **IAM**: Role-based access control for resources.
- **CloudWatch**: Logging and monitoring of infrastructure.


## **Setup Instructions**

### Prerequisites
- AWS Account
- AWS CLI installed
- CloudFormation templates
- Node.js and npm (for backend)

### Steps to Deploy
1. **Create VPC & Subnets**:
   - Navigate to the  and launch the CloudFormation stack.
   
2. **Deploy EC2 Instances**:
   - Launch EC2 instances using the  file, ensuring that Auto Scaling and ELB are configured.

3. **Set Up RDS Database**:
   - Launch the RDS stack using . Ensure Multi-AZ is enabled.

4. **Configure S3 and CloudFront**:
   - Set up the S3 bucket for static file storage with the .
   - Use  for CloudFront setup.

5. **Deploy Backend**:
   - Clone the  directory and deploy the Node.js (or Python) API to EC2.

6. **Frontend Application**:
   - Deploy the frontend in the  directory to an S3 bucket for static hosting.

### Monitoring
- CloudWatch is set up to monitor EC2 instances, RDS, and Auto Scaling. You will receive alarms for any performance issues.

## **Conclusion**

This architecture ensures that your web application is scalable, secure, and cost-effective. You can further enhance the project by adding features like serverless components or integrating API Gateway and Lambda for a more microservice-driven approach.

