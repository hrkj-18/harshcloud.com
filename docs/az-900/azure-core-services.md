## Data Center

- **Physical facility**
- **Hosting for** a group of networked **servers**
- Own **power**, **cooling** & **networking** infrastructure

## Region

- The g**eographical area** on the planet
- **One but usually more data centers** connected with a **low-latency network** (<2 milliseconds)
- **Location** for your services
- Some services are **available only in certain regions**
- Some services are **global services**, as such are not assigned/deployed in a specific region
- Globally available with **50+ regions**
- Special **government regions** (US DoD Central, US Gov Virginia, etc.)
- Special **partnered regions** (China East, China North)

## Availability Zone

- **Regional feature**
- Grouping of **physically separate** facilities
- Designed to **protect from data center failures**
- If the zone goes down **others continue working**
- Two service **categories**
    - **Zonal** services (Virtual Machines, Disks, etc.)
    - **Zone-redundant** services (SQL, Storage, etc.)
- **Not** **all** regions are **supported**
- The s**upported** region has **three or more zones**
- A **zone** is **one or more data centers**

## Region Pair

- **Each region** is **paired** with another region making it a region pair
- Region **pairs are static** and cannot be chosen
- Each pair resides within the **same geography**
    - The exception is Brazil South
- **Physical isolation** with at least 300 miles distance (when possible)
- Some services have **platform-provided replication**
- **Planned updates** across the pairs
- **Data residency** maintained for disaster recovery

|Region Pair A|Region Pair B|
|---|---|
|East US|West US|
|UK West|UK South|
|North Europe (Ireland)|West Europe (Netherlands)|
|East Asia (Hong Kong)|Southeast Asia (Singapore)|

## Geographies

- **Discrete market**
- Typically **contains two or more regions**
- Ensures **data residency**, **sovereignty**, **resiliency**, and **compliance** requirements are met
- **Fault-tolerant** to protect from region-wide failures
- Broken up into areas
    - **Americas**,
    - **Europe**,
    - The **Asia Pacific**,
    - The **Middle** **East** and **Africa**
- Each **region belongs only to one Geography**

## Azure Resource

- The object **used to manage services** in Azure
- Represents **service lifecycle**
- Saved as **JSON definition**

## Resource Groups

- **Grouping** of resources
- Holds **logically related** resources
- Typically organizing by
    - **Type**
    - **Lifecycle** (app, environment)
    - **Department**
    - **Billing**,
    - **Location** or
    - **combination of those**

## Resource Manager

- **Management Layer** for all resources and resource groups
- **Unified** language
- **Controls** **access** and **resources**

## Additional Info

- Each **resource must** be in one, and **only one resource group**
- Resource **groups have their own location** assigned
- Resources in the resource groups **can reside in different locations**
- Resources **can be moved** between the resource groups
- Resource **groups can’t be nested**
- Organize based on your organization needs but consider
    - Billing
    - Security and access management
    - Application Lifecycle

## Virtualization

- Emulation of physical machines
- Different virtual hardware configurations per machine/app
- Different operating systems per machine/app
- Total separation of environments
    - file systems,
    - services,
    - ports,
    - middleware,
    - configuration

## Virtual Machines

- Infrastructure as a Service (IaaS)
- Total control over the operating system and the software
- Supports marketplace and custom images
- Best suited for
    - Custom software requiring custom system configuration
    - Lift-and-shift scenarios
- Can run any application/scenario
    - web-apps & web services,
    - databases,
    - desktop applications,
    - jump boxes,
    - gateways, etc.

## Virtual Machine Scale Sets

- Infrastructure as a Service (IaaS)
- Set of identical virtual machines
- Built-in auto-scaling features
- Designed for manual and auto-scaled workloads like web services,* batch processing, etc.

## Containers

- Use host’s operating system
- Emulate operating system (VMs emulate hardware)
- Lightweight (no O/S)
    - Development Effort
    - Maintenance
    - Compute & storage requirements
- Respond quicker to demand changes
- Designed for almost any scenario

## Azure Container Instances

