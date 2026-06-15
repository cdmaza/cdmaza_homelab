# HomeLab

By leveraging GitOps and Infrastructure as Code (IaC), this project automates the entire lifecycle of my home lab services. It provides a flexible, scalable framework journey to my own self-hosted environment.

Goals: It's run and do what i want.

## First server:

### LENOVO 36C5

| Specs  | Details |
| ------------- |:-------------:|
| Baseboard      | SDK0K13455     |
| WIN      | 3273058843540     |
| CPU      | Intel(R) Core(TM) i5-7400 CPU @ 3.00GHz     |
| RAM      | 8GB     |
| Storage      | 1 TB     |

[Lenovo Help Center](https://pcsupport.lenovo.com/us/en/products/desktops-and-all-in-ones/500-series/510s-08ikl/90gb/solutions/ht504725-where-to-find-the-maximum-supported-ram-information)

### Limitations

1. CPU bottleneck (4 threads, no hyperthreading)
2. Low RAM -> Need upgrade to 32GB

    a. No ECC Memory - Not good for critical production
3. Old PC - Cost electrical more

**Good for homelab learning**

### Features
* Reverse proxy (NGINX)
* Internal DNS (Pi-hole)
* CI/CD (Jenkins / GitLab)
* Monitoring (Prometheus + Grafana)


### Tech stack

<table>
    <tr>
        <th>Logo</th>
        <th>Name</th>
        <th>Description</th>
    </tr>
    <tr>
        <td><img width="32" src="https://simpleicons.org/icons/ansible.svg"></td>
        <td><a href="https://www.ansible.com">Ansible</a></td>
        <td>Automate bare metal provisioning and configuration</td>
    </tr>
    <tr>
        <td><img width="32" src="https://avatars.githubusercontent.com/u/30269780"></td>
        <td><a href="https://argoproj.github.io/cd">ArgoCD</a></td>
        <td>GitOps tool built to deploy applications to Kubernetes</td>
    </tr>
    <tr>
        <td><img width="32" src="https://github.com/jetstack/cert-manager/raw/master/logo/logo.png"></td>
        <td><a href="https://cert-manager.io">cert-manager</a></td>
        <td>Cloud native certificate management</td>
    </tr>
    <tr>
        <td><img width="32" src="https://avatars.githubusercontent.com/u/21054566?s=200&v=4"></td>
        <td><a href="https://cilium.io">Cilium</a></td>
        <td>eBPF-based Networking, Observability and Security (CNI, LB, Network Policy, etc.)</td>
    </tr>
    <tr>
        <td><img width="32" src="https://avatars.githubusercontent.com/u/314135?s=200&v=4"></td>
        <td><a href="https://www.cloudflare.com">Cloudflare</a></td>
        <td>DNS and Tunnel</td>
    </tr>
    <tr>
        <td><img width="32" src="https://www.docker.com/wp-content/uploads/2022/03/Moby-logo.png"></td>
        <td><a href="https://www.docker.com">Docker</a></td>
        <td>Ephemeral PXE server</td>
    </tr>
    <tr>
        <td><img width="32" src="https://github.com/kubernetes-sigs/external-dns/raw/master/docs/img/external-dns.png"></td>
        <td><a href="https://github.com/kubernetes-sigs/external-dns">ExternalDNS</a></td>
        <td>Synchronizes exposed Kubernetes Services and Ingresses with DNS providers</td>
    </tr>
    <tr>
        <td><img width="32" src="https://upload.wikimedia.org/wikipedia/commons/thumb/3/3f/Fedora_logo.svg/267px-Fedora_logo.svg.png"></td>
        <td><a href="https://getfedora.org/en/server">Fedora Server</a></td>
        <td>Base OS for Kubernetes nodes</td>
    </tr>
    <tr>
        <td><img width="32" src="https://upload.wikimedia.org/wikipedia/commons/b/bb/Gitea_Logo.svg"></td>
        <td><a href="https://gitea.com">Gitea</a></td>
        <td>Self-hosted Git service</td>
    </tr>
    <tr>
        <td><img width="32" src="https://grafana.com/static/img/menu/grafana2.svg"></td>
        <td><a href="https://grafana.com">Grafana</a></td>
        <td>Observability platform</td>
    </tr>
    <tr>
        <td><img width="32" src="https://helm.sh/img/helm.svg"></td>
        <td><a href="https://helm.sh">Helm</a></td>
        <td>The package manager for Kubernetes</td>
    </tr>
    <tr>
        <td><img width="32" src="https://avatars.githubusercontent.com/u/49319725"></td>
        <td><a href="https://k3s.io">K3s</a></td>
        <td>Lightweight distribution of Kubernetes</td>
    </tr>
    <tr>
        <td><img width="32" src="https://kanidm.com/images/logo.svg"></td>
        <td><a href="https://kanidm.com">Kanidm</a></td>
        <td>Modern and simple identity management platform</td>
    </tr>
    <tr>
        <td><img width="32" src="https://avatars.githubusercontent.com/u/13629408"></td>
        <td><a href="https://kubernetes.io">Kubernetes</a></td>
        <td>Container-orchestration system, the backbone of this project</td>
    </tr>
    <tr>
        <td><img width="32" src="https://github.com/grafana/loki/blob/main/docs/sources/logo.png?raw=true"></td>
        <td><a href="https://grafana.com/oss/loki">Loki</a></td>
        <td>Log aggregation system</td>
    </tr>
    <tr>
        <td><img width="32" src="https://avatars.githubusercontent.com/u/1412239?s=200&v=4"></td>
        <td><a href="https://www.nginx.com">NGINX</a></td>
        <td>Kubernetes Ingress Controller</td>
    </tr>
    <tr>
        <td><img width="32" src="https://raw.githubusercontent.com/NixOS/nixos-artwork/refs/heads/master/logo/nix-snowflake-colours.svg"></td>
        <td><a href="https://nixos.org">Nix</a></td>
        <td>Convenient development shell</td>
    </tr>
    <tr>
        <td><img width="32" src="https://ntfy.sh/_next/static/media/logo.077f6a13.svg"></td>
        <td><a href="https://ntfy.sh">ntfy</a></td>
        <td>Notification service to send notifications to your phone or desktop</td>
    </tr>
    <tr>
        <td><img width="32" src="https://avatars.githubusercontent.com/u/3380462"></td>
        <td><a href="https://prometheus.io">Prometheus</a></td>
        <td>Systems monitoring and alerting toolkit</td>
    </tr>
    <tr>
        <td><img width="32" src="https://docs.renovatebot.com/assets/images/logo.png"></td>
        <td><a href="https://www.whitesourcesoftware.com/free-developer-tools/renovate">Renovate</a></td>
        <td>Automatically update dependencies</td>
    </tr>
    <tr>
        <td><img width="32" src="https://raw.githubusercontent.com/rook/artwork/master/logo/blue.svg"></td>
        <td><a href="https://rook.io">Rook Ceph</a></td>
        <td>Cloud-Native Storage for Kubernetes</td>
    </tr>
    <tr>
        <td><img width="32" src="https://avatars.githubusercontent.com/u/48932923?s=200&v=4"></td>
        <td><a href="https://tailscale.com">Tailscale</a></td>
        <td>VPN without port forwarding</td>
    </tr>
    <tr>
        <td><img width="32" src="https://avatars.githubusercontent.com/u/13991055?s=200&v=4"></td>
        <td><a href="https://www.wireguard.com">Wireguard</a></td>
        <td>Fast, modern, secure VPN tunnel</td>
    </tr>
    <tr>
        <td><img width="32" src="https://avatars.githubusercontent.com/u/84780935?s=200&v=4"></td>
        <td><a href="https://woodpecker-ci.org">Woodpecker CI</a></td>
        <td>Simple yet powerful CI/CD engine with great extensibility</td>
    </tr>
    <tr>
        <td><img width="32" src="https://zotregistry.dev/v2.0.2/assets/images/logo.svg"></td>
        <td><a href="https://zotregistry.dev">Zot Registry</a></td>
        <td>Private container registry</td>
    </tr>
</table>

## Resources
 - [Open source github](https://github.com/miantiao-me/awesome-homelab)