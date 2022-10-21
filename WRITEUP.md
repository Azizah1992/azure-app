# Write-up Template

### Analyze, choose, and justify the appropriate resource option for deploying the app.

*For **both** a VM or App Service solution for the CMS app:*

Virtual Machine, which is considered as IaaS (Infrastructure as a Service) and the other one is Azure App Service, which is a PaaS (Platform as a Service).

- *Analyze costs, scalability, availability, and workflow*
 
 # costs 
  
    Azure App Service can actually be more expensive as compared to VMs. At time of writing, the Production-level App Service is a Dv2-Series equivalent of Azure VM

    Azure App Service will continue charging even though apps are unused or when stopped.

    VMs are only charged on disk costs when stopped.


 # scalability

    ### In VMs, horizontal scaling is achieved via Scale Sets
     Require separate load balancer If existing VM does not belong to Scale Set, might need a bit of configuration work to enable.

    ### Azure App Service provides an integrated load balancer and can easily increase instances (Just by slider!)

 # availability
    -Azure App Service can be deployed into Availability Zones (AZ) to help you achieve resiliency and reliability for your business-critical workloads. This architecture is also known as zone redundancy.

    -During Virtual Machine creation, availability set is making sure that each VMs inside an availability set are isolated with separate physical servers, compute racks, storage units, and network switches. For example, let we have 3 VMs in an Availability Set. So if one set of physical servers, compute racks, storage units, and network switches of a VM down, resources of other 2 VMs still up and works as they 3 VMs are deployed under separate resources and down of one VM won't impact other VM. 

    

- *Choose the appropriate solution (VM or App Service) for deploying the app*
- *Justify your choice*

### Assess app changes that would change your decision.

*Detail how the app and any other needs would have to change for you to change your decision in the last section.* 