- The simplest and fastest way to run a container in Azure
- Platform as a Service
- Serverless Containers
- Designed for
    - Small and simple web apps/services
    - Background jobs
    - Scheduled scripts

## Azure Kubernetes Service (AKS)

- The open-source container orchestration platform
- Platform as a Service
- Highly scalable and customizable
- Designed for high scale container deployments (anything really!)

## App Service

- Designed as enterprise-grade web application service
- Platform as a Service
- Supports multiple programming languages and containers

## Azure Functions (Function Apps)

- Platform as a Service
- Serverless
- Two hosting/pricing models
    - Consumption-based plan
    - Dedicated plan
- Designed for micro/nano-services

## Summary

- Virtual Machines (IaaS) - Custom software, custom requirements, very specialized, high degree of control
- VM Scale Sets (IaaS) - Auto-scaled workloads for VMs
- Container Instances (PaaS) - Simple container hosting, easy to start
- Kubernetes Service (PaaS) - Highly scalable and customizable * container hosting platform
- App Services (PaaS) - Web applications, a lot of enterprise web * hosting features, easy to start
- Functions (PaaS) (Function as a Service) (Serverless) - micro/nano-services, excellent consumption-based pricing, easy to start

## Azure Networking

- Connect cloud and on-premises
- On-premise networking functionality

## Azure Virtual Network

- Logically isolated networking components
- Segmented into one or more subnets
- Subnets are discrete sections
- Enable communication of resources with each other, internet and on-premises
- Scoped to a single region
- VNet peering allows cross-region communication
- Isolation, Segmentation, Communication, Filtering, Routing

## Azure Load Balancer

- Even traffic distribution
- Supports both inbound and outbound scenarios
- High-availability scenarios
- Both TCP (transmission control protocol) and UDP (user datagram protocol) applications
- Internal and External traffic
- Port Forwarding
- High scale with up to millions of flows

## VPN Gateway

- The specific type of virtual network gateway for on-premises to azure traffic over the public internet

## Application Gateway

- Web traffic load balancer
- Web application firewall
- Redirection
- Session affinity
- URL Routing
- SSL termination

## Content Delivery Network

- Define content
- Minimize latency
- POP (points of presence) with many locations

## Data Types

- Structured - Data that can be represented using tables with very strict schema. Each row must follow a defined schema. Some tables have defined relationships between them. Typically used in relational databases.
- Semi-structured - Data that can be represented using tables but without a strictly defined schema. Rows must only have a unique key identifier.
- Unstructured - Any files in any format. Like binary files, application files, images, movies, etc.

## Storage Account

- Group of services which include
    - blob storage,
    - queue storage,
    - table storage, and
    - file storage
- Used to store
    - files,
    - messages, and
    - semi-structured data
- Highly scalable (up to petabytes of data)
- Highly durable (99.999999999% - 11 nines, up to 16 nines)
- Cheapest per GB storage

## Blob Storage

- BLOB – binary large object – file
- Designed for storage of files of any kind
- Three storage tiers
    - Hot – frequently accessed data
    - Cool – infrequently accessed data (lower availability, high durability)
    - Archive – rarely (if ever) accessed data

## Queue Storage

- Storage for small pieces of data (messages)
- Designed for scalable asynchronous processing

## Table Storage

- Storage for semi-structured data (NoSQL)
    - No need for foreign joins, foreign keys, relationships, or strict schema
    - Designed for fast access
- Many programming interfaces and SDKs

## File Storage

- Storage for files accessed via shared drive protocols
- Designed to extend on-premise file shares or implement lift-and-shift scenarios

## Disk Storage

- Disk emulation in the cloud
- Persistent storage for Virtual Machines
- Different
    - sizes,
    - types (SSD, HDD)
    - performance tiers
- The disk can be unmanaged or managed

## Data Types

- **Structured** - Data that can be represented using tables with very strict schema. Each row must follow a defined schema. Some tables have defined relationships between them. Typically used in relational databases.
- **Semi-structured** - Data that can be represented using tables but without a strictly defined schema. Rows must only have a unique key identifier.
- **Unstructured** - Any files in any format. Like binary files, application files, images, movies, etc.

## Cosmos DB

