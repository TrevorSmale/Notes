# AZURE NOTES
## Microsoft Azure Cloud Services

Azure is a cloud computing platform and suite of services provided by Microsoft. It offers tools for building, deploying, and managing applications and infrastructure in the cloud. Azure provides services such as computing, storage, networking, databases, AI, machine learning, IoT, analytics, and security. Developers can use various programming languages, and Azure allows quick scaling based on workload demands. It provides enterprise-level security features and compliance with industry and regulatory standards. Azure is a comprehensive platform for building, deploying, and managing applications and infrastructure in a secure and flexible cloud environment.

# AZ 104 TOPICS

# Table of Contents

## Table of Contents

- [AZURE NOTES](#azure-notes)
  - [Microsoft Azure Cloud Services](#microsoft-azure-cloud-services)
- [AZ 104 TOPICS](#az-104-topics)
- [Table of Contents](#table-of-contents)
  - [Table of Contents](#table-of-contents-1)
  - [Azure Active Directory (Azure AD)](#azure-active-directory-azure-ad)
  - [Azure AD Connect](#azure-ad-connect)
  - [Azure AD Roles and RBAC](#azure-ad-roles-and-rbac)
  - [Azure AD Privileged Identity Management (PIM)](#azure-ad-privileged-identity-management-pim)
  - [Azure AD Conditional Access](#azure-ad-conditional-access)
  - [Azure Policy](#azure-policy)
  - [Azure Blueprints](#azure-blueprints)
  - [Azure Storage Accounts](#azure-storage-accounts)
  - [Azure Blob storage](#azure-blob-storage)
  - [Azure Files](#azure-files)
  - [Azure Managed Disks](#azure-managed-disks)
  - [Azure Backup](#azure-backup)
  - [Azure Site Recovery](#azure-site-recovery)
  - [Azure Storage Explorer](#azure-storage-explorer)
  - [Azure File Sync](#azure-file-sync)
  - [Azure Blob Storage Lifecycle Management](#azure-blob-storage-lifecycle-management)
  - [Azure Blob Storage Access Tiers](#azure-blob-storage-access-tiers)
  - [Azure Shared Access Signatures (SAS)](#azure-shared-access-signatures-sas)
  - [Azure Data Box](#azure-data-box)
  - [Deploy and Manage Azure Compute Resources (25-30%)](#deploy-and-manage-azure-compute-resources-25-30)
  - [Virtual Machines (VMs)](#virtual-machines-vms)
  - [Azure VM Sizes and Types](#azure-vm-sizes-and-types)
  - [Availability Sets](#availability-sets)
  - [Azure Virtual Machine Scale Sets (VMSS)](#azure-virtual-machine-scale-sets-vmss)
  - [Azure Container Instances (ACI)](#azure-container-instances-aci)
  - [Azure App Service](#azure-app-service)
  - [Azure Functions](#azure-functions)
  - [Azure Logic Apps](#azure-logic-apps)
  - [Azure Batch](#azure-batch)
  - [Azure Managed Kubernetes Service (AKS)](#azure-managed-kubernetes-service-aks)
  - [Azure Container Registry](#azure-container-registry)
  - [Azure Service Fabric](#azure-service-fabric)
  - [Azure Batch AI](#azure-batch-ai)
  - [Azure Batch HPC](#azure-batch-hpc)
  - [Azure Autoscaling](#azure-autoscaling)
  - [Azure virtual networks (VNet)](#azure-virtual-networks-vnet)
  - [Subnets](#subnets)

## Azure Active Directory (Azure AD)

Azure AD is a cloud-based identity and access management service provided by Microsoft Azure. It serves as the foundation for managing user identities and controlling access to Azure resources. Azure AD allows you to create and manage user accounts, groups, and guest accounts. With Azure AD, you can implement single sign-on (SSO) for seamless access to various applications and services. It also provides features like Multi-Factor Authentication (MFA) for enhanced security.

## Azure AD Connect

Azure AD Connect is a tool that enables synchronization between an organization's on-premises Active Directory and Azure AD. It ensures that user accounts, groups, and attributes from the on-premises directory are replicated to Azure AD. Azure AD Connect supports different synchronization options, including password hash synchronization, pass-through authentication, and federated authentication. By using Azure AD Connect, organizations can maintain a unified identity management experience across their on-premises and Azure environments.

## Azure AD Roles and RBAC

Role-Based Access Control (RBAC) is a vital component of Azure's security model. RBAC allows you to assign specific roles to users or groups, granting them the necessary permissions to manage Azure resources. Azure provides a set of built-in roles with different levels of access, such as Owner, Contributor, and Reader. Additionally, you can create custom roles to meet specific requirements. RBAC ensures that users have the right level of access to perform their tasks while maintaining security and governance.

## Azure AD Privileged Identity Management (PIM)

PIM is a service within Azure AD that helps organizations manage and control access to privileged roles. Privileged roles have broad access to Azure resources and need to be carefully monitored and controlled. PIM enables just-in-time (JIT) access, allowing users to acquire elevated access for a limited period when needed. It reduces the risk of prolonged exposure to privileged roles and enhances security by providing time-bound assignments and approval workflows.

## Azure AD Conditional Access

Conditional Access in Azure AD allows you to define policies that enforce specific controls based on various conditions. These policies help protect your Azure resources and data by requiring additional authentication or applying access restrictions under specific circumstances. For example, you can configure policies that enforce multi-factor authentication (MFA) for specific applications, restrict access based on device compliance, or enforce geographic restrictions. Conditional Access policies provide granular control over access and enhance security by ensuring that only authorized users can access Azure resources.

## Azure Policy

Azure Policy is a service that allows organizations to enforce compliance and governance within their Azure environments. Azure Policy enables you to define and assign policies that specify rules and guidelines for resource configurations. Policies can enforce specific compliance standards, such as requiring specific tags on resources, prohibiting certain resource types, or enforcing encryption for storage accounts. Azure Policy evaluates resources for compliance and provides insights into non-compliant resources. It helps organizations maintain consistency, security, and governance across their Azure deployments.

## Azure Blueprints

Azure Blueprints provide a way to create reusable, governed Azure environments. A blueprint is a declarative definition of an environment that includes resource groups, policies, role assignments, and more. With Azure Blueprints, organizations can define a standard set of resources and configurations that adhere to their internal standards and compliance requirements. By applying a blueprint, you can rapidly deploy and update environments while ensuring consistency and compliance. Azure Blueprints make it easier to create repeatable deployments and enable governance for Azure resources.

## Azure Storage Accounts

Learn to create and manage Azure storage accounts to store different types of data.

Azure Storage Accounts are a fundamental component of Azure storage. They provide a way to store various types of data such as blobs, files, tables, and queues. By creating and managing storage accounts, you can control access to your data and configure settings to optimize performance and security. Azure Storage Accounts offer different redundancy options to ensure data durability and availability.

## Azure Blob storage

Understand how to store and manage unstructured data in Azure Blob storage.

Azure Blob storage is a service designed to store and manage unstructured data such as images, videos, documents, and backups. It offers a scalable and cost-effective solution for storing large amounts of data. With Blob storage, you can store data in containers and access it from anywhere using HTTP or HTTPS. Blob storage provides different storage tiers, access controls, and security features to meet your specific requirements.

## Azure Files

Explore Azure Files for creating shared file systems accessible from anywhere.

Azure Files provides a fully managed file share solution in the cloud. It allows you to create file shares that can be accessed from anywhere using the standard SMB (Server Message Block) protocol. Azure Files supports both Windows and Linux environments, making it easy to share files across different platforms. It also provides features like snapshots, access control, and Azure Active Directory integration for secure and efficient file sharing.

## Azure Managed Disks

Learn to create and manage managed disks for virtual machines.

Azure Managed Disks simplify the management of disks used by Azure virtual machines. With Managed Disks, you no longer need to worry about managing storage accounts for storing virtual machine disks. You can create, resize, and manage disks directly within the Azure portal or through Azure APIs. Managed Disks provide options for different disk types, performance tiers, and redundancy options, giving you flexibility in configuring storage for your virtual machines.

## Azure Backup

Understand how to configure and manage Azure Backup to protect data and workloads.

Azure Backup is a cloud-based backup service that allows you to protect your data and workloads in Azure. With Azure Backup, you can back up virtual machines, files, and folders, Azure SQL databases, and more. It provides features like automated backups, backup policies, and recovery options to ensure data availability and recoverability. Azure Backup integrates with other Azure services, making it easy to set up and manage data protection for your Azure resources.

## Azure Site Recovery

Discover how to set up disaster recovery for Azure VMs and on-premises workloads.

Azure Site Recovery is a disaster recovery solution that helps protect your applications and data from disruptions caused by planned or unplanned outages. It provides replication and recovery capabilities for Azure virtual machines, Hyper-V virtual machines, and physical servers. Azure Site Recovery enables you to replicate your workloads to a secondary location and automate the failover and failback processes. It helps minimize downtime and provides a reliable solution for business continuity.

## Azure Storage Explorer

Learn to use the Azure Storage Explorer tool for managing storage resources.

Azure Storage Explorer is a standalone application that allows you to easily manage and interact with your Azure storage resources. With Storage Explorer, you can browse and manage blob containers, queues, tables, and files in Azure storage accounts. It provides a user-friendly interface for uploading, downloading, and managing your data. You can also set access control permissions, view storage analytics, and perform other administrative tasks using Storage Explorer.

## Azure File Sync

Explore file synchronization between on-premises servers and Azure Files.

Azure File Sync is a service that enables you to synchronize files between on-premises Windows servers and Azure Files. It provides a centralized location for your files, allowing you to access them from both on-premises servers and Azure virtual machines. Azure File Sync reduces storage costs by tiering less frequently accessed files to Azure Files while keeping frequently accessed files locally. It also provides data synchronization and multi-site collaboration capabilities.

## Azure Blob Storage Lifecycle Management

Understand how to automate the movement and deletion of data.

Azure Blob Storage Lifecycle Management allows you to define rules to automatically manage the lifecycle of your blob data. With lifecycle management, you can transition blobs between different storage tiers or delete them based on their age or other criteria. This feature helps optimize storage costs by automatically moving data to the most cost-effective tier and deleting unnecessary data. You can define lifecycle management rules using Azure portal, PowerShell, or Azure CLI.

## Azure Blob Storage Access Tiers

Learn about different access tiers for optimizing storage costs.

Azure Blob Storage offers different access tiers: hot, cool, and archive. Each tier provides a different level of availability, durability, and cost. Hot access tier is optimized for frequently accessed data, while cool access tier is designed for less frequently accessed data. Archive access tier is for long-term retention and archival of rarely accessed data. By choosing the appropriate access tier for your data, you can optimize storage costs based on the data's usage patterns.

## Azure Shared Access Signatures (SAS)

Understand how to grant limited access permissions to resources using shared access signatures.

Azure Shared Access Signatures (SAS) provide a secure way to grant limited and time-limited access permissions to Azure storage resources. With SAS, you can generate a token that includes specific permissions, expiry time, and other constraints. This token can be shared with others, allowing them to access the specified resources for a limited time and with restricted privileges. SAS can be used to provide temporary access to containers, blobs, queues, or tables, and offers granular control over resource access.

## Azure Data Box

Discover the Azure Data Box service for offline data transfer to Azure.

Azure Data Box is a service that enables offline data transfer to Azure by shipping physical devices to Microsoft for data ingestion into Azure storage. It is useful when you have large amounts of data to transfer and limited network bandwidth. With Azure Data Box, you can transfer terabytes or petabytes of data securely and efficiently. Once the data is ingested into Azure storage, you can access and manage it using other Azure services. Azure Data Box supports multiple types of devices tailored to different data transfer scenarios.

## Deploy and Manage Azure Compute Resources (25-30%)

## Virtual Machines (VMs)

Learn to create, configure, and manage Azure VMs.

Azure Virtual Machines (VMs) provide a scalable and flexible computing environment in the cloud. With Azure VMs, you can create and run virtual machines to host your applications and services. You have full control over the VM's configuration, including operating system, storage, and networking. Azure VMs support both Windows and Linux operating systems, and you can choose from a wide range of VM sizes to meet your performance and resource requirements.

## Azure VM Sizes and Types

Understand different VM sizes and types available in Azure and their use cases.

Azure offers a variety of VM sizes and types to cater to different workloads and performance requirements. VM sizes range from small and economical options to high-performance and memory-intensive instances. Each VM size has a specific combination of CPU, memory, disk, and networking capacity. By choosing the right VM size, you can optimize performance and cost-efficiency for your applications and workloads.

## Availability Sets

Explore availability sets for ensuring high availability of VMs.

Availability sets in Azure are used to ensure high availability and reliability of virtual machines. By distributing VMs across fault domains and update domains, availability sets minimize the impact of hardware or software failures and planned maintenance events. VMs within an availability set are placed in different fault domains to protect against single points of failure. This configuration enables you to achieve higher uptime and fault tolerance for your applications running on Azure VMs.

## Azure Virtual Machine Scale Sets (VMSS)

Learn to deploy and manage scalable sets of VMs.

Azure Virtual Machine Scale Sets (VMSS) allow you to deploy and manage a group of identical VMs that can scale automatically based on demand. VMSS simplifies the management and scaling of VMs, making it ideal for applications that require horizontal scaling. You can define scaling rules based on metrics like CPU utilization or request rate to dynamically increase or decrease the number of VM instances. VMSS provides elasticity and ensures that your application can handle varying workloads efficiently.

## Azure Container Instances (ACI)

Discover how to deploy and manage containers without managing underlying infrastructure.

Azure Container Instances (ACI) is a serverless container solution that allows you to run containers in Azure without the need to manage the underlying infrastructure. With ACI, you can quickly deploy containers and easily scale them based on demand. ACI integrates with other Azure services and provides isolation, security, and pay-per-second billing. It is well-suited for scenarios like batch processing, microservices, and tasks that require on-demand container instances.

## Azure App Service

Understand how to deploy and manage web apps, mobile app backends, and RESTful APIs.

Azure App Service is a fully managed platform for building, deploying, and scaling web, mobile, and RESTful API applications. It supports popular programming languages, frameworks, and runtime environments. With App Service, you can focus on your application code while Azure handles the underlying infrastructure, scaling, and management tasks. App Service offers features like automatic scaling, deployment slots, and integration with Azure DevOps for streamlined application development and deployment.

## Azure Functions

Explore serverless computing with Azure Functions to execute event-driven code.

Azure Functions is a serverless compute service that enables you to run event-driven code without provisioning or managing infrastructure. With Functions, you can write code in multiple languages and execute it in response to various triggers like HTTP requests, timers, and message queues. Functions scale automatically, and you pay only for the execution time of your functions. This makes it suitable for building serverless architectures, microservices, and event-driven workflows.

## Azure Logic Apps

Learn to build and orchestrate workflows using Azure Logic Apps.

Azure Logic Apps is a cloud-based service that allows you to build and automate workflows by connecting various systems, services, and APIs. With Logic Apps, you can create workflows using a visual designer and a rich set of connectors. Logic Apps provide capabilities like conditional branching, looping, and error handling, enabling you to build complex business processes. It integrates well with other Azure services and provides monitoring and diagnostic features for workflow management.

## Azure Batch

Understand how to run large-scale parallel and batch computing jobs with Azure Batch.

Azure Batch is a cloud-based job scheduling service that allows you to run large-scale parallel and batch computing jobs. With Batch, you can scale out to thousands of virtual machines to process data-intensive workloads efficiently. Batch provides features like job and task management, resource provisioning, and automatic scaling. It supports a wide range of applications and can be integrated with other Azure services to build end-to-end solutions for big data processing, rendering, and scientific simulations.

## Azure Managed Kubernetes Service (AKS)

Discover how to deploy and manage Kubernetes clusters on Azure.

Azure Managed Kubernetes Service (AKS) simplifies the deployment, management, and scaling of Kubernetes clusters in Azure. With AKS, you can create a fully managed Kubernetes environment without the need to manage the underlying infrastructure. AKS provides automated updates, scaling, and monitoring for your Kubernetes clusters. It integrates with Azure Active Directory for authentication and authorization and supports popular Kubernetes tools and extensions for container orchestration and management.

## Azure Container Registry

Learn to store and manage container images in Azure.

Azure Container Registry is a private container registry service that allows you to store, manage, and deploy container images. With Container Registry, you can securely store your container images and easily distribute them to your Azure deployments. Container Registry integrates with other Azure services like AKS, Azure Functions, and Azure DevOps, enabling seamless integration and deployment of containerized applications.

## Azure Service Fabric

Explore the Azure Service Fabric platform for building and managing scalable microservices applications.

Azure Service Fabric is a distributed systems platform that simplifies the building, deployment, and management of highly scalable and reliable microservices-based applications. Service Fabric provides capabilities for automatic scaling, rolling upgrades, and fault tolerance. It supports stateful and stateless services, allowing you to build complex applications with ease. Service Fabric can be used for a wide range of applications, including IoT solutions, e-commerce systems, and high-scale web applications.

## Azure Batch AI

Understand how to use Azure Batch AI for running distributed AI workloads.

Azure Batch AI is a service that enables you to run distributed artificial intelligence (AI) and machine learning (ML) workloads at scale. With Batch AI, you can train and infer AI models using parallel processing and GPU acceleration. It integrates with popular AI frameworks and tools like TensorFlow, PyTorch, and Microsoft Cognitive Toolkit. Batch AI provides features for job management, data preparation, and result visualization, making it easier to develop and deploy AI solutions.

## Azure Batch HPC

Discover how to run high-performance computing (HPC) workloads with Azure Batch.

Azure Batch provides capabilities for running high-performance computing (HPC) workloads at scale. With Batch, you can distribute HPC jobs across a pool of virtual machines and leverage parallel processing to accelerate computations. Batch supports popular HPC tools and libraries and provides features for job scheduling, resource management, and data movement. It enables you to achieve faster results and cost-effective HPC solutions by leveraging the power of Azure infrastructure.

## Azure Autoscaling

Learn to configure autoscaling for automatically adjusting resources based on demand.

Azure Autoscaling allows you to dynamically adjust the number of resources allocated to your applications based on workload demand. By configuring autoscaling rules, you can automatically scale up or down resources like virtual machines, containers, or application instances. Autoscaling helps ensure optimal performance, cost-efficiency, and high availability by automatically adjusting resources to match workload fluctuations. It provides flexibility and agility in handling changing demand patterns and can be combined with other Azure services for comprehensive scaling solutions.

## Azure virtual networks (VNet)

Understand the creation and management of virtual networks in Azure.

Azure virtual networks (VNets) are a fundamental networking component in Azure. They provide an isolated and customizable network environment for your Azure resources. With VNets, you can securely connect and control the flow of traffic between your virtual machines, cloud services, and other Azure resources. By creating and managing VNets, you can define IP address ranges, configure network security, and establish connectivity with on-premises networks or other Azure VNets.

## Subnets

Learn about subnets and their role in segmenting virtual networks.

Subnets are subdivisions of a virtual network (VNet) that allow you to segment and organize your network resources. By dividing a VNet into multiple subnets, you can isolate and control network traffic between different groups of resources. Subnets provide logical boundaries within a VNet and help enforce network security and access control. Each subnet has its own IP address range and can be associated with network security groups and route tables to further customize network behavior.


