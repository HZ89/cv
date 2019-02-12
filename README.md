# 朱慧鹏的简历

- Topic: Devops Golang kubernetes 容器 运维开发 自动化 深度学习训练平台

## 关于我

- 朱慧鹏
- 1989-06 ～ Now
- 大专/商丘师范学院(2008.09~2011.07)
- 工作年限: 8年
- Github: [HZ89](https://github.com/HZ89)
- 期望职位: golang dev/Devops Engineer/SRE
- 期望城市: 上海 北京
- Wechat: 371852029
- Email: wcg6121@gmail.com
- 目前状态: 在职

## 技能清单

所列出的均为熟练使用的技能

- 开发语言: Golang,Python
- 版本管理: Git（gitlab、github、gitea）
- CI/CD: [Gitea](https://github.com/go-gitea/gitea)+[Drone](https://github.com/drone/drone),[Gitlab-ci](https://about.gitlab.com/features/gitlab-ci-cd/),Jenkins
- 数据库: MySQL
- 方法论: Devops
- IaC: [Terraform](https://github.com/hashicorp/terraform) [RKE](https://github.com/rancher/rke)
- Automation: Ansible
- Infar: Kubernetes, OVS/OVN, Fannel, Calico, RoCE, IB, IPoIB
- Container Tech: RKT, Docker
- Ops: LNMP, Linux Kernel Parameter, MySQL, CEPH
- OS: Centos 6/7, CoreOS, Ubuntu 16.04
- cloud platform: aws alicloud 使用各平台的golang sdk开发。熟悉各平台的网络特征，用户管理体系，混合云设计

## 项目经历

有完整实施的项目，时间倒序排列

### Momenta

#### MOPS k8s 多集群管理平台

- 基于360开源的[wayne](https://github.com/Qihoo360/wayne)项目定制开发
  - ingress相关功能
  - 对接阿里云实现域名自动解析
  - 现有集群导入功能

#### Jenkins CI平台

- jenkins+kubernetes 提供jenkins构建集群
- 使用共享存储解决jenkins agent编译缓存

#### goslurm 深度学习调度平台

- CLI兼容[slurm](https://www.schedmd.com/) 降低传统HPC生态用户迁移成本
- 基于k8s调度任务,使用自定义scheduler
- 兼容 `caffe2` `tensorflow` `pytorch` 常见框架 使用对应k8s的operator
- 云上环境与云下环境混合部署
- 云上环境自动扩缩容
- 集群自动部署（terraform+rke）
- 支持多集群
- 支持以太网以及RDMA网络

#### RKE 功能扩展

- [RKE](https://github.com/rancher/rke)对接[Vault](https://www.vaultproject.io/)实现k8s集群证书的统一管理

### 上海游族

#### UPaaS 私有PaaS平台

类似于简化版的网易蜂巢，包含代码托管构建，镜像市场，弹性计算，云盘 等功能

- 负责系统后端架构设计，技术选型。后端系统开发
- 子系统：
    - CI/CD 系统: 使用 `gogs` git服务 和 `drone` 自动构建系统 进行代码过托管和自动构建
    - 私有docker registry: 使用 `Vmware Harbor` 高可用集群建设私有镜像托管系统
    - CEPH 块存储以及对象存储系统: 为PaaS平台提供块存储实现云盘功能，对git系统提供共享存储，为registry 提供对象存储
    - Kubernetes: 提供弹性计算和服务调度功能。
    - `archon`实现kubernetes集群的管理。使用一个共享的管理集群来管理每个租户的业务集群。

#### Djob 集中式Cron任务管理&&命令调度系统

- 负责系统设计，需求梳理，架构设计，技术选型，后端开发
- 设计功能: 集中的管理cron任务并且支持一次性任务的分发，支持跨机房管理，支持任务依赖，任务精度精确到秒,支持一次性任务执行的并发控制
- 技术栈: Golang, SWIM协议, TIDB, GRPC, etcd
- 实现:
    - 利用SWIM协议将所有的服务器组成一个大集群，集群状态由SWIM协议维护，实时小消息由SWIM协议分发
    - 人为将服务器逻辑上定义为`server`和`agent`端.
    - `server`负责任务的调度，分发，执行结果回收，消息转发并且执行SWIM协议也可以执行任务. 
    - `agent`仅仅运行 SWIM 协议以及执行具体任务。
    - GRPC协议负责大包（大于1k）或非实时消息传输：`agent`获取具体任务信息，任务执行结果回传等
    - etcd 用于同步`server`端状态。由于SWIM为弱一致消息所以需要etcd来同步每个任务的执行状态和锁信息

#### CMDB

- 负责系统设计，需求整理，把控进度
- 计划设计开发一个CMDB系统来管理中间件，操作系统，硬件，网络设备，IDC 所有运维相关实体的配置信息，但是由于经验不足，而且没有具体需求导致项目陷入描述每个具体配置对象的配置模式，而忽略了CMDB的本质最终导致无法推进

### 17173北京分公司

#### 监控系统

- 负责基于`zabbix`设计一个监控系统监控173所有服务器以及中间件，数据库的状态，以及报警
- 基于`zabbix`定制了报警行为，报警模式。以`python`开发了一套`zabbix`的报警脚本库。使用`MySQL-TokuDB` 作为存储。由于当时zabbix当时不能处理大量数据，对监控系统依据业务进行拆分，然后封装一个统一接口对外提供服务

## 工作经历(2010.05~now)

- Momenta（AI无人驾驶）
    - 时间: 2018-2-22~now
    - 职位: 开发工程师
    - 职责: 负责devops流程的保障与技术支持以及深度学习训练平台开发
- 上海游族
    - 时间: 2015.03~2018.01
    - 职位: 运维开发主管/资深运维工程师 （二次入职导致职位变化）
    - 职责: 带领运维开发团队开发游族内部自动化运维系统/负责运维技术选型架构，新技术推广
    - 离职原因: 想要回北京
    - 总结: 从运维到运维开发到devops转型的一段经历。做出了自己想做的系统并且接触实践了最新的技术。关键是认识了一群很棒的人。
- 17173北京分公司
    - 时间: 2013.09~2015.03
    - 职位: 运维开发工程师
    - 职责: 负责运维系统开发以及一些运维工作
    - 离职原因: 畅游公司内部动荡
    - 总结: 经历过最棒的团队。也是从运维转向运维开发的起点。
- 上海江游
    - 时间: 2011.05~2013.02
    - 职位: 运维
    - 职责: 所有运维相关的事情
    - 离职原因: 年轻想四处看看
    - 总结: 从零开始的小公司，接触到运维的方方面面（IDC网络建设，IDC选择，服务器硬件等全部运维相关的软硬件工作），开拓眼界。
- 第九城市
    - 时间: 2010.05~2011.05
    - 职位: NBU1部运维
    - 职责: 负责NBU1部的社交网站以及社交游戏运维
    - 离职原因: 九城大裁员
    - 总结: 一切的起点。九城给了我一个相对完整的体系。为我第二份工作提供了一个参考架构和各种解决方案。