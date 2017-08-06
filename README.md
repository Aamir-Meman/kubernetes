# kubernetes
This is a .yaml file to run pods

# file: pod.yml 

 -$ kubectl create -f pod.yml
 
 -$ kubectl get pods
 
 -$ kubectl describe pods
 
 -$ kubectl get pods
 
 -$ kubectl get pods/hello-pod
 
 -$ kubectl pods --all-namespaces
 
 -$ kubectl delete pods hello-pod

# file: rc.yml

   -$ kubectl create -f rc.yml
   
   -$ kubectl get rc
   
   -$ kubectl describe rc
   
   -$ kubectl apply -f rc.yml ( changing to 20 replicas)
   
   -$ kubectl get rc -o wide
   
   -$ kubectl get pods
   
# Creating the service the Iterative way

   -$ kubectl expose rc hello-rc --name=hello-svc --target-port:8080 --type=NodePort
   
   -$ kubectl describe svc hello-svc (expose your each amazon-instance-ip-address:NodePort)

# Getting the svc and deleting the service
   
   -$ kubectl get svc
   
   -$ kubectl delete svc hello-svc
   
# Creating the service the Declarative Way
   
   -file : svc.yml
   
   -$ kubectl create -f svc.yml
   
   -$ kubectl get svc
   
   -$ kubectl describe svc hello-svc
   
   -$ kubectl describe ep hello-svc { This describe the endpoints of pods i.e. IP address}
