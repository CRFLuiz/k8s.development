# Environment
**EC2 t4g.medium**
- 2 vCPU | 4 GiB RAM
- debian 10
- arm

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
- kubectl apply -f k8s/development.db.yaml
- kubectl apply -f k8s/development.db.redis.yaml
