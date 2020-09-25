- [Essential Terms and Test Review](#essential-terms-and-test-review)
  * [Essential Cloud Concepts](#essential-cloud-concepts)
  * [Cloud Architecture Approaches:](#cloud-architecture-approaches-)
  * [Services & Availability](#services---availability)
  * [Hierarchy within Azure](#hierarchy-within-azure)
  * [Computer Resources](#computer-resources)
  * [Azure Storage & Database](#azure-storage---database)
  * [Networking](#networking)
  * [Azure Solutions](#azure-solutions)
  * [AI](#ai)
  * [DevTest Labs](#devtest-labs)
  * [Azure Security & Trust](#azure-security---trust)
  * [Governance & Compliance](#governance---compliance)
  * [Azure Support & Billing](#azure-support---billing)
    + [How to Access Azure](#how-to-access-azure)


## Essential Cloud Concepts
**High availability** - The ability to keep services up and running for long periods of time, with
very little downtime, depending on the service in question.

**Fault tolerance** - The ability to remain up and running even in the event of a component or
service no longer functioning. Typically, redundancy is built into cloud services architecture
so if one component fails, a backup component takes its place.

**Disaster recovery** - The ability to recover from an event which has taken down a cloud
service. Cloud services disaster recovery can happen very quickly with automation and
services being readily available to use.

**Scalability** - The ability to increase or decrease resources for any given workload. You can
add additional resources to service a workload (known as scaling out), or add additional
capabilities to manage an increase in demand to the existing resource (known as scaling up).
Scalability can be done manually.

**Elasticity** - The ability to automatically or dynamically increase or decrease resources as
needed. Elastic resources match the current needs, and resources are added or removed
automatically to meet future needs. A distinction between scalability and elasticity is that
elasticity is done automatically.

**Agility** - The ability to react quickly. Cloud services can allocate and deallocate resources
quickly. They are provided on-demand via self-service, so vast amounts of computing
resources can be provisioned in minutes.

**CapEx** - physical infrastructure costs up front, such as the purchase of computing
hardware.

**OpEx** - no up front costs; pay as you go. Cloud services are usually CapEx for
accounting purposes.
Economies of scale is the ability to reduce costs and gain efficiency when operating at a
larger scale. Cloud providers such as Microsoft, Google, and Amazon are large businesses,
and are able to leverage the benefits of economies of scale, and then pass those benefits on
to their customers.

Three cloud models, ranked in order of control/administration, from most to the least:

- **IaaS** - Infrastructure as a Service. With IaaS, you rent IT infrastructure servers and virtual
  machines (VMs), storage, networks, and operating systems from a cloud provider on a
  pay-as-you-go basis.
- **PaaS** - Platform as a Service provides an environment for building, testing, and
  deploying software applications. The goal of PaaS is to help create an application as
  quickly as possible without having to manage the underlying infrastructure. Examples
  include Azure SQL or WebApps.
- **SaaS** - Software as a Service is software that is centrally hosted and managed for the
  end customer. It allows users to connect to and use cloud-based apps over the internet.
  Common examples are email, calendars, and office tools such as Office 365, Workday,
  or Salesforce.

## Cloud Architecture Approaches:

- **Public** - A public cloud is owned by the cloud services provider. It provides resources
  and services to multiple organizations and users who connect to the cloud service via a
  secure network connection, typically over the internet.

- **Private** - A private cloud is owned and operated by the organization that uses the
  resources from that cloud. They create a cloud environment in their own datacenter and
  provide self-service access to compute resources to users within their organization. The
  organization remains the owner, entirely responsible for the operation of the services
  they provide.

- **Hybrid** - A hybrid cloud combines both public and private clouds, allowing you to run
  your applications in the most appropriate location. An example of a hybrid cloud usage
  scenario would be hosting a website in the public cloud and linking it to a highly secure
  database hosted in a private cloud.

  <br>

## Services & Availability

Azure provides over 100 services that enable you to do everything from running
existing applications on VMs to exploring new software paradigms like AI and
Serverless.

The most commonly used categories of services in Azure:

- Compute
- Networking
- Storage
- Mobile
- Databases
- Web
- Internet of Things
- Big Data
- Artificial Intelligence
- DevOps

Azure divides the world into geographies that are defined by geopolitical boundaries or
country borders.

**Azure geography** - a discrete market typically containing two or more
regions that preserve data residency and compliance boundaries.

Right now there are four geographies:

- Americas
- Europe
- Asia Pacific
- Middle East and Africa

**Region** - a geographical area on the planet containing at least one, but potentially
multiple datacenters that are nearby and networked together with a low-latency network.

Some examples of regions:

- Central US
- East US 2
- West US 2
- West Europe
- France Central

Each of the regions above also have at least three availability zones.

**Availability Zones** - physically separate datacenters within an Azure region. Each Availability Zone is made up of
one or more datacenters equipped with independent power, cooling, and networking.

For even further redundancy, Azure offers region pairs, which is when one region is paired
with another region within the same geography (such as US, Europe, or Asia) at least 300
miles away.

<br>

## Hierarchy within Azure

- **Subscription** - an agreement with Microsoft to use one or more Microsoft cloud platforms
  or services, for which charges accrue based on either a per-user license fee or on cloudbased resource consumption. An organization can have multiple subscriptions.

- **Resource** - a manageable item that is available through Azure. Examples includes virtual
  machines, storage accounts, web apps, databases, and virtual networks.
  A resource group is a logical container that holds related resources for an Azure solution.
  You decide which resources belong in a resource group based on what makes the most
  sense for your organization.

- **Azure Resource Manager** - the deployment and management service for Azure. It
  provides a management layer that enables you to create, update, and delete resources in
  your Azure account.

<br>

## Computer Resources

- **Virtual Machines** - a complete computing solution where you manage and maintain
  everything except the underlying hardware and networking. You pay for VMs on an hourly
  basis, and prices vary depending on the amount of memory and CPUs the VM uses.

- **Scale Sets** are sets of multiple, identical VMs that are created and deleted automatically,
  which provides high availability for services running on these Scale Sets.
  Azure Containers are a modified runtime environment built on top of a host OS that
  executes an application.

Azure supports Docker containers with these two management services:

- **Azure Container Instances (ACI)**. Azure Container Instances (ACI) offers the fastest
  and simplest way to run a container in Azure. You don't have to manage any virtual
  machines or configure any additional services. ACI is a PaaS offering that allows you to
  upload your containers and execute them directly with automatic elastic scale.

- **Azure Kubernetes Service (AKS)**. The task of automating, managing, and interacting
  with a large number of containers is known as orchestration. Azure Kubernetes Service
  (AKS) is a complete orchestration service for containers with distributed architectures
  with multiple containers.

App Services provides a managed platform to host web applications. There are three varieties:

- Web Apps
- Web Apps for Containers
- API Apps

**Azure Functions** is an instance of serverless computing. An Azure Function exists to execute
a single piece of code that performs a single function. You are only charged for the time
required to execute the Ruction code.

<br>

## Azure Storage & Database

**Azure SQL Database** - a relational database based on the latest stable version of the
Microsoft SQL Server database engine which offers a PasS database solution.

**Azure Cosmos DB** is a globally distributed database service. It supports schema-less data
that lets you build highly responsive database that is updated and maintained by users
around the world. Can store JSON.

**Azure PostgreSQL** is an implementation of free, open source distributed database that is
similar in features to Cosmos DB, and supports SQL queries.

**Azure Blob Storage** is an _unstructured_ data solution, allowing it to support thousands of
simultaneous uploads for things like video, log files, and images. Blobs are highly scalable,
and apps work with blobs in much the same way as they work with files on a disk. Store disks.

**Azure Data Lake** allows you to perform analytics on your data usage and prepare reports.
Data Lake is a large repository that stores both structured and unstructured data.

**Azure Files** offers fully managed file shares in the cloud that are accessible via the industry
standard Server Message Block (SMB) protocol. Azure file shares can be mounted
concurrently by cloud or on-premises deployments of Windows, Linux, and macOS.

**Disk storage** provides disks for virtual machines, applications, and other services to access
and use as they need, similar to how they would in on-premises scenarios.

Azure offers three storage tiers for blob object storage:

- **Hot storage tier**: optimized for storing data that is accessed frequently.
- **Cool storage tier**: optimized for data that are infrequently accessed and stored for at
  least 30 days.
- **Archive storage tier:** for data that are rarely accessed and stored for at least 180 days
  with flexible latency requirements.

  <br>

## Networking

**Virtual Network** is to a network what a Virtual Machine is to a computer/server. VNets
allow resources such as Azure Virtual Machines or VM's to securely communicate with each
other, the internet and on-premises networks.

**Azure Load Balancer** ensures that traffic is evenly distributed between redundant systems. It
supports inbound and outbound scenarios, provides low latency and high throughput, and
scales up to millions of flows for all TCP and UDP applications, working at Layer 4 of the OSI.

The **Azure Application Gateway** is a web traffic load balancer that enables you to manage
traffic to web apps. Traditional load balancers operate at the transport layer (OSI layer 4 -
TCP and UDP), routing traffic based on source IP address and port, to a destination IP
address and port. Application Gateways can make routing decisions based on attributes of
an HTTP request - things like a URL path or host headers.

A **VPN Gateway** is a specific type of virtual network gateway that is used to send encrypted
traffic between an Azure virtual network and an on-premises location over the public
Internet.

A **Content Delivery Network** is a distributed network of servers that can deliver web
content close to users. CDN's store cache content on Edge Servers in locations that are close
to users in order to minimize latency.

**Azure Traffic Manager** uses the DNS server that's closest to the user to direct user traffic to a
globally distributed endpoint. This endpoint can be to the region that's closest to your user.

<br>

## Azure Solutions

**Internet of Things** - a collection of Microsoft-managed cloud services that connect, monitor,
and control billions of IoT assets. In simple terms, an IoT solution is made up of one or more
IoT devices that communicate with one or more back-end services hosted in the cloud.
There are two main Azure components that work with IoT devices.

- **IoT Hub** - a PaaS offering that that collects data from your IoT devices. It is managed,
  secure, and offers a relatively easy way to begin building out an IoT solution. IoT Hub
  supports communications both device to the cloud, and from cloud to the device.
- **IoT Central** - a SaaS offering for IoT in Azure. IoT Central reduces the burden and cost
  of developing, managing, and maintaining enterprise-grade IoT solutions. Using IoT
  Central, you don’t have to write code to deploy and monitor connected devices. It
  provides several connections and dashboards that allow for rapid setup.
  Big Data describes analysis of vast amounts of information. Azure offers these solutions:
- **Data Lake Analytics.** Azure Data Lake Analytics is a great visual name, you have a
  massive body of data, a lake that you can perform analytical procedures on. With Azure
  Data Lake Analytics, you can do this without having to manage servers, virtual
  machines, or clusters of computers.
- **Azure HDInsight.** Very similar to Azure Data Lake Analytics, the difference being open
  source frameworks. HDInsights includes products such as Apache Hadoop, which
  allows many computers to work together. It also includes Apache Spark, which is an
  interface to allow parallel program between clusters of computers, and Apache Kafka,
  which allows processing of real time data feeds.
- **Azure Data Bricks.** This is based on Apache Spark, and offers an API layer where a
  wide span of analytic-based languages can be used to work with your data: R, SQL,
  Python, Scala and Java. It is built especially for data engineering and data science.

  <br>

## AI
AI offers the capability of a machine to imitate intelligent human behavior - analyzing
images, comprehending speech, etc.

Azure offers two ways to get started with AI:

- **Azure AI Studio** - a drag and drop interface for designing AI experiments
- **Azure Machine Learning** - the drag and drop interface, plus several extensions that
  allow for integration with existing AI tools and coding
  Serverless computing an extreme version of platform as a service or PaaS. You should be
  familiar with these Serverless computing solutions:
- **Functions.** A Function provides a single instance of functionality that executes a single
  task. There are no servers, no applications, no systems.
- **Logic Apps.** A logic App can schedule, automate and orchestrate tasks, business
  processes and workflows.
- **Event Grid.** Event Grid is a routing service for connected applications that ensure
  events are sent and received fast and accurately
  DevOps is a not a specific solution, but a set of strategies and tools for deploying highquality software into production using CI/CD pipelines.

br>

## DevTest Labs

**Azure DevTest Labs** is an Azure solution that allows developers to efficiently self-manage
virtual machines (VMs) and PaaS resources without waiting for approvals.
You can use DevTest Labs to automate environment creation, which facilitates rapid testing
of new code.

## Azure Security & Trust

**Network Security Groups** - NSGs filter traffic at the network layer using rules that allow or
deny traffic based on what Microsoft calls '5-tuple' information:

1. Protocol – such as TCP, UDP, ICMP
2. Source IP address
3. Source port
4. Destination IP address
5. Destination port

**Application Security Groups (ASGs)** can apply security riles at scale, because an ASG is a
logical grouping of virtual machines.

**Azure Firewall** is a managed service that filters on more levels than the Network Security
Group does. It can filter traffic on OSI layer 3, 4, and 7.

**DDoS Protection** is automatically enabled as part of the Azure platform. It provides alwayson traffic monitoring and real-time mitigation of common network-level attacks, providing
the same defenses utilized by Microsoft's own online services. It’s possible to upgrade DDoS
Protection from Basic to Standard for additional mitigation capabilities

A **User Defined Route** is used to override Azure’s default routing behavior between VNets
and resources. For example, you can use a UDRs to send traffic between two subnets
through a firewall appliance rather than directly between the two subnets.

Two fundamental regarding identity and access control are authentication and
authorization:

- **Authentication** is the process of establishing the identity of a person or service looking
  to access a resource.
- **Authorization** is the process of establishing what level of access an authenticated
  person or service has. It specifies what data they're allowed to access and what they
  can do with it.

**Azure Active Directory (Azure AD)** is Microsoft’s cloud-based identity and access
management service.

**The Azure Security Center** is a monitoring service that provides threat protection across all
of your services both in Azure, and on-premises. It can:

- Provide recommendations based on your configurations, resources, and networks.
- Monitor settings across on-premises and cloud workloads, and automatically apply
  required security to new services as they come online.
- Continuously monitor all your services, and perform automatic security assessments to
  identify potential vulnerabilities
- Use machine learning to detect and block malware from being installed on your virtual
  machines and services.
- Analyze and identify potential inbound attacks.

**Azure Information Protection Service (AIP)** works in conjunction
with Office 365, Microsoft's online productivity suite. Use AIP to classify documents
(including email) according to how sensitive it is. This allows protection of files even when
they are sent outside of your corporate network.
Azure Key Vault allows for secure storage of passwords and other secrets. You can then
share those secrets with others without revealing the actual secret.

**Azure Advanced Threat protection (ATP)** helps monitor users in both cloud and on-prem
environments. ATP analyzes user activity, and alerts admins when users engage in unusual
behavior

<br>

## Governance & Compliance

**Azure Monitor** maximizes the availability and performance of your applications by
delivering a comprehensive solution for collecting, analyzing, and acting on telemetry from
your cloud and on-premises environments.

- **Azure Service Health** is a suite of experiences that provide personalized guidance and
  support when issues with Azure services affect you. Azure Service Health can also help you
  prepare for planned maintenance that could affect the availability of your resources.

**Azure Policy** is a set of rules that define what can be added, and how those things that are
added can be configured. They specify the whats and hows of your Azure implementation.
Initiatives work alongside policies in Azure Policy. An initiative definition is a set or group of
policy definitions to help track your compliance state for a larger goal.

**Role-Based Access Control (RBAC)** lets you define who - i.e. which users are able to access
to specific Azure resources, and what they can do to those resources once they gain access.

**Resource Locks** can be applied to any resource to block modification or deletion. Resource
locks can set to either Delete or Read-only, and can be applied to subscriptions, resource
groups, and to individual resources. Locks are inherited when applied at higher levels.

**Azure Blueprints** enables cloud architects to define a repeatable set of Azure resources that
implements and adheres to an organization's standards, patterns, and requirements.

**Azure Government** delivers a dedicated cloud to government agencies and partners so that
these entities can leverage cloud advantages. Azure Government services handle data that is
subject to certain government regulations and requirements, such as FedRAMP, NIST
800.171 (DIB), ITAR, IRS 1075, DoD L4, and CJIS.

**Azure China** is a physically separated instance located in China. It’s independently operated
by 21ViaNet, and is not connected to any other Azure region. This ensures data complies
with all applicable Chinese laws and regulations.

Azure provides compliance with many industry and governmental regulations, including
these:

- **GDPR** is the General Data Protection Regulation, which forces companies to protect user
  data and provide a way for individuals to manage their data.
- **ISO** is the International Standardization Organization, an independent nongovernmental
  organization and the world’s largest developer of voluntary international standards.
- **NIST** is the National Institute of Standards and Technology, and focuses purely on the tech
  industry, in particular on information security frameworks for US federal agencies.
- **HIPAA** is the Health Information Portability and Accountability Act, a US healthcare law that
  establishes requirements for the use, disclosure, and safeguarding of individually
  identifiable health information.

<br>

## Azure Support & Billing

### How to Access Azure

- **Azure Portal** is a website that lets you manage all of your Azure resources - if you can deploy
  or manage it in Azure, you can do it through the Azure Portal website.

- **Azure Command-Line Interface (Azure CLI)** is a set of commands used to create and
  manage Azure resources. You can use this tool in Windows, macOS, and Linux environments.
  and it can also be run in Docker containers or in the Azure Cloud Shell.

- **Azure PowerShell** is a set of cmdlets for managing Azure resources directly from the
  PowerShell command line. Azure PowerShell provides powerful features for automation.
  Azure PowerShell works with 6.x and higher on all platforms (current version is version 7).

- **Azure Cloud Shell** is an interactive, authenticated, browser-accessible shell for managing
  Azure resources. It provides the flexibility of choosing the shell experience that best suits the
  way you work: either Bash or PowerShell.
  
  ## Cost Management

All Azure resources live within a subscription, which is a unit of billing within an Azure
tenant (account).

**Management Groups** are a unit of subscription management. You can leverage
management groups to take bulk actions across multiple subscriptions. For example,
Management Groups can be used to group subs by department, region, or anything else
that suits the organization needs.

Use **Azure Cost Management** to set budgets, schedule reports, and analyze costs areas This
is a free Azure tool that provides a dashboard for easy visualization of Azure costs.

**Azure Pricing Calculator** allows you to run scenarios that estimate monthly costs for
selected cloud resources.

The **Azure Total Cost of Ownership (TCO) Calculator** generates a report that compares the
costs of your on-premises infrastructure with the costs of using Azure products in the cloud.
