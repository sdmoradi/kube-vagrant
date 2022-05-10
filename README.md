# kube-vagrant
![Kubernetes Logo](https://raw.githubusercontent.com/kubernetes-sigs/kubespray/master/docs/img/kubernetes-logo.png)

deploy kubernets multi master ha cluster with Vagrant and virtualbox and using ceph as storage class (ceph rook) 

## Quick Start

To deploy the cluster you can use :

### Ansible

#### Usage

```ShellSession
# Install dependencies from ``requirements.txt``
sudo pip3 install -r requirements.txt
```
### Vagrant

For Vagrant we need to install python dependencies for provisioning tasks.
Check if Python and pip are installed:

```ShellSession
python -V && pip -V
```

If this returns the version of the software, you're good to go. If not, download and install Python from here <https://www.python.org/downloads/source/>
Install the necessary requirements

```ShellSession
sudo pip install -r requirements.txt
vagrant up
```
