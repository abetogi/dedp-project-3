# Write-up Template

### Analyze, choose, and justify the appropriate resource option for deploying the app.

*For **both** a VM or App Service solution for the CMS app:*
- *Analyze costs, scalability, availability, and workflow*

Costs
Azure Virtual Machines:
- Higher up-front costs for setup and ongoing maintenance
- Costs can fluctuate based on the type of VM, storage, and additional services
- Typically more expensive for small-scale applications

Azure App Service:
- Predictable and lower costs with different pricing tiers (Dev/Test, Production, Isolated)
- You only pay for the App Service plan, with various options to suit different needs
- Continuous integration and deployment can reduce operational costs

Scalability
Azure Virtual Machines:
- Requires manual configuration and management for scaling
- Can support high scalability with Virtual Machine Scale Sets and Load Balancers

Azure App Service:
- Built-in auto-scaling 
- Seamless scalability without manual intervention
- Ideal for web applications with fluctuating traffic

Availability
Azure Virtual Machines:
- High availability options require setting up multiple VMs, load balancers, and availability zones
- More control over redundancy and failover mechanisms

Azure App Service:
- High availability is built-in
- Supports multiple regions and auto-failover
- SLA (Service Level Agreement) ensures 99.95% uptime

Workflow
Azure Virtual Machines:
- Full control over the OS and environment
- More complex setup and management
- Time-consuming for ongoing maintenance and updates

Azure App Service:
- Simplified deployment and management
- Focus on application development rather than infrastructure
- Continuous integration and deployment support with GitHub, Azure DevOps, etc.

- *Choose the appropriate solution (VM or App Service) for deploying the app*

Given the basic nature of the CMS application, where users can log in, view, and publish articles with text stored in Azure SQL Server and images in Azure Blob Storage, the Azure App Service is the appropriate solution.

Azure App Service is cost-effective with predictable, lower costs and flexible pricing tiers suited for a simple CMS application. It offers built-in auto-scaling to handle varying traffic loads without manual intervention, ensuring high availability and regional redundancy to minimize downtime. This service simplifies management by allowing developers to focus on the application while Azure manages the infrastructure. Additionally, it supports continuous deployment, enabling seamless integration and deployment with popular repositories like GitHub and Azure DevOps, which streamlines the development workflow.

### Assess app changes that would change your decision.

If the CMS application evolved to require greater control over the OS, such as specific OS configurations or custom software installations not supported by App Service, using Virtual Machines would become necessary. High-performance compute needs, including extensive data processing or other resource-intensive operations, would also make VMs more appropriate. For complex applications requiring specific environments or configurations, VMs would offer the necessary flexibility. Additionally, if the CMS needed to install and run custom software or services not supported by App Service, VMs would be a better fit.