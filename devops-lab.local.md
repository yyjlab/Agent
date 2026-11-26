# DevOps 实验环境与学习方式

- 用户的实验集群是机房 Windows 宿主机上的 VMware 三节点。做本地实验时默认参考此环境，涉及公司生产和其他项目时先辨别目标。
- `master01` 为控制平面，`node01`、`node02` 为工作节点。内网地址依次为 `192.168.10.100`、`192.168.10.101`、`192.168.10.102`。前两台是 Rocky Linux 10.1，`node02` 是 Rocky Linux 10.2，均以 2026-11-25 的输出为准。
- VMnet8 使用 NAT，子网 `192.168.10.0/24`，网关 `192.168.10.2`，Windows VMnet8 地址 `192.168.10.1`。台式机办公网地址 `172.168.30.253`，笔记本用 RDP 管理台式机。已验证的 Xshell 入口为宿主机 TCP `2201` 转发到 `master01:22`。其他端口映射先核对。
- Kubernetes 最近报告为 `v1.35.6`，容器运行时为 `containerd 2.2.6`。当时三节点均 Ready，无 StorageClass、Metrics API 不可用，管理节点未安装 Helm。宿主机内存紧张，按小规模实验设计。变更前重新核对目标环境和资源。
- 用户按公司实际系统每天学习一个知识点，优先自己走完手动安装、配置、验证和排障。Prometheus/Grafana 学习顺序为手动二进制、Docker Compose、Kubernetes。已有学习手册时直接更新对应 Markdown。
- 详细环境和 Linux 实战见 `E:\notes\devops\linux-architect-series\README.md`。监控手册在 `E:\notes\devops\prometheus-grafana\Prometheus-Grafana 安装与实战.md`。
