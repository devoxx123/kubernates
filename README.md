# kubernates & AWS Installation Process Steps

Basic Ngnix Deployement on Kubernates
-------------------------------------
apiVersion: apps/v1 # for versions before 1.9.0 use apps/v1beta2
kind: Deployment
metadata:
  name: nginx-deployment
spec:
  selector:
    matchLabels:
      app: nginx
  replicas: 2 # tells deployment to run 2 pods matching the template
  template:
    metadata:
      labels:
        app: nginx
    spec:
      containers:
      - name: nginx
        image: nginx:1.7.9
        ports:
        - containerPort: 80
        
        
 Reference Link---- https://kubernetes.io/docs/tasks/run-application/run-stateless-application-deployment/
 
 Youtube Link----- https://www.youtube.com/watch?v=Jn3PMClvUh0
