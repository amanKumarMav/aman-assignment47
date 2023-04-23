# You have deployed an application, that is listening at port 8000. You used a replica-set to deploy it and created a NodePort service to make it accessible. But when you test it, somehow the application is not reachable at the port. Write down your approach and sequentially all the steps that you will take to find out the issue.
  1. Check the status of application and replica set , wheather all are running and have no error.
  2. Correct the configuration (YAML) file where nodeport is properly configured. It should map with correct nodeport.  
