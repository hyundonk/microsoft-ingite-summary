# microsoft-ingite-summary



### KeyNote from Satya

- Azure for all workloads
- Azure is world's computer
- Azure Arc - Azure is world 
  - AKS enabled by Azure Arc
- Azure VMs - Ampere Altra Arm-based processors
- **Azure Premium SSD v2 Disk**
- Azure Elastic SAN
- Azure confidential computing (AMD, Intel, NVDIA)
  - Azure Virtual Desktop, AKS worker nodes, SQL server
- **Azure Managed Confidential Consortium Framework** (Preview)
- Microsoft Intelligent Data Platform - A complete data platform
  - 59% savings
  - Azure Cosmos DB for PostgreSQL
  - Azure Synapse Analytics
  - Azure Synapse Link 
  - Azure Synapse Data Explorer
  - Purview - Unified data governance, Risk and Compliance
- Delivering efficiency with AI 
  - Microsoft AI model - Best in the industry - Model traininig , inferencing
    - Turing (Rich language understanding)
    - Z-Code (100 language translation)
    - Florence (Visual recognition)
  - Azure OpenAI Service (with Sam Altman, CO-founder and CEO OpenAI)
    - GPT - human-like language generation
    - DALL-E  2 - Realistic Image Generation
    - Codex - Advanced code generation
  - Azure Machine Learning
  - Azure Container for PyTorc
  - Responsible AI Dashboard
  - Microsoft Designer
  - GitHub co-pilot Labs - 
- Power Platform - Low code/No code
  - Power Apps
  - Natural language to cloud flow in Power Automate
  - AI Builder enhancements
  - Microsoft Syntex for Process automation
    - automatic classification, summarization and translation
    - Content assembly, advanced search, e-signature
    - Archiving , backup, and security management
- Microsoft 365 - Re-energizing your workforce
  - Microsoft Teams Premium
- AKS Updates
  - The # of nodes increase to 5K (SLA required)
  - Pod Identity has been replaced with Workload Identity
  - New Azure CNI with overlay network : increases IP space
- Azure Private Resolver GA
- IP Protection - DDoS protection per IP



### Inside Azure Innovations - Mark Russinovich

- Two phase liquid immersion
  - 1/8 failure rate of air cooled
  - Overclocking up to 20%
  - 1.02 PUE with two phase immersion (5~15 reduced power consumption)
  - Waterless technology
- Azure hosts upgrades with limited VM distuption
  - VM-PHU: > 30s
  - Live migration 13s
  - Hot patch < 20ms (Host OS and Hypervisor)
  - Microcode update (firmware) - No distruption
  - **Hipervisor Hot Restart** < 1s (Hot patch를 할 수 없는 경우. 같은 HW에 새로운 Hypervisor를 메모리에 생성 )
- **Accelerated offload**  - 
  - Storage IO offload using FPGA with existing networking offload
  - Ebsv5 VM size
    - 2x more storage performance (260K IOPS, 8,000 MB/s, 100 Gbps network throughput) than previous Ebsv5
- Sirius technology - Offload SDN policies evaluation to disaggregated appliance
- **Cloud Block Storage as a SAN**
- Azure Container Instances
  - warm pool -> create 1000s of containers in 30ms~10s rather than several minutes.
  - Resource Central triggered/User triggered
- Confidential Computing
  - Confidential inference
- Quantum Computing
  - Topological qubits (majorana fermions) 
    - Reliable, Speed, Size
    - https://aka.ms/azurequantum



### Accelerate your SAN migration to the cloud

#### SAN의 특징

- low Cost: Storage Appliance의 throughput을 SAN에 있는 모든 volume이 공유 -> Stable throughput (Cloud의 기존 block storage solution은 volume마다 dedicated throughput을 지)
- SAN Migration project에서 각각의 volume별로 sizing을 할 필요가 없음. Migration 속도를 높일 수 있음

#### Azure Elastic SAN

- Millions of IOPS (2M IOPS, 32GBps throughput on preview)
- iSCSI
- Customer scenario
  - Consolidate storage volumes
  - Different compute options
  - Higher storage throughput
- SAN resource의 throughput을 모든 volume이 공유
- 요구하는 성능에 따라 base unit 을 값을 정하고 추가 필요한 capacity unit을 추가.
- 1 base unit: 1TB, 5k IOPS, 80 MB/s vs 1 capacity unit: 1TB
- Up to 20 volume groups
- Roadmap
  - New use cases
  - Performance & Scale
  - Service Management/Security Management
  - Backup/DR

[Azure Elastic SAN in preview - Microsoft Community Hub](https://techcommunity.microsoft.com/t5/azure-storage-blog/azure-elastic-san-in-preview/ba-p/3643414)





[Automated cloud application testing with Azure and Playwright (microsoft.com)](https://ignite.microsoft.com/en-US/sessions/ea19c293-7d8a-4218-8203-5af9528a091b?source=sessions)



[DevSecOps: A foundational component for effective Cloud Native security (microsoft.com)](https://ignite.microsoft.com/en-US/sessions/418befd8-a7ee-4f46-a6a8-8b522b120135)

- Why DevSecOps? -> Customer Challenge
  - Fragmented Visibility on DevOps pipelines, compute instances
  - Silo DevOps and Security
  - Shift Left
  - Need code to cloud protection
- Microsoft Defender for Cloud
  - Can view runtime assets alongside DevOps Inventory	
    - Automated discovery of DevOps repositories. using connectors to source code management system.
    - Continuous assessment
    - Security insights

[Implementing Effective DevSecOps for Azure (microsoft.com)](https://ignite.microsoft.com/en-US/sessions/6bc7f188-2a15-42ea-99e3-31ff528be894) by Palo Alto



[Make building cloud native solutions a breeze with visual studio code, GitHub and Azure container apps (microsoft.com)](https://ignite.microsoft.com/en-US/sessions/3ab3e57a-1cdb-428a-acbd-048a2d83da4c?source=sessions)

[Making cloud native easier: Architecting the next-gen Azure PaaS (microsoft.com)](https://ignite.microsoft.com/en-US/sessions/e3840983-765b-43e6-a558-685dc93df21d?source=sessions)

[Making cloud native easier: Architecting the next-gen Azure PaaS (microsoft.com)](https://ignite.microsoft.com/en-US/sessions/e3840983-765b-43e6-a558-685dc93df21d?source=sessions)

[Deep dive into Dapr.io and Cloud Native Architectures (microsoft.com)](https://ignite.microsoft.com/en-US/sessions/0a1cf385-2cca-4cdf-89da-af49b86cf0de?source=sessions)



### Azure Managed Confidential Consortium Framework

- open-source framework leveraging the isolation and attestation capabilities of Trusted Execution Environments like those provided by [Azure confidential computing](https://azure.microsoft.com/solutions/confidential-compute/). 
- decouples node provisioning and operation from network and application governance, making it possible for the solution provider to maintain the set of nodes executing the transactions, without having any access to their contents. Network governance on the other hand, for example, deciding what code to execute, is entirely driven by a consortium, is rule-based, and is programmable and auditable to all participants through an immutable verifiable history. In addition, the immutable history is produced by and resides on the network to support non-repudiation and transparency of participant transactions, through the emission of offline-verifiable receipts. 



### [Announcing Azure Deployment Environments preview (microsoft.com)](https://techcommunity.microsoft.com/t5/apps-on-azure-blog/announcing-azure-deployment-environments-preview/ba-p/3650223)



















