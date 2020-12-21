# Kubernetes CKA Example Environments

## 下载 vagrant 镜像

```bash
vagrant box add https://mirrors.tuna.tsinghua.edu.cn/ubuntu-cloud-images/bionic/current/bionic-server-cloudimg-amd64-vagrant.box --name ubuntu/bionic64
```

## 适配中国国情

已添加阿里源，同时 `k8s` 使用阿里云的国内镜像

## k8s 版本
已更新至 `v1.20.1`


## setup and run
You will start a two node cluster on your machine, one master and one worker. For this you need to install VirtualBox and vagrant, then:


```
git clone git@github.com:liyongjian5179/cka-example-environments.git
cd cka-example-environments/cluster1
./up.sh

vagrant ssh cluster1-master1
vagrant@cluster1-master1:~$ sudo -i
root@cluster1-master1:~# kubectl get node
```

You should be connected as `root@cluster1-master1`. You can connect to other worker nodes using root, like ssh `root@cluster1-worker1`
If you want to destroy the environment again run `./down.sh`. You should destroy the environment after usage so no more resources are used!


