# **Automated EKS Deployment with CI/CD: A Complete Guide Using Jenkins and Terraform**

![Project Preview](image.png)

## **Overview**

This repository provides a step-by-step guide to automating the deployment of an Amazon Elastic Kubernetes Service (EKS) cluster and a Kubernetes-based application using Jenkins and Terraform. By integrating infrastructure-as-code (IaC) and continuous integration/continuous deployment (CI/CD), this project simplifies and accelerates the delivery pipeline.

---

## **Features**

- 🚀 **Automated EKS Deployment**: Use Terraform to provision a scalable, secure, and resilient EKS cluster.
- 🕠️ **CI/CD Pipeline with Jenkins**: Configure a Jenkins pipeline to automate cluster setup and application deployment.
- 🌐 **Kubernetes Integration**: Deploy and manage containerized applications with Kubernetes manifest files.
- 🔒 **Infrastructure as Code**: Ensure reproducibility and reliability with Terraform scripts.
- 📈 **Scalable Architecture**: Leverage AWS cloud infrastructure for high availability.

---

## **Project Structure**

```plaintext
📂 Root Directory
🔷📂 tf-aws-eks          # Terraform scripts for EKS cluster creation
🔷📂 jenkins_server      # Terraform and shell scripts for Jenkins setup
🔷📂 manifest            # Kubernetes YAML files for application deployment
🔷 Jenkinsfile            # Jenkins pipeline script
🔷 README.md              # Documentation
🔷 image.png              # Project diagram or preview
```

---

## **Key Components**

### **1. Setting Up Jenkins**
- Create an EC2 instance with Terraform to host Jenkins.
- Install tools like `Java`, `Terraform`, `Docker`, `AWS CLI`, and `Kubectl`.
- Configure Jenkins for CI/CD operations.

### **2. EKS Cluster Creation**
- Write Terraform scripts to create a secure and scalable EKS cluster within a private subnet.
- Secure cluster access using IAM roles and policies.

### **3. Application Deployment**
- Deploy a simple Nginx application to the EKS cluster using Kubernetes manifests.
- Configure a LoadBalancer to expose the application.

### **4. CI/CD Pipeline**
- Automate EKS provisioning and application deployment using a Jenkins pipeline.
- Integrate Terraform and Kubernetes commands into Jenkins stages.

---

## **Pre-Requisites**

Before you begin, ensure the following are ready:

1. **AWS Account**: Set up an IAM user with access keys for Terraform and Jenkins.
2. **Tools Installed**:
   - AWS CLI ([Install Guide](https://docs.aws.amazon.com/cli/latest/userguide/install-cliv2.html))
   - Terraform ([Install Guide](https://developer.hashicorp.com/terraform/tutorials/aws-get-started/install-cli))
   - Kubectl ([Install Guide](https://kubernetes.io/docs/tasks/tools/install-kubectl/))
3. **Key Pair**: Create an EC2 key pair for SSH access to the Jenkins server.

---

## **How to Use**

1. **Clone the Repository**:
   ```bash
   git clone <repository_url>
   cd <repository_folder>
   ```

2. **Initialize Terraform**:
   ```bash
   cd jenkins_server
   terraform init
   ```

3. **Apply Terraform Configuration**:
   ```bash
   terraform apply -var-file=variables/dev.tfvars
   ```

4. **Access Jenkins**:
   - Retrieve the Jenkins server's public IP and open it in a browser.
   - Follow the setup instructions and configure the pipeline.

5. **Run the Jenkins Pipeline**:
   - Configure your AWS credentials and Git repository in Jenkins.
   - Start the pipeline to deploy the EKS cluster and application.

---

## **Outputs**

- A running EKS cluster on AWS.
- A deployed Nginx application accessible via a LoadBalancer endpoint.
- A Jenkins pipeline automating infrastructure and application deployment.

---

## **Screenshots**

### Jenkins Pipeline Execution
![Pipeline Execution](https://via.placeholder.com/700x400)

### EKS Cluster in AWS
![EKS Cluster](https://via.placeholder.com/700x400)

### Application Running
![Application Screenshot](https://via.placeholder.com/700x400)

---

## **Future Enhancements**

- **Monitoring & Logging**: Integrate Prometheus and Grafana for monitoring.
- **Security Improvements**: Add secret management and fine-grained access control.
- **Multi-Environment Deployment**: Support staging and production environments.

---

## **Contributing**

Contributions are welcome! Feel free to submit a pull request or open an issue for discussion.

---

## **License**

This project is licensed under the [MIT License](LICENSE).

---

