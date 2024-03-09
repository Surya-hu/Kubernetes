### Create the K8s EKS,further you have to do the deployment of Nginx application

Pre-requisites:  
1. Installed eksctl  
2. Installed kubectl
3. Created IAM user with adminfullaccess  
4. Installed aws-cli and configured with IAM accesskey

Below images shows all the versions of above said tools  

![image](https://github.com/Surya-hu/Kubernetes/assets/119995742/f13b2f4d-cc88-4ea3-861d-dc9a3e1d79e0)

Cluster has been created using below command  

`eksctl create cluster --name my-test-cluster --region ap-southeast-1 --node-type t2.micro --nodes-min 2 --nodes-max 2 --zones ap-southeast-1a,ap-southeast-1b`


![image](https://github.com/Surya-hu/Kubernetes/assets/119995742/e7d7dd81-e36e-497b-a539-2c0dbd9c2b10)


Master and worker nodes created successfully  

![image](https://github.com/Surya-hu/Kubernetes/assets/119995742/316af5f4-ecc8-40dc-90d1-0bb97c2b4367)


Created a deployment file called `nginx-deployment.yaml` with below contents  

![image](https://github.com/Surya-hu/Kubernetes/assets/119995742/77114c05-81cb-40d9-ab20-3d60b6417ec5)

Applied the deployment using `kubectl apply -f nginx-deployment.yaml`  

Exposed the deployment using `kubectl expose deployment nginx-deployment --port=80 --target-port=80 --type=LoadBalancer`  

Verified if the service has been deployed properly  

![image](https://github.com/Surya-hu/Kubernetes/assets/119995742/8a45e839-6a5a-4c98-8c81-1b8d192f3b43)


Using the External IP verified and found that nginx application deployed successfully and working as shown below  

![image](https://github.com/Surya-hu/Kubernetes/assets/119995742/574daad6-6b97-4a3f-9cbd-ccacbd21cc11)





