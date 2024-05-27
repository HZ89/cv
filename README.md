# Resume Of Hui Peng Zhu

- Topic: Devops Golang Kubernetes Containers Automation Machine Learning Platform

## About Me

- Hui Peng Zhu
- 1989-06 ～ Now
- Years Of Experience: 12 years
- Github: [Hz89](https://github.com/Hz89)
- Desired Position: Infrastructure Develop/Devops Engineer/SRE
- Desired City: Singapore
- Email: wcg6121@gmail.com
- Current Status: Employed
- Education：Associate Degree

## Skills List

- Programming Languages: Golang, Python
- Version Control: Git (Gitlab, Github, Gitea)
- CI/CD: [Drone](https://github.com/drone/drone), Jenkins
- Databases: MySQL, TiDB, TiKV, Codis, Redis
- Methodologies: Devops
- IaC: [Terraform](https://github.com/hashicorp/terraform), [RKE](https://github.com/rancher/rke)
- Infrastructure: Kubernetes, OVS/OVN, Fannel, Calico, RoCE, IB, IPoIB
- Container Tech: RKT, Docker
- Ops: LNMP, Linux Kernel Parameter, MySQL, CEPH, Docker, Kubernetes
- OS: CentOS 6/7, CoreOS, Ubuntu 16.04
- Cloud Platform: AWS, Alicloud, using Golang SDK for development on each platform. Familiar with the network characteristics, user management systems, and hybrid cloud design of each platform.

## Project Experience

### Tencent

- Tencent Cloud [EKS](https://cloud.tencent.com/document/product/457/39804)
  - Responsible for EKS 1.0 ~ 1.5 ~ 2.0 architecture design and core code development
  - Responsible for project pipeline construction and development specification implementation
  - Responsible for Windows containers

- EKS OS Development
  - Specially customized Linux distribution for EKS scenarios, focusing on improving startup speed

- CSI on nodeless Kubernetes
  - Due to the strong dependency on nodes in the design of CSI, it cannot be used in nodeless Kubernetes like EKS. Designed an implementation compatible with existing CSI user interfaces.

### Momenta

#### MOPS K8s Multi-Cluster Management Platform

- Custom development based on the 360 open-source [Wayne](https://github.com/Qihoo360/wayne) project
  - Ingress-related functions
  - Integrated with Alibaba Cloud for automatic domain name resolution
  - Existing cluster import function

#### Jenkins CI Platform

- Jenkins + Kubernetes provides Jenkins build clusters
- Solved Jenkins agent compilation cache using shared storage

#### Goslurm Deep Learning Scheduling Platform

- CLI compatible with [Slurm](https://www.schedmd.com/), reducing migration costs for traditional HPC ecosystem users
- Task scheduling based on K8s, using a custom scheduler
- Compatible with common frameworks like `Caffe2`, `TensorFlow`, `PyTorch`, using corresponding K8s operators
- Hybrid deployment of cloud and on-premises environments, multi-cluster scheduling
- Automatic scaling in cloud environments using AWS ASG
- Automatic cluster deployment (Terraform + RKE)
- Supports heterogeneous network environment scheduling with Ethernet and RDMA networks

#### Hive Training Dataset Management System

- Multi-version control of training sets. Integrated with AWS S3, Alibaba Cloud OSS, and other backend storage
- Git-like operation interface for users
- Supports version control of training datasets

#### CacheFS Distributed File System for Deep Learning

- Multi-level caching with memory, SSD disk, server-side memory cache
- Implemented P2P cache for multi-node training scenarios
- Storage layer based on `Facebook Haystack` architecture
- Master in storage layer achieves HA through raft
- Access interface layer provides gRPC, HTTP API, and POSIX interface using FUSE
- FUSE implementation supports multiple storage layers AWS S3, Alibaba Cloud OSS, CEPH, and Haystack
- Implemented Kubernetes CSI interface, training tasks mount training sets via PV PVC

### Youzu Interactive

#### UPaaS Private PaaS Platform

Similar to a simplified version of NetEase Honeycomb, includes code hosting and building, image market, elastic computing, cloud disk, etc.

- Responsible for system backend architecture design, technology selection, and backend system development
- Subsystems:
  - CI/CD System: Used `Gogs` git service and `Drone` automated build system for code hosting and automated builds
  - Private Docker Registry: Built a highly available private image hosting system using `VMware Harbor`
  - CEPH Block Storage and Object Storage System: Provided block storage for PaaS platform to implement cloud disk functions, shared storage for git system, and object storage for registry
  - Kubernetes: Provided elastic computing and service scheduling functions
  - `Archon` for managing Kubernetes clusters. Used a shared management cluster to manage each tenant's business cluster.

#### Djob Centralized Cron Job Management & Command Scheduling System

- Responsible for system design, requirements sorting, architecture design, technology selection, and backend development
- Designed functions: Centralized management of cron jobs and support for one-time task distribution, cross-data-center management, task dependencies, task accuracy to the second, and concurrency control of one-time tasks
- Technology stack: Golang, SWIM protocol, TiDB, gRPC, etcd
- Implementation:
  - Used SWIM protocol to form a large cluster of all servers, cluster state maintained by SWIM protocol, real-time small messages distributed by SWIM protocol
  - Logically defined servers as `Server` and `Agent`
  - `Server` responsible for task scheduling, distribution, result collection, message forwarding, and also executing SWIM protocol tasks.
  - `Agent` only runs SWIM protocol and executes specific tasks.
  - gRPC protocol for large packages (greater than 1k) or non-real-time message transmission: `Agent` retrieves specific task information, returns task execution results, etc.
  - Etcd used to synchronize `Server` state. Since SWIM is a weak consistency message, etcd is needed to synchronize the execution status and lock information of each task.

#### CMDB

- Responsible for system design, requirements sorting, and progress control
- Planned to design and develop a CMDB system to manage middleware, operating systems, hardware, network devices, IDC, and all operation-related entities' configuration information, but due to lack of experience and specific requirements, the project fell into describing the configuration of each specific configuration object, ignoring the essence of CMDB, eventually leading to stagnation.

### 17173 Beijing Branch

#### Monitoring System

- Responsible for designing a monitoring system based on `Zabbix` to monitor the status of all servers, middleware, and databases of 173, and alerting
- Customized alert behavior and modes based on `Zabbix`. Developed a set of `Zabbix` alert script library in `Python`. Used `MySQL-TokuDB` as storage. Since Zabbix couldn't handle large amounts of data at that time, split the monitoring system according to business needs, then encapsulated a unified interface to provide services externally.

## Work Experience

- Tiktok (Singapore)
  - Duration: 2022-12 ~ Now
  - Position: SRE
  - Responsibilities: Responsible for TikTok e-commerce stability, K8s cluster high availability, etc.

- Tencent
  - Duration: 2019-08 ~ 2022-12
  - Position: Senior Backend Development Engineer 3.2
  - Responsibilities: Responsible for EKS product architecture design and development, as well as R&D specifications and process formulation.

- Momenta (AI Autonomous Driving)
  - Duration: 2018-02-22 ~ 2019-08
  - Position: Development Engineer
  - Responsibilities: Responsible for ensuring DevOps processes and technical support, and developing deep learning training platforms.

- Youzu Interactive
  - Duration: 2015.03 ~ 2018.01
  - Position: DevOps Development Supervisor/Senior DevOps Engineer (Rehired, leading to position change)
  - Responsibilities: Led the DevOps development team to develop internal automated operation and maintenance systems/Responsible for operation and maintenance technology selection and architecture, promotion of new technologies.
  - Reason for Leaving: Wanted to return to Beijing
  - Summary: A journey from operation and maintenance to DevOps development transformation. Achieved the systems I wanted to build and practiced the latest technologies. The key was meeting a great group of people.

- 17173 Beijing Branch
  - Duration: 2013.09 ~ 2015.03
  - Position: DevOps Development Engineer
  - Responsibilities: Responsible for DevOps system development and some operation and maintenance work.
  - Reason for Leaving: Internal turmoil at Changyou Company
  - Summary: Experienced the best team. Also the starting point for the transition from operation and maintenance to DevOps development.

- Shanghai Jiangyou
  - Duration: 2011.05 ~ 2013.02
  - Position: Operation and Maintenance
  - Responsibilities: All operation and maintenance-related tasks
  - Reason for Leaving: Young and wanted to explore
  - Summary: A small company starting from scratch, exposed to all aspects of operation and maintenance (IDC network construction, IDC selection, server hardware, etc.), broadened horizons.

- The9 Limited
  - Duration: 2010.05 ~ 2011.05
  - Position: NBU1 Department Operation and Maintenance (Intern)
  - Responsibilities: Responsible for operation and maintenance of NBU1 department's social websites and social games.
  - Summary: The starting point of everything. The9 provided a relatively complete system.
