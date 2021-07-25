## Cost Affecting Factors

- Base Cost
    - **Resource Types** – All Azure services (resources) have resource-specific pricing models. Typically consisting of one or more metrics.
    - **Services** – Azure specific offers (Enterprise, Web Direct, CSP, etc.) have different cost and billing components like prepaids, billing cycles, - discounts, etc.
    - **Location** – running Azure services vary between Azure regions
    - **Bandwidth** – network traffic when uploading (inbound/ingress) data to Azure or downloading (outbound/egress) from Azure
- Savings
    - Reserved Instances
    - Hybrid Benefits

## Azure Reservations

Purchase Azure services for 1 or 3 years in advance with a significant discounts

- **Reserved instances** – Azure Virtual Machines
- **Reserved capacity** – Azure Storage, SQL Database vCores, Databricks DBUs, Cosmos DB RUs
- **Software plans** – Red Hat, Red Hat OpenShift, SUSE Linux, etc.
- **Reservations** are made for 1 or 3 years

## Azure Spot VMs

Purchase unused Virtual Machine capacity for significant discount

- How it works
    - **Significant dicount** for Azure VMs
    - **Capacity** can be **taken away at any time**
    - Customer can **set maximum price** after discount to keep or evict the machine
- **Best for interruptable workloads** (batch processing, dev/test environments, large compute workloads, non-critical tasks, etc.)

## Hybrid use Benefit

Use existing licenses in the cloud

- Use existing licenses in the Azure
    - **Windows Server**
        - Azure VM
    - **RedHat**
        - Azure VM
    - **SUSE Linux**
        - Azure VM
    - **SQL Server**
        - Azure SQL Database
        - Azure SQL Managed Instance
        - Azure SQL Server on VM
        - Azure Data Factory SQL Server Integration Services

## Tools

- **Pricing calculator** – estimate the cost of Azure services
    - Select service
    - Adjust parameters (usage)
    - View the price
- **Total Cost of Ownership (TCO) calculator** – estimate and compare the cost of running workloads in datacenter versus Azure
    - Define your workloads
    - Adjust assumptions
    - View the report

## Azure Cost Management

- A centralized service for reporting usage and billing of Azure environment
- Self-service cost exploration capabilities
- Budgets & alerts
- Cost recommendations
- Automated exports

## Minimizing Costs in Azure

1. Azure Pricing Calculator to choose the low-cost region
    - Good latency
    - All required services are available
    - Data sovereignty/compliance requirements
2. Hybrid use benefit and Azure Reservations
3. Azure Cost Management monitoring, budgets, alerts and recommendations
4. Understand service lifecycle and automate environments
5. Use autoscaling features to your advantage
6. Azure Monitor to find and scale down underutilized resources
7. Use tags & policies for effective governance

## SLA

**Service Level Agreement** (SLA) is a formal agreement between a service provider and a customer.

**SLA** is a **promise** of a service’s **availability** (uptime & connectivity). **Availability** is a measure of time that a service remains operational.

- Each Service has its own SLA
- Ranges from 99% to 99.999%
- Free services typically don’t have an SLA
- Broken SLA means service credit return (discount)

|SLA|Monthly Downtime|
|---|---|
|99%|7h 18m 17s|
|99.5%|3h 39m 8s|
|99.9%|43m 49s|
|99.95%|21m 54s|
|99.99%|4m 22s|
|99.999%|26s|

## Formulas

### Logical AND - adding dependency

Availability of **S1 AND S2** = Availability(S1) * Availability(S2)

### Scenario - Azure website with SQL backend db

- Availability = Availability(web) app * Availability(sql)
- Availability = 99.95% * 99.95%
- Availability = 0.9995 * 0.9995
- Availability = 0.99900025
- Availability ~ 99.9%

### Logical OR - adding redundancy

Availability of **S1 OR S2** = 100% - ( Unvailability(S1) * Unvailability(S2) )

### Scenario - Two redundant web apps behind a load balancer

- Availability(both-web) = 100% - ( Unvailability(web1) * Unvailability(web2) )
- Availability(both-web) = 100% - ( 0.05% * 0.05% )
- Availability(both-web) = 1 – ( 0.0005 * 0.0005 )
- Availability(both-web) = 1 – 0.00000025
- Availability(both-web) = 0.99999975
- Availability(both-web) ~ 99.9999%

## Key Items

- **Formal agreement** between **Microsoft** & the **customer**
- Calculated as a **percentage of service availability** (**uptime** & **connetivity**) (a promise)
- Breaking the SLA provides a discount from the final monthly bill (**Service Credit**)
- **Higher tier** services offer better **SLAs**
- **Free** services typically have **no SLA** (0% SLA)
- **Preview** services have **no SLA**
- **Composite SLA** is a combined SLA of all application components

## Service Lifecycle

- Every service in Azure follows its own service lifecycle
- **Public preview** is a **‘beta’** stage of the service available to general public use
- **Features** can also be in **preview** stages
- Designed for **testing**, **not production** solutions
- **General availability** is a **‘production’** release of the service

## Public Preview Key Info

- No SLA
- Some services have no support coverage
- Limited region availability
- Limited functionality
- Pricing changes
- Direction changes
- Azure Portal Previews ([https://preview.portal.azure.com](https://preview.portal.azure.com/))