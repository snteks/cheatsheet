Setting up a web application backed by micro services on Amazon EKS (Elastic Kubernetes Service) involves multiple components and considerations. Below is a list of key components and steps you might need to consider for such an infrastructure:

1. **[[Amazon EKS Cluster]]:**
   - Create an Amazon EKS cluster to manage your Kubernetes environment.

2. **[[Amazon ECR (Elastic Container Registry) or Docker Hub]]:**
   - Store your container images in a container registry. Amazon ECR is a managed container registry that integrates with Amazon EKS.

3. [[Kubernetes Manifests]]:
   - Define Kubernetes manifests (YAML files) for your microservices and other resources like deployments, services, ingress controllers, etc.

4. **[[Microservices]]:**
   - Develop microservices for your application. Each microservice should be containerized and deployable independently.

5. **[[Container Orchestration]]:**
   - Use Kubernetes for container orchestration. Define Deployments, Services, ConfigMaps, and Secrets in your Kubernetes manifests.

6. **[[Load Balancer or Ingress Controller]]:**
   - Set up a load balancer or an Ingress controller to route external traffic to your microservices. This could be AWS ALB (Application Load Balancer) or an Ingress controller like Nginx or Traefik.

7. **[[Networking]]:**
   - Configure networking for your microservices. Ensure that the necessary security groups, network policies, and VPC configurations are in place.

8. **[[AWS RDS (Relational Database Service)]]:**
   - If your application requires a relational database, consider using Amazon RDS. Configure your microservices to connect to the database.

9. **[[AWS Secrets Manager]]:**
   - Manage sensitive information, such as database credentials, using AWS Secrets Manager.

10. **[[Monitoring and Logging]]:**
    - Set up monitoring tools like Amazon CloudWatch or Prometheus for monitoring your EKS cluster. Configure logging to capture application logs.

11. **[[AWS Identity and Access Management (IAM)]]:**
    - Define IAM roles and policies for your services to access AWS resources securely.

12. **[[Security]]:**
    - Implement security best practices, such as encrypting data in transit and at rest, securing access to your cluster, and regularly updating dependencies.

13. **[[Continuous Integration/Continuous Deployment (CI/CD)]]:**
    - Implement a CI/CD pipeline to automate the deployment process. You can use tools like AWS CodePipeline, Jenkins, or GitLab CI.

14. **[[Scaling]]:**
    - Configure autoscaling for your services to handle varying workloads.

15. **[[Backup and Disaster Recovery]]:**
    - Implement backup strategies for your data and have a disaster recovery plan in place.

16. **[[AWS CloudFormation or Terraform]]:**
    - Use Infrastructure as Code (IaC) tools like AWS CloudFormation or Terraform to define and provision your infrastructure.

17. **[[SSL&TLS Certificates]]:**
    - If your application requires secure communication, obtain and configure SSL/TLS certificates.

18. **[[DNS Configuration]]:**
    - Set up DNS records to point to your application's external-facing services.

19. **[[Service Discovery]]:**
    - Consider implementing service discovery mechanisms to allow services to discover and communicate with each other dynamically.

This is a high-level overview, and the specific details will depend on the requirements of your web application and microservices architecture. Always refer to the official AWS documentation for the most up-to-date information and best practices.