**Create Cluster**

    gcloud container clusters create [CLUSTER_NAME]
    
**Get Credentials for Created Cluster**

    gcloud container clusters get-credentials [CLUSTER_NAME]
    
**Deploy an application on Cluster**

    kubectl create deployment [APP_NAME] --image=[IMAGE]
    
    E.g - kubectl create deployment hello-server --image=gcr.io/google-samples/hello-app:1.0
    
**Expose Deployment for accessing publically**

    kubectl expose deployment [DEPLOYMENT_NAME] --type LoadBalancer --port [EXPOSED_PORT] --target-port [CONTAINER_PORT]
    
    E.g - kubectl expose deployment hello-server --type LoadBalancer --port 80 --target-port 8080
    
    Passing in the --type LoadBalancer flag creates a Compute Engine load balancer for your container. 
    The --port flag initializes public port 80 to the Internet and --target-port routes the traffic 
    to port 8080 of the application.
    
