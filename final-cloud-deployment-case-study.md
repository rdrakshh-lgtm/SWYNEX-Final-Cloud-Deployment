\# SWYNEX Technologies Internship

\# Task 4: Final Cloud Deployment Case Study



\## 1. Introduction



This case study presents the work completed during the SWYNEX Technologies cloud internship tasks. It combines cloud architecture design, static website deployment, monitoring concepts, cost awareness, security practices, and lessons learned.



The objective is to understand the complete cloud deployment workflow, from designing an architecture to publishing a website and documenting operational best practices.



\### Project Details



\- Organization: SWYNEX Technologies

\- Project: Final Cloud Deployment

\- Domain: Cloud Computing

\- Hosting Platform: GitHub Pages

\- Documentation Format: Markdown



\## 2. Project Objectives



The main objectives of this project are:



\- Understand cloud architecture and infrastructure design.

\- Design a scalable and secure cloud architecture.

\- Deploy a responsive static website.

\- Understand deployment verification and status checks.

\- Document monitoring and alerting strategies.

\- Identify methods for reducing cloud costs.

\- Apply security and access-control best practices.

\- Document lessons learned during the project.



\## 3. Cloud Architecture Design



\### 3.1 Overview



The initial architecture task focused on designing a cloud-based Task Management REST API using Amazon Web Services (AWS).



The proposed architecture includes services for application hosting, database management, file storage, caching, security, networking, and monitoring.



\### 3.2 Proposed AWS Components



\*\*Amazon ECS with AWS Fargate\*\*

\- Runs containerized backend application services.

\- Supports horizontal scaling.

\- Reduces the need to manage application servers directly.



\*\*Application Load Balancer\*\*

\- Distributes incoming application traffic.

\- Routes requests to healthy application targets.



\*\*Amazon RDS for PostgreSQL\*\*

\- Stores structured application data.

\- Supports managed relational database operations.



\*\*Amazon S3\*\*

\- Stores uploaded files and static assets.

\- Provides durable object storage.



\*\*Amazon ElastiCache for Redis\*\*

\- Provides in-memory caching.

\- Can reduce repeated database queries.



\*\*Amazon CloudFront\*\*

\- Delivers static content through a content delivery network.

\- Can improve content delivery performance.



\*\*Amazon Route 53\*\*

\- Provides DNS and domain-routing capabilities.



\*\*Amazon Cognito\*\*

\- Can support user authentication and identity management.



\*\*AWS Secrets Manager\*\*

\- Stores application secrets and credentials securely.



\*\*Amazon CloudWatch\*\*

\- Supports metrics, logs, dashboards, and alarms.



\*\*AWS CloudTrail\*\*

\- Records supported AWS account and API activity for auditing.



\### 3.3 Network and Security Design



The proposed design uses a Virtual Private Cloud (VPC) with separated network subnets.



\- Public subnets can host internet-facing components such as a load balancer.

\- Private application subnets can host backend services.

\- Private database subnets can isolate database resources.

\- Security groups restrict network traffic.

\- IAM policies control access to AWS resources.

\- Secrets should not be hardcoded into source code.



\### 3.4 Scalability and Reliability



The architecture can be designed to support:



\- Horizontal application scaling.

\- Load balancing.

\- Health checks.

\- Database backups.

\- Caching.

\- Centralized monitoring.

\- Controlled access to application resources.



Note: This section documents a proposed AWS architecture. It does not claim that these AWS resources were deployed as part of the static website project.



\## 4. Static Website Deployment



\### 4.1 Project Overview



The second task involved creating and deploying a responsive static website using HTML and CSS.



The website introduces a basic cloud deployment demonstration and provides an example of publishing a website online.



\### 4.2 Technologies Used



\- HTML5

\- CSS3

\- Git

\- GitHub

\- GitHub Pages



\### 4.3 Deployment Process



The deployment workflow was:



1\. Created the website using HTML and CSS.

2\. Tested the website locally.

3\. Created a GitHub repository.

4\. Initialized Git and committed the project files.

5\. Pushed the source code to GitHub.

6\. Configured GitHub Pages to publish the website from the main branch.

7\. Opened the published URL and verified that the website loaded.



\### 4.4 Project Links



\*\*Live Website:\*\*



https://rdrakshh-lgtm.github.io/SWYNEX-Basic-Cloud-Deployment/



\*\*Source Code Repository:\*\*



https://github.com/rdrakshh-lgtm/SWYNEX-Basic-Cloud-Deployment



\### 4.5 Deployment Verification



After deployment, the following checks can be performed:



\- Confirm that the website opens successfully.

\- Verify that the layout is responsive.

\- Confirm that the CSS stylesheet loads.

\- Check for broken links and missing assets.

\- Inspect browser Developer Tools for errors.

\- Review the repository's deployment status.



\## 5. Monitoring and Logging



\### 5.1 Importance of Monitoring



Monitoring helps identify availability issues, deployment failures, and application errors.



A reliable monitoring process helps teams detect problems and investigate them before they affect more users.



\### 5.2 Basic Monitoring Checks



The following checks are appropriate for the static website:



\- Open the live website periodically.

\- Verify that important page elements load correctly.

\- Check browser network requests for failed assets.

\- Inspect browser console errors.

\- Review GitHub Pages deployment status.

\- Review GitHub Actions logs when a deployment workflow is configured.



\### 5.3 Logging



For a static website hosted on GitHub Pages, deployment information can be reviewed through GitHub's repository and deployment interfaces.



Browser Developer Tools can help identify client-side errors and failed network requests.



