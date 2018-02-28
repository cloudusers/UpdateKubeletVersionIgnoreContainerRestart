# UpdateKubeletVersionIgnoreContainerRestart

TYPE: patch. 
TARGET: when update kubelet version, ignore restart containers


STEPS:
1, download source of kubernets such as kubernets-1.9.1.tar.gz (https://github.com/kubernetes/kubernetes/releases)
2, unzip && cd kubernets-1.9.1
3, patch -p1 < ../kubernetes-1.9.1.IgnoreContainerRestart.patch
4, make -j8

in  kubernetes-1.9.1/_output/bin, new kubelet will be produced
