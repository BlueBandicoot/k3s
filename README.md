# Kubernetes Cluster 

![Raspbernetes](docs/imdocs/img/raspbernetes.jpgg/raspbernetes.png)

## Nodes
+ OS: 
    **Ubuntu 20.04.5 aarch64** 
+ Domain: 
    **k8s.local**
+ HAProxy IP:
    **10.1.0.160**

| Hostname | IP eth0 | IP wlan0 | Rôle |
|---|---|---|---|
| **master1**  | 172.16.1.12 | 10.1.0.152 | Master node + KeepAlived + HAProxy |
| **master2**  | 172.16.1.13 | 10.1.0.153 | Master node + KeepAlived + HAProxy |
| **master3** | 172.16.1.14 | 10.1.0.154 | Master node + KeepAlived + HAProxy |
| **worker1** | 172.16.1.15 | 10.1.0.155 | Worker node |
| **worker2** | 172.16.1.16 | 10.1.0.156 | Worker node |
| **worker3** | 172.16.1.17 | 10.1.0.157 | Worker node |
| **worker4** | 172.16.1.18 | 10.1.0.158 | Worker node |
| **worker5** | 172.16.1.19 | 10.1.0.159 | Worker node |
| **dns** | 172.16.1.10 | 10.1.0.150 | PowerDNS, Vault, MinIO |
| **log/monitoring** | 172.16.1.11 | 10.1.0.151 | Grafana (Prometheus+Loki) or ELK |

## Physical position

| Cirrus |
|---|
| Master1 |
| Master2 |
| Worker4 |
| Worker5 |
| DNS |

| Nimbus |
|---|
| Master3 |
| Worker1 |
| Worker2 |
| Worker3 |
| OBS |


## Choices

+ Distribution: **k0s**
+ Bare-metal: **MetalLB**
+ GitOps: Mix of **Ansible** for host management and **ArgoCD** for cluster management
+ Networking: **Calico** + **Istio**
+ Ingress: **Istio**
+ Network Security: **Istio**
+ Storage: **rook-ceph**
+ Backups: **???**
+ Certificate management: **cert-manager**
+ Secret management: **sops** + **Sealed Secrets**? **Vault**?
+ Identity Provider: **keycloak**
+ Monitoring:
+ Log managment:
+ Misc: **external-dns** for automated dns

### Tools references/documentations

## Deployment



### Prerequisites

### Outside cluster monitoring & log management 

#### Monitoring

#### Log management

#### PowerDNS setup

[Here](docs/powerdns.md) for a detailed guide

### Cluster deployment

### Tools deployment ( GitOps methodology )