This deployment does not include a separately configured application server with centralized server logs.



\### 5.4 Proposed Alerting Strategy



A basic website availability alert can follow this process:



1\. Periodically check the website using an uptime-monitoring service.

2\. Detect repeated failed availability checks.

3\. Send a notification through a supported channel.

4\. Investigate hosting status, deployment history, and configuration.

5\. Fix the issue and verify that the website is accessible again.



This is a proposed approach. An external monitoring service must be configured before real alerts can be generated.



\## 6. Cost Awareness



Cost awareness helps avoid unnecessary cloud spending.



\### 6.1 Cost Optimization Practices



\- Select hosting services appropriate to project requirements.

\- Review service pricing before creating cloud resources.

\- Use free or low-cost services where suitable.

\- Set budgets and billing alerts when using paid cloud services.

\- Remove unused resources.

\- Optimize large images and static assets.

\- Review storage and data-transfer usage.

\- Monitor service limits and billing reports.

\- Understand the limitations of free-tier services.



\### 6.2 Hosting Cost Considerations



The demonstration website uses GitHub Pages for static hosting.



The proposed AWS architecture describes a separate application design whose actual costs would depend on service selection, resource size, traffic, storage, and data transfer.



No specific cloud cost savings are claimed because a paid AWS deployment and its billing data were not measured for this project.



\## 7. Security and Access Control



Security is important throughout the development and deployment lifecycle.



\### 7.1 Security Checklist



\- Enable two-factor authentication on GitHub.

\- Use strong, unique passwords.

\- Restrict repository permissions to trusted contributors.

\- Never commit passwords, API keys, or access tokens.

\- Review changes before merging them.

\- Keep dependencies updated when applicable.

\- Use HTTPS when accessing the live website.

\- Review repository and deployment permissions.

\- Apply least-privilege IAM policies when using AWS.

\- Store cloud credentials in an appropriate secrets-management service.

\- Restrict database access to authorized application components.



\### 7.2 Access Control in AWS



For the proposed AWS architecture:



\- Use IAM roles and policies to control access.

\- Avoid sharing long-lived credentials unnecessarily.

\- Restrict inbound and outbound network access where appropriate.

\- Keep databases in private subnets when the design permits.

\- Audit relevant account activity.

\- Review access permissions regularly.



\## 8. Deployment Workflow



The overall workflow followed for the static website is:



\*\*Plan → Develop → Test → Commit → Push → Deploy → Verify → Document\*\*



\### Workflow Explanation



1\. Plan the website and required files.

2\. Develop the HTML and CSS.

3\. Test the website locally.

4\. Commit changes using Git.

5\. Push changes to the GitHub repository.

6\. Publish the website using GitHub Pages.

7\. Verify the deployed website.

8\. Document monitoring, security, and cost considerations.



\## 9. Challenges and Solutions



\### Challenge 1: Git and Repository Setup



\*\*Challenge:\*\* Connecting a local project to its GitHub repository required correct folder paths and Git configuration.



\*\*Solution:\*\* Used Git Bash to initialize the repository, configure the remote, commit files, and push the project.



\### Challenge 2: Website Deployment



\*\*Challenge:\*\* The website needed to be published online rather than remain available only on the local computer.



\*\*Solution:\*\* Configured GitHub Pages to publish the website from the main branch.



\### Challenge 3: Deployment Verification



\*\*Challenge:\*\* A successful source-code push does not automatically prove that the live website works correctly.



\*\*Solution:\*\* Opened the published URL and verified the deployed website.



\### Challenge 4: Monitoring and Cost Awareness



\*\*Challenge:\*\* Monitoring, alerting, and cloud cost management require a clear understanding of operational practices.



\*\*Solution:\*\* Documented status checks, a proposed alerting workflow, cost-awareness measures, and security checklists.



\## 10. Lessons Learned



This project helped develop an understanding of:



\- Basic cloud architecture design.

\- The purpose of common AWS services.

\- Static website development using HTML and CSS.

\- Version control using Git and GitHub.

\- Publishing a website with GitHub Pages.

\- Deployment verification and troubleshooting.

\- Monitoring and logging concepts.

\- Cost-awareness practices.

\- Security and access-control principles.

\- Technical documentation and project presentation.



The project also highlighted the importance of distinguishing between a proposed cloud architecture and infrastructure that has actually been deployed.



\## 11. Future Improvements



Possible future improvements include:



\- Deploying a backend application to a cloud platform.

\- Configuring a real uptime-monitoring service.

\- Implementing email or other availability alerts.

\- Adding automated testing.

\- Integrating a continuous deployment workflow.

\- Configuring cloud budgets and billing notifications.

\- Adding a custom domain.

\- Performing security reviews and performance testing.



These are future improvements and are not claimed as completed features.



\## 12. Conclusion



This final cloud deployment case study brings together cloud architecture design, static website deployment, monitoring concepts, cost awareness, and security practices.



The project demonstrates the importance of planning infrastructure, publishing and verifying a website, documenting operational procedures, and applying appropriate security controls.



The experience provides a foundation for exploring more advanced cloud deployments and DevOps practices.



\*\*Project:\*\* Final Cloud Deployment Case Study  

\*\*Organization:\*\* SWYNEX Technologies  

\*\*Status:\*\* Documentation and static website deployment completed



\## 13. References



\- AWS Documentation: https://docs.aws.amazon.com/

\- Git Documentation: https://git-scm.com/doc

\- GitHub Documentation: https://docs.github.com/

\- GitHub Pages Documentation: https://docs.github.com/en/pages

