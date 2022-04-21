# k8spractice
1. Create an nginx pod in a default namespace and verify the pod running
2. Create a namespace called 'podpractice' and an nginx pod  in this namespace using yaml
3. Create a busybox pod (using kubectl command) that runs the command "env". Run it and see the output
4. List all the pods in all namespaces
5. Create a pod with image nginx called nginx and expose traffic on port 80. Change pod's image to nginx:1.7.1. Execute a simple shell on the nginx pod
6. Create an nginx pod and set an env value as 'var1=val1'. (inline)
7. Create a Pod with two containers, both with image busybox and command "echo hello; sleep 3600". Connect to the second container and run 'ls'
8. Delete all the pods and namespaces created till now
9. Create a namespace called 'multipodpractice' 
10. Do below in multipodpractice namesapce
11. Create 3 pods with names nginx1,nginx2,nginx3. All of them should have the label app=v1. Show all labels of the pods. Change the labels of pod 'nginx2' to be app=v2. Get the label 'app' for the pods (show a column with APP labels)
12. Annotate pods nginx1, nginx2, nginx3 with "description='my description'" value. Check the annotations for pod nginx1
13. Clean all pods from this namespace.
14. Create a deployment with image nginx:1.18.0, called nginx, having 2 replicas, defining port 80 as the port that this container exposes. Check how the deployment rollout is going. Update the image to ngginx:1.2.0(deliberately wrong name). Verify something wrong with rollout. Check the rollout version. Return to previous version.
15. Scale the deployment to 5 replicas. Autoscale the deployment, pods between 5 and 10, targetting CPU utilization at 80%
16. Create a pod mp-hello with image alpine,nginx and consul:1.8. Use command sleep infinity for alpine container.
17. Create a Pod with three busy box containers with commands “ls; sleep 3600;”, “echo Hello World; sleep 3600;” and “echo this is the third container; sleep 3600” respectively and check the statusRun command ls in the third container busybox3 of the above pod
18. Create a Pod with main container busybox and which executes this “while true; do echo ‘Hi I am from Main container’ >> /var/log/index.html; sleep 5; done” and with sidecar container with nginx image which exposes on port 80. Verify both containers are running.
19. Create and display a configmap from a file
    
20. Create and display a configmap from a .env file
    
21. Create a configMap called 'options' with the value var5=val5. Create a new nginx pod that loads the value from variable 'var5' in an env variable called 'option'
    
22. Create a configMap 'anotherone' with values 'var6=val6', 'var7=val7'. Load this configMap as env variables into a new nginx pod
    
23. Create a configMap 'cmvolume' with values 'var8=val8', 'var9=val9'. Load this as a volume inside an nginx pod on path '/etc/lala'. Create the pod and 'ls' into the '/etc/lala' directory.
    
24. Create the YAML for an nginx pod that has the capabilities "NET_ADMIN", "SYS_TIME" added to its single container
    
25. Create a secret called mysecret with the values password=mypass
26. Create a secret called mysecret2 that gets key/value from a file
    
27. Create an nginx pod that mounts the secret mysecret2 in a volume on path /etc/foo
    
28. Create a configmap named config with values foo=lala,foo2=lolo. Display its values. 
