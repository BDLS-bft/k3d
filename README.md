# k3d
K3D Kubernetes Cluster

## Install K3D 
```bash
curl -s https://raw.githubusercontent.com/k3d-io/k3d/main/install.sh | bash
```

![image](https://github.com/BDLS-bft/k3d/assets/9446035/7a12be19-addf-49b2-ae2a-c34053d6c0e4)

```
k3d help
k3d --version
```
![image](https://github.com/BDLS-bft/k3d/assets/9446035/f3dcd111-93a0-40b5-8ab6-e70b3dab3601)

## Install kubectl

```
curl -LO "https://dl.k8s.io/release/$(curl -L -s https://dl.k8s.io/release/stable.txt)/bin/linux/amd64/kubectl"
chmod +x kubectl
sudo mv kubectl /usr/local/bin/
```

![image](https://github.com/BDLS-bft/k3d/assets/9446035/3ee98fd1-8d80-4986-adb9-85b12a7c075b)

* Note!
*  DO NOT cd /usr/local/bin/ then download the `kubectl` it will creat a symlink bot actual file.
*  Note: k3d v5.x.x requires at least Docker v20.10.5

![image](https://github.com/BDLS-bft/k3d/assets/9446035/72170acd-bdae-414c-99d8-bb259f79cfc3)

```
kubectl version --client
kubectl config view
```
![image](https://github.com/BDLS-bft/k3d/assets/9446035/e7007ccb-6719-4ee0-bdd1-128f611fb53c)

## Check current pods or Nodes
```
kubectl get pods
kubectl get nodes
# If you get error run this comment for more details
kubectl get nodes -v=10
```

## Create Cluster
```
k3d cluster create orgcluster
k3d cluster list
k3d node list
k3d cluster stop orgcluster
k3d cluster delete orgcluster
```



# Windows 

```
choco install k3d -y
choco install jq -y
choco install yq -y
choco install kubernetes-helm -y

```
![image](https://github.com/BDLS-bft/k3d/assets/9446035/d7c1db74-9254-4e7f-8956-b3033aba95c5)



