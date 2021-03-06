# OpenShift Origin All-in-One Vagrant box

This is a vagrant file which provisions an all-in-one OpenShift Origin installation. I mainly use this for development purposes.

NOTE: Tested only on Fedora 25

## Step 1: Install Pre-requisites
If you are on Fedora (like me):
```bash
$ dnf install @virtualization vagrant ansible
```

## Step 2: Create and provision the vagrant box
```
$ git clone https://github.com/deepaksrivastav/openshift-origin-allinone.git
$ cd openshift-origin-allinone
$ vagrant up
```

Grab a cup of coffe!

If the installation was successful, you should see something like this :

```
TASK [Installation Details] ****************************************************
ok: [default] => {
    "msg": "Login into openshift console at https://192.168.121.160:8443 with username/password as admin/admin"
}

PLAY RECAP *********************************************************************
default                    : ok=4    changed=2    unreachable=0    failed=0  
```

PS: Do not re-provision the appliance if installation fails. The playbooks are not idempotent (yet)
