# Harrison Zhu's Resume

**Specialties:** DevOps, Golang, Kubernetes, Containers, Automation, Machine Learning Platforms

---

## About Me

- **Name**: Harrison Zhu
- **Experience**: 14.5 years
- **GitHub**: [Hz89](https://github.com/Hz89)
- **Position Sought**: Infrastructure Developer / DevOps Engineer / SRE
- **Preferred Location**: Singapore
- **Contact**:
  - **Email**: wcg6121@gmail.com
- **Current Role**: Employed
- **Education**: Associate Degree

---

## Skills

- **Programming Languages**: Golang, Python
- **Version Control**: Git (GitLab, GitHub, Gitea)
- **CI/CD**: [Drone](https://github.com/drone/drone), Jenkins
- **Databases**: MySQL, TiDB, TiKV, Codis, Redis
- **Infrastructure as Code (IaC)**: [Terraform](https://github.com/hashicorp/terraform), [RKE](https://github.com/rancher/rke)
- **Infrastructure**: Kubernetes, OVS/OVN, Flannel, Calico, RoCE, IB, IPoIB
- **Container Technologies**: RKT, Docker
- **Operating Systems**: CentOS 6/7, CoreOS, Ubuntu 16.04
- **Cloud Platforms**: AWS, Alibaba Cloud (Extensive use of Golang SDK)
- **Methodologies**: DevOps, Agile

---

## Project Experience

### Tencent Cloud

- **Tencent Cloud EKS**:
  - Led architecture and core development for EKS versions 1.0, 1.5, and 2.0.
  - Established CI/CD pipelines and development standards.
  - Developed and managed Windows container support.

- **EKS OS Development**:
  - Created a customized Linux distribution tailored for EKS, optimizing startup speed.

- **CSI on Nodeless Kubernetes**:
  - Implemented a unique CSI compatible with nodeless Kubernetes for EKS.

---

### Momenta (AI Autonomous Driving)

- **MOPS K8s Multi-Cluster Management Platform**:
  - Enhanced and customized the open-source [Wayne](https://github.com/Qihoo360/wayne) project for multi-cluster management.
  - Integrated Alibaba Cloud for DNS automation.

- **Jenkins CI Platform**:
  - Deployed Jenkins with Kubernetes for build clusters.
  - Implemented caching for Jenkins agents with shared storage.

- **Goslurm Deep Learning Scheduling Platform**:
  - Developed K8s-based scheduler compatible with Slurm for deep learning tasks.
  - Integrated with frameworks like TensorFlow, PyTorch, and Caffe2.
  - Hybrid cloud deployment with multi-cluster and auto-scaling on AWS.

- **Hive Training Dataset Management System**:
  - Created a version-controlled dataset management system compatible with AWS S3 and Alibaba Cloud OSS.
  - Provided a Git-like interface for managing dataset versions.

- **CacheFS Distributed File System**:
  - Designed a distributed, multi-layer caching system for deep learning tasks.
  - Supported various storage backends (AWS S3, Alibaba Cloud OSS, CEPH) and implemented Kubernetes CSI integration.

---

### Youzu Interactive

- **UPaaS Private PaaS Platform**:
  - Architected a private PaaS including CI/CD, image repository, and elastic computing with Kubernetes.
  - Integrated [Gogs](https://github.com/gogs/gogs) for git services, `Drone` for builds, and `Harbor` for a private Docker registry.

- **Djob Centralized Cron Job Management**:
  - Built a high-availability cron job management and command scheduling system using Golang, SWIM, gRPC, etcd, and TiDB.

- **CMDB**:
  - Designed and began developing a CMDB system for managing configuration and asset information across infrastructure.

---

### 17173 Beijing Branch

- **Monitoring System**:
  - Implemented a `Zabbix`-based monitoring system with customized alerts and data storage.
  - Used MySQL-TokuDB and Python scripts to improve data handling for high-volume monitoring.

---

## Work Experience

- **TikTok (Singapore)**
  - **Position**: SRE
  - **Duration**: Dec 2022 – Present
  - **Role**: As part of the SRE team at TikTok, I focus on identifying and resolving critical stability and performance issues. My role includes monitoring, diagnosing, and troubleshooting various bottlenecks to ensure optimal system performance and reliability.
  - **Key Achievements**:
    - Identified and resolved IO bottlenecks in the production environment, enhancing overall system responsiveness.
    - Optimized connection pool management in the Go MySQL driver, leading to improved database access performance.
    - Addressed and resolved long-connection issues within the service mesh, improving network reliability and stability.
    - Enhanced the network IO performance of TikTok's internal framework, Kitex, by optimizing configurations and identifying architectural improvements.

- **Tencent Cloud**
  - **Position**: Senior Backend Developer
  - **Duration**: Aug 2019 – Dec 2022
  - **Role**: Led architecture and core development for Tencent’s EKS platform, focusing on building scalable, nodeless Kubernetes services from the ground up.
  - **Key Achievements**:
    - Developed and scaled Tencent Cloud’s nodeless Kubernetes to support over 2 million cores, serving 1,000+ enterprise customers.
    - Built a custom Linux OS for EKS, reducing startup time and optimizing system resources for container workloads.
    - Designed and implemented a CSI-compatible storage solution to ensure seamless storage management in a nodeless Kubernetes environment.

- **Momenta (AI Autonomous Driving)**
  - **Position**: Development Engineer
  - **Duration**: Feb 2018 – Aug 2019
  - **Role**: Supported deep learning platform development, focusing on DevOps, CI/CD, and infrastructure scalability.
  - **Key Achievements**:
    - Customized the Wayne open-source project for multi-cluster Kubernetes management and integrated it with Alibaba Cloud for automated DNS management.
    - Deployed a Kubernetes-based Jenkins CI environment, reducing build times by implementing caching solutions for shared storage.
    - Developed a distributed file system, CacheFS, for deep learning, supporting AWS S3, Alibaba OSS, and CEPH, and integrated with Kubernetes CSI to streamline dataset access.

- **Youzu Interactive**
  - **Position**: Senior DevOps Engineer / DevOps Development Supervisor
  - **Duration**: Mar 2015 – Jan 2018
  - **Role**: Spearheaded Youzu’s private PaaS platform, integrating CI/CD, container management, and infrastructure automation.
  - **Key Achievements**:
    - Architected and launched UPaaS, a private PaaS platform combining Gogs, Drone, and Harbor for code, build, and image management.
    - Created Djob, a centralized cron job management system, achieving high availability and flexibility for task scheduling across Youzu’s infrastructure.
    - Initiated the development of a CMDB system to manage configuration and asset information, enhancing operational insights and control.

- **17173 Beijing Branch**
  - **Position**: DevOps Development Engineer
  - **Duration**: Sep 2013 – Mar 2015
  - **Role**: Supported development and operations for a high-performance monitoring solution tailored for large-scale gaming applications.
  - **Key Achievements**:
    - Developed a Zabbix-based monitoring system with customized alerts and data handling improvements, specifically for gaming applications.
    - Implemented a MySQL-TokuDB backend to manage and store high-volume monitoring data efficiently.

- **Shanghai Jiangyou**
  - **Position**: Operations and Maintenance
  - **Duration**: May 2011 – Feb 2013
  - **Role**: Provided IT operations support and maintenance, focusing on server uptime, performance, and reliability.
  - **Key Achievements**:
    - Maintained and supported various applications and infrastructure, ensuring high availability and performance.
    - Implemented regular server and network audits to optimize uptime and resource management.

- **The9 Limited**
  - **Position**: Operations and Maintenance Intern
  - **Duration**: May 2010 – May 2011
  - **Role**: Assisted with maintenance and operation of The9’s gaming and social websites, ensuring minimal downtime and optimal user experience.
  - **Key Achievements**:
    - Supported daily operations for NBU1 department’s social websites and gaming platforms.
    - Conducted regular backups, audits, and troubleshooting to prevent and resolve technical issues.

---

## Summary

I previously built a nodeless Kubernetes service from scratch at Tencent Cloud, scaling it to support over 2 million cores and serving more than 1,000 enterprise customers. Currently, I am responsible for ensuring the stability of TikTok Shop, a platform composed of over 3,000 microservices.

I am seeking a position with competitive compensation that aligns with my experience and expertise. As an Employment Pass (EP) holder, I would also require visa sponsorship from any future employer.