### Setup minikube at your local and explore creating namespaces

Pre-requisites:  
Installed eksctl, kubectl, awscli and IAM user with administratoraccess  using the official docs page.

Using below command created cluster and nodes:  
`eksctl create cluster --name my-test-cluster --region ap-southeast-1 --node-type t2.micro --nodes-min 2 --nodes-max 3 --zones ap-southeast-1a,ap-southeast-1b`

Clusted created and Pods created successfully as shown below:  
![image](https://github.com/Surya-hu/Kubernetes/assets/119995742/72d227b2-5704-4109-84b1-73cc1dc38616)



![image](https://github.com/Surya-hu/Kubernetes/assets/119995742/559c08b8-a5b4-4136-bcde-103f6638bd36)


Master and worker nodes has been created successfully:  


![image](https://github.com/Surya-hu/Kubernetes/assets/119995742/4f93258a-e991-48eb-a64f-cca3ed4b6ebf)



Created the namespace and listed the nginx running in the namespace:  

![image](https://github.com/Surya-hu/Kubernetes/assets/119995742/b1fe0042-98ad-48ae-9254-1664867d0443)