- Globally distributed NoSQL (semi-structured data) Database service
- Schema-less
- Multiple APIs (SQL, MongoDB, Cassandra, Gremlin, Table Storage)
- Designed for
    - Highly responsive (real-time) applications with super-low latency responses <10ms
    - Multi-regional applications

## SQL Database

- **Relational database** service in the cloud (PaaS) (DBaaS - Database as a Service)
- **Structured data service** defined using schema and relationships
- **Rich Query Capabilitie**s (SQL)
- **High-performance**, reliable, fully managed, and secure database for building - applications

## Azure SQL product family

- Azure **SQL Database** – Reliable relational database based on SQL Server
- Azure **Database for MySQL** – Azure SQL version for MySQL database engine
- Azure **Database for PostgreSQL** – Azure SQL version for PostgreSQL database engine
- Azure **SQL Managed Instance** – Fully-fledged SQL Server managed by the cloud provider
- Azure **SQL on VM** – Fully-fledged SQL Server on IaaS
- Azure **SQL DW (Synapse)** – Massively Parallel Processing (MPP) version of SQL Server

## Azure Marketplace

- Think of it like an “Azure Shop” where you purchase services and solutions for the Azure platform
- Each product is a template that contains one or multiple services
- Products are delivered by first and third-party vendors
- Solutions can leverage all service categories like IaaS, PaaS, and SaaS

## Internet of Things

Internet of Things (**IoT**) is a network of internet-connected devices (**IoT Devices**) embedded in everyday objects enabling sending and receiving data such as **settings** and **telemetry**.

## Azure IoT Hub

