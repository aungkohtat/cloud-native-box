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

git config user.name "aungkohtat"
git config user.email "aungkohtat717@gmail.com"
```

#### Up and Running vagrant box
```
git clone git@github.com:aungkohtat/cloud-native-box.git
cd cloud-native-box
mkdir .ssh
cd .ssh
ssh-keygen
/Users/aungkohtet/Desktop/cloud-native-box/.ssh/id_rsa
cd ../
vagrant up
```

#### Spin up k8s cluster
```
vagrant ssh
cd k8s-cop/1-single-cluster/setup/
./setup-kindcluster123.sh
```
