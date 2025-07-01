# # Hands-On Project AWS: IAM for Zappy e-Bank

## Project Overview
This 2-hour mini-project explores AWS IAM for Zappy e-Bank, a fintech startup, focusing on users, groups, policies, MFA, and role attachment to an EC2 instance, executed on Ubuntu (WSL) with VS Code via Ubuntu.

## Setup
- Initiated on Jul 01, 2025, 11:14 AM WAT.
- Used Ubuntu terminal (WSL) with VS Code, documenting in ~/Documents/Workspace/AWS_IAM_Project.

## Project Execution

### 1. Log In and Navigate to IAM Dashboard
- Logged into AWS Management Console and accessed IAM dashboard.

### 2. Create IAM Policies
- **Developers Policy**: Created “ZappyDevPolicy” for EC2 access (all actions, all resources).
- **Analysts Policy**: Created “ZappyAnalystPolicy” for S3 access (all actions, all resources).

### 3. Create IAM Groups
- **Development-Team**: Group with “ZappyDevPolicy” for EC2 access.
- **Analyst-Team**: Group with “ZappyAnalystPolicy” for S3 access.

### 4. Create IAM Users
- **John**: Added to “Development-Team” with console access.
- **Mary**: Added to “Analyst-Team” with console access.

### 5. Test and Validate Access
- **John’s Access**: Logged in, accessed EC2, and confirmed instance management.
- **Mary’s Access**: Logged in, accessed S3, and confirmed bucket creation.
- **Validation**: Verified least privilege (John no S3, Mary no EC2).

### 6. Implement Multi-Factor Authentication (MFA)
- **John’s MFA**: Enabled with authenticator app, verified with codes.
- **Mary’s MFA**: Enabled similarly.

### 7. Attach IAM Role to EC2 Instance
- Created “EC2DevRole” with “ZappyDevPolicy,” attached to a new EC2 instance, and verified EC2 actions.

### Project Reflection
1. **Role of IAM in AWS**: IAM manages identities and permissions, ensuring secure and efficient resource access by defining who can do what, critical for Zappy e-Bank’s data security.
2. **IAM Users vs. Groups**: Users are individual identities (e.g., John for specific tasks); groups organize users with shared policies (e.g., Development-Team for all developers), simplifying management.
3. **Creating IAM Policies**: Involves selecting a service (e.g., EC2), defining actions and resources, naming (e.g., “ZappyDevPolicy”), and attaching to users/groups.
4. **Principle of Least Privilege**: Limits users to necessary permissions (e.g., John only EC2), reducing security risks in cloud environments.
5. **John and Mary Scenario**: John’s “Development-Team” config allows EC2 access for coding; Mary’s “Analyst-Team” config allows S3 access for data analysis, both aligning with least privilege.

## Tools Used
- **Ubuntu Terminal (WSL)**: For documentation.
- **VS Code**: For editing `README.md`.
- **Git Bash**: For version control (optional).
- **AWS Management Console**: For IAM and EC2 management.

## Conclusion
This project successfully secured Zappy e-Bank’s AWS environment with IAM, implementing least privilege and MFA, providing a foundation for fintech cloud security.