- Managed service for bi-directional communication
- Platform as a Service (PaaS)
- Highly secure, scalable, and reliable
- Integrates with a lot of Azure Services
- Programmable SDKs for popular languages (C, C##, Java, Python, Node.js)
- Multiple protocols (HTTPS, AMQP, MQTT)

## Azure IoT Central

- IoT App Platform - Software as a Service (SaaS)
- Industry-specific app templates
- No deep technical knowledge required
- Service for connecting, management, and monitoring IoT devices
- Highly secure, scalable, and reliable
- Built on top of the IoT Hub service and 30+ other services

## Azure Sphere

- Secure end-2-end IoT Solutions
    - Azure Sphere certified chips (microcontroller units - MCUs)
    - Azure Sphere OS based on Linux
    - Azure Security Service trusted device-to-cloud communication

## Big Data

**Big Data** is a field of technology that helps with the **extraction**, **processing** and **analysis** of information that is **too large or complex** to be dealt with by traditional software.

## The three V’s rule

Big data typically has one of the following characteristics

- **Velocity** - how fast the data is coming in or how fast we are processing it
    - Batch
    - Periodic
    - Near Real-Time
    - Real-Time
- **Volume** - how much data we are processing
    - Megabytes
    - Gigabyte
    - Terabytes
    - Petabytes
- **Variety** - how structured/complex the data is
    - Tables
    - Databases
    - Photo, Audio
    - Video, Social Media

## Azure Synapse Analytics

- Big data analytics platform (PaaS)
- Multiple components
    - Spark
    - Synapse SQL
        - SQL pools (dedicated – pay for provisioned performance)
        - SQL on-demand (ad-hoc – pay for TB processed)
    - Synapse Pipelines (Data Factory – ETL)
    - Studio (unified experience)

## Azure HDInsight

- Flexible multi-purpose big data platform (PaaS)
- Multiple technologies supported (Hadoop, Spark, Kafka, HBase, Hive, Storm, Machine Learning)

## Azure Databricks

- Big data collaboration platform (PaaS)
- Unified workspace for notebook, cluster, data, access management, and collaboration
- Based on Apache Spark
- Integrates very well with common Azure data services

## Artificial Intelligence

**Artificial Intelligence** (**AI**) is the simulation of human intelligence & capabilities by computer software.

## Machine Learning

**Machine Learning** is a subcategory of AI where computer software is “**taught**” to **draw conclusions** and **make predictions** **from data**.

## Azure Machine Learning

- Cloud-based platform for creating, managing, and publishing machine learning models
- Platform as a Service (PaaS)
- Machine Learning Workspace – top-level resource
- Machine Learning Studio – web portal for end-2-end development
- Features
    - Notebooks – using Python and R
    - Automated ML – run multiple algorithms/parameters combinations, choose the best model
    - Designer – graphical interface for no-code development
    - Data & Compute – management of storage and compute resources
    - Pipelines – orchestrate model training, deployment, and management tasks

## Serverless

**Serverless computing** is a cloud-hosted execution environment that allows customers to **run their applications** in the cloud while **completely abstracting underlying infrastructure**.

## Azure Functions

- Serverless coding platform (Functions as a Service, FaaS)
- Designed for nano-service architectures and event-based applications
- Scales up and down very quickly
- Highly scalable
- Supports popular languages and frameworks (.NET & .NET Core, Java, Node.js, Python, PowerShell, etc.)

## Azure Logic Apps

- Serverless enterprise integration service (PaaS)
- 200+ connectors for popular services
- Designed for orchestration of
    - business processes,
    - integration workflows for applications, data, systems, and services
- No-code solution

## Azure Event Grid

- Fully managed serverless event routing service
- Uses publish-subscribe model
- Designed for event-based and near-real-time applications
- Supports dozen of built-in events from most common Azure services

## DevOps

**DevOps** is a set of practices that combine both development (**Dev**) and operations (**Ops**).

DevOps aims to **shorten the development life cycle** by providing **continuous integration** and **delivery** (CI/CD) capabilities while **ensuring high quality** of deliverables.

## Azure DevOps

- **Collection of services** for building solutions using DevOps practices
- Services included
    - **Boards** – tracking work
    - **Pipelines** – building CI/CD workflows (build, test and deploy apps)
    - **Repos** – code collaboration and versioning with Git
    - **Test Plans** – manual and exploratory testing
    - **Artifacts** – manage project deliverables
- Extensible with **Marketplace** – over 1000 available apps
- Evolved from **TFS** (Team Foundation Server), through **VSTS** (Visual Studio Team Services)

## Azure DevTest Labs

- Service for creation of **sandbox environments** for developers/testers (PaaS)
- Quick setup of **self-managed virtual machines**
- **Preconfigured templates** for VMs
- Plenty of additional **artifacts** (tools, apps, custom actions)
- Lab **policies** (quotas, sizes, auto-shutdowns)
- **Share** and **automate** labs via custom images
- Premade plugins/API/tools for **CI/CD pipeline automation**

## Azure Portal

- Public web-based interface for management of Azure platform
- Designed for self-service
- Customizable
- Simple tasks

## Azure PowerShell

- PowerShell and module
- Designed for automation
- Multi-platform with PowerShell Core
- Simple to use
    - Connect-AzAccount – log into Azure
    - Get-AzResourceGroup – list resource groups
    - New-AzResourceGroup – create a new resource group
    - New-AzVm – create a virtual machine

## Azure CLI

- Command Line Interface for Azure
- Designed for automation
- Multi-platform (Python)
- Simple to use
    - az login – log into Azure
    - az group list – list resource groups
    - az group create – create a new resource group
    - az vm create – create a virtual machine
- Native OS terminal scripting

## Azure Cloud Shell

- Cloud-based scripting environment
- Completely free
- Supports both Azure PowerShell and Azure CLI
- Dozen of additional tools
- Multiple client interfaces
    - Azure Portal integration (portal.azure.com)
    - Shell Portal (shell.azure.com)
    - Visual Studio Code Extension
    - Windows Terminal
    - Azure Mobile App
    - Microsoft Docs integration

## Azure Advisor

- **Personalized consultant** service
- Designed to provide **recommendations** and **best practices** for
    - **Cost** (SKU sizes, idle services, reserved instances, etc.)
    - **Security** (MFA settings, vulnerability settings, agent installations, etc.)
    - **Reliability** (redundancy settings, soft delete on blobs, etc.)
    - **Performance** (SKU sizes, SDK versions, IO throttling, etc.)
    - **Operational** Excellence (service health, subscription limits, etc.)
- **Actionable** recommendations
- **Free**!