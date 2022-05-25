# Ansible

## Installing Ansible

Kubespray supports multiple ansible versions and ships different `requirements.txt` files for them.
Depending on your available python version you may be limited in chooding which ansible version to use.

It is recommended to deploy the ansible version used by kubespray into a python virtual environment.

```ShellSession
VENVDIR=kube-vagrant-venv
KUBESPRAYDIR=kube-vagrant
ANSIBLE_VERSION=2.12
virtualenv  --python=$(which python3) $VENVDIR
source $VENVDIR/bin/activate
cd $KUESPRAYDIR
pip install -U -r requirements-$ANSIBLE_VERSION.txt
test -f requirements-$ANSIBLE_VERSION.yml && \
  ansible-galaxy role install -r requirements-$ANSIBLE_VERSION.yml && \
  ansible-galaxy collection -r requirements-$ANSIBLE_VERSION.yml
```

### Ansible Python Compatibility

Based on the table below and the available python version for your ansible host you should choose the appropriate ansible version to use with kubespray.

| Ansible Version | Python Version |
| --------------- | -------------- |
| 2.9             | 2.7,3.5-3.8    |
| 2.10            | 2.7,3.5-3.8    |
| 2.11            | 2.7,3.5-3.9    |
| 2.12            | 3.8-3.10       |

