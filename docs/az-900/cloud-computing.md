# Cloud Computing

## Basics

Service delivery model over the internet (cloud). This includes but is not limited to

- **compute power** meaning servers such as Windows, Linux, hosting environments, etc.
- **storage** like files and/or databases
- **networking** in azure but also outside when connecting to your company network
- **analytics** services for visualization and telemetry data

## Key concepts

- **scalability** is the ability to scale, so allocate and de-allocate resources at any time
- **elasticity** is the ability to scale dynamically
- **agility** is the ability to react fast (scale quickly)
- **fault tolerance** is the ability to maintain system up-time while physical and service component failures happen
- **disaster recovery** is the process and design principle which allows a system to recovers from natural or human-induced disasters
- **high availability** is the agreed level of operational up-time for the system. It is a simple calculation of system up-time versus the whole lifetime of the system.
    - availability = up-time/(up-time + downtime)

## Economies of Scale

The principle of economies of scale states that as the companies grow they become more effective at managing shared operations. Be that HR and hiring, taxes, accounting, internal operations, marketing, big purchases via contracts meaning better discounts, etc., etc.

Because of those, companies can save/earn more which in return allows for a reduction in the cost of their services to their customers. This is the so-called ‘price per unit.

It’s not possible to go to 0 because, in the end, some underlying infrastructure needs to run to provide the services. But the larger the scale the more benefits can be passed to customers.

In fact, at the current scale, Microsoft can already offer multiple services for free due to how small a fraction of the cost it is for them.

## Consumption-based model

The consumption-based model is a **pricing model** used in the cloud so that customers are only charged **based on their resource usage**.

This model is characterized by

- **No associated upfront cost**
- **No wasted resources** as such *no charges are incurred for unused resources*. Unused in this case is different per service. For instance, blob storage that stores any data is considered to be used, as it consumes the storage space. Virtual Machines that are running consume CPU, memory, and other resources even if there isn’t any traffic. Hence they are considered to be used and will incur charges.
- **Pay for what you need**
- **Stop paying when you don’t**

**Consumption** is the virtual metric used to calculate how much each resource (service) in Azure was used. Each service has many smaller metrics that track its consumption to offer the best possible pricing model. Those metrics are tracked on a very granular level.

## CapEx vs OpEx

Differences between Capital Expenditure and Operational Expenditure


||Capital Expenditure|Operational Expenditure|
|---|---|---|
|Up front cost|Significant|None|
|Ongoing cost|Low|Based on usage|
|Tax Deduction|Over time|Same year|
|Early Termination|No|Anytime|
|Maintenance|Significant|Low|
|Value over time|Lowers|No change|

## Service Models responsibilities

**As a service** means which party will manage the particular layer and all the layers below.

- The **Software** layer consists of the application (application code and set) & the application data
- **Platform** layer means all the supporting software and the operating system required to host the application
- The **Infrastructure** layer consists of hardware the infrastructure and virtualization required to host the platform

|Layer|Layer|
|---|---|
|Application|Software|
|Data|Software|
|Runtime|Platform|
|Middleware|Platform|
|Operating System|Platform|
|Virtualization|Infrastructure|
|Servers|Infrastructure|
|Networking|Infrastructure|
|Storage|Infrastructure|

## Responsibility Matrix

As such following table represents the responsibilities

|Layer|	On-Premises|	IaaS|	PaaS|	SaaS|
|---|---|---|---|---|
|Application|You|You|You|Cloud provider|
|Data|You|You|You|Cloud provider|
|Runtime|You|You|Cloud provider|Cloud provider|
|Middleware|You|You|Cloud provider|Cloud provider|
|Operating System|You|You|Cloud provider|Cloud provider|
|Virtualization|You|Cloud provider|Cloud provider|Cloud provider|
|Servers|You|Cloud provider|Cloud provider|Cloud provider|
|Networking|You|Cloud provider|Cloud provider|Cloud provider|
|Storage|You|Cloud provider|Cloud provider|Cloud provider|

## Cloud Deployment Model

**Cloud Deployment Model** is simple a separation that describes where are the company resources deployed. Whenever this is in a public cloud provider environment or private data center.

The below table presents high-level deployment model separation

|Layer|	Cloud Provider|	Own Datacenter|
|---|---|---|
|Public|✅|✖|
|Hybrid|✅|✅|
|Private|✖|✅|

## Public Cloud

### Key Characteristics

- Everything runs on cloud provider hardware
- No local hardware
- Some services share hardware with other customers

### Advantages

- No CapEx (No initial investment)
- High Availability
- Agility
- Pay as you Go (PAYG) pricing
- No hardware maintenance
- No deep technical skills required

### Disadvantages

- Not all security and compliance policies can be met
- No ownership over the physical infrastructure
- Rare specific scenarios can’t be done

## Private Cloud

### Key Characteristics

- Everything runs on your own datacenter
- Self-service should be provided
- You maintain the hardware

### Advantages

- Can support any scenario
- Total control over security and infrastructure
- Can meet any security and compliance policy

### Disadvantages

- The initial investment is required (CapEx)
- Limited agility constrained by server capacity and team skills
- Very dependent on IT skills & expertise

## Hybrid Cloud

### Key Characteristics

- Combines both Public & Private cloud

### Advantages

- Great flexibility
- You can run any legacy apps in a private cloud
- Can utilize existing infrastructure
- Meet any security& compliance requirements
- Can take advantage of all public cloud benefits

### Disadvantages

- Can be more expensive
- Complicated to manage due to larger landscape
- Most dependent on IT skills & expertise from all three models
