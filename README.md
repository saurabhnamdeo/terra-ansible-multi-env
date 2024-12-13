Sure! Here's a `README.md` file for your GitHub repository:

```markdown
# AWS EC2 Setup and Configuration

This repository contains steps to set up an AWS EC2 instance, install Ansible and Terraform, create an AWS IAM user, and configure AWS CLI.

## Steps

Step 1: Create AWS EC2 t2.medium Instance
1. Log in to your AWS Management Console.
2. Navigate to the EC2 Dashboard.
3. Click on "Launch Instance".
4. Choose the Amazon Machine Image (AMI) you prefer.
5. Select the instance type `t2.medium`.
6. Configure instance details, add storage, and configure security groups as needed.
7. Review and launch the instance.

Step 2: Install Ansible
1. SSH into your EC2 instance.
2. Update the package list:
   ```bash
   sudo apt-get update
   ```
3. Install Ansible:
   ```bash
   sudo apt-get install -y ansible
   ```

### Step 3: Install Terraform
1. SSH into your EC2 instance.
2. Install dependencies:
   ```bash
   sudo apt-get install -y gnupg software-properties-common curl
   ```
3. Add the HashiCorp GPG key:
   ```bash
   curl -fsSL https://apt.releases.hashicorp.com/gpg | sudo apt-key add -
   ```
4. Add the HashiCorp Linux repository:
   ```bash
   sudo apt-add-repository "deb [arch=amd64] https://apt.releases.hashicorp.com $(lsb_release -cs) main"
   ```
5. Update the package list and install Terraform:
   ```bash
   sudo apt-get update
   sudo apt-get install -y terraform
   ```

### Step 4: Create AWS IAM User and Key
1. Log in to your AWS Management Console.
2. Navigate to the IAM Dashboard.
3. Click on "Users" and then "Add user".
4. Enter a username and select "Programmatic access".
5. Attach the necessary policies (e.g., `AdministratorAccess`).
6. Complete the steps to create the user and download the access key and secret key.

### Step 5: Configure AWS CLI with IAM User
1. SSH into your EC2 instance.
2. Install AWS CLI if not already installed:
   ```bash
   sudo apt-get install -y awscli
   ```
3. Configure AWS CLI with the IAM user credentials:
   ```bash
   aws configure
   ```
   - Enter the access key ID.
   - Enter the secret access key.
   - Enter the default region name (e.g., `us-west-2`).
   - Enter the default output format (e.g., `json`).

You are now ready to use Ansible and Terraform on your AWS EC2 instance!
```

Feel free to customize this `README.md` file as needed. If you have any more questions or need further assistance, let me know!
