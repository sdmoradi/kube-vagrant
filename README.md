# kube-vagrant
![Kubernetes Logo](https://raw.githubusercontent.com/kubernetes-sigs/kubespray/master/docs/img/kubernetes-logo.png)

deploy kubernets multi master ha cluster with Vagrant and virtualbox and using ceph as storage class (ceph rook) 

## Requirements

- ** Host with 24 core CPU and 48 Gi RAM and any OS
- ** Download and install Vagrant in host from <https://www.vagrantup.com/downloads>
- ** Download and install VituallBox from <https://www.virtualbox.org/wiki/Downloads>

## Quick Start

To deploy the cluster you can use :

### Vagrant

#### Usage

```ShellSession
# Install dependencies from ``requirements.txt``
sudo pip install -r requirements.txt
vagrant up
```

### Access to cluster nodes and manage

```ShellSession
vagrant ssh k8s-1
sudo cp /etc/kubernetes/admin.conf .
sudo chown vagrant:vagrant admin.conf
export $KUBECONFIG=admin.conf

kubectl get nodes -o wide
```
