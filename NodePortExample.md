**Service Yaml for Node Port**

```
apiVersion: v1
kind: Service
metadata:
  name: nginx
spec:
  type: NodePort
  ports:
    - port: 80
      nodePort: 30080
      name: http
    - port: 443
      nodePort: 30443
      name: https
  selector:
    name: nginx
 ```
 
 The drawback of using NodePort is that you've to take care of integrating with your providers firewall by yourself. 
 
 For GCE opening up the above for publicly on all nodes could look like
 
    gcloud compute firewall-rules create myservice --allow tcp:30080,tcp:30443
    
Once this is in place your services should be accessable through any of the public IPs of your nodes. You'll find them with:

    gcloud compute instances list
    
Reference: https://stackoverflow.com/questions/42040238/how-to-expose-nodeport-to-internet-on-gce    
