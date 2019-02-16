# kubernetes-nginx-hostPath
kubernets nginx, pv, pvc, pod and service

Step 1: Run 'nginx-pv.yml' file.

-kubectl create -f nginx-pv.yml 

This file creates PersistentVolume, with storage capacity of 2Gi.


Step 2: Run 'nginx-pvc.yml' file. 

-kubectl create -f nginx-pvc.yml 

This file creates PersistentVolumeClaim, with storage of 1Gi.


Step 3: Run 'nginx-pod.yml' file. 

-kubectl create -f nginx-pod.yml 

This file creates Nginx Pod. Attaches volume to it. 

NOTE: I have 2 workers running, and both of the workers have the folder "/home/ubuntu/data/app-data", which contains a custom 'index.html' file. You need to change this to your settings on your worker nodes. 


Step 4: Run 'nginx-service.yml' file. 

-kubectl create -f nginx-service.yml 

This file creates a service NodePort, which publishes port 30080 of your node to access your Nginx pod on port 80.


