# Suppose you have deployed your application using a deployment controller. Assume the initial number of replicas is one. Write the steps needed to update a container's image using deployment, making sure that there is zero downtime.
    - Steps to update the image, with zero runtume. 
       1. Set the strategy type rolling-update (if it is not set) in deployment controller.
       2. Add patch deployment using command - **kubectl patch deployment <deployment_name> -p '{"spec": {"minReadySeconds": 10}}'** - this will not allow the pod to get down till 10 sec. 
       3. Then update the image using the commands - **kubectl set image deployment <deployment_name> <container_name>=<container_image_name_V2>**
             ex:  <container_image_name_V2> - luksa/kubia:v2
       4. this commands will show us the transition from v1 to v2
            **kubectl get po**
            **kubectl get rs**
