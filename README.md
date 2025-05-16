# cloud-native-box

#### Create /etc/vbox/networks.conf
```
sudo su
cd /etc
mkdir vbox
cd vbox
vi networks.conf
* 0.0.0.0/0 ::/0
:wq!
```

#### My Cloud Native Box GitHub Account
```
eval "$(ssh-agent -s)"
ssh-add ~/.ssh/github.com.aungkohtat
ssh -T git@github.com

git config user.name "username"
git config user.email "user email"
```

#### Up and Running vagrant box
```
git clone git@github.com:aungkohtat/cloud-native-box.git
cd cloud-native-box
mkdir .ssh
cd .ssh
ssh-keygen   # (Need to replace: previous_pwd_result/id_rsa)
vi Vagrant   # (Need to replace: Path to your private key file location)
/Users/aungkohtet/Desktop/cloud-native-box/.ssh/id_rsa
cd ../
```

### Making Vagrant Box Up and Running

```
vagrant up
vagrant status     # Check vagrant box is up or not
```

#### Spin up k8s cluster
```
vagrant ssh
cd k8s-cop/1-single-cluster/setup/
./setup-kindcluster123.sh
```
#### Clean up

```bash
#!/usr/bin/env bash

kind delete clusters 123
kubectl config delete-context 123
kind delete clusters 124
kubectl config delete-context 124
kind delete clusters 125
kubectl config delete-context 125
kind delete clusters 127
kubectl config delete-context 127

```

**Or**

```bash
./terardown.sh
```
