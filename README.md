# Requirements
- docker (requirement for minikube)
- k8s (minikube used.)
- kubectl
- helm

# Steps
- Create a volume SC1 (will save db data) and atach to the ec2. To mount:
```bash
sudo mkfs.ext4 /dev/nvme1n1
sudo mount /dev/nvme1n1 /k8s/
```
- minikube start