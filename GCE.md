**Setting Default Project**

    gcloud config set project [PROJECT_ID]

**Setting Default Compute Zone**

    gcloud config set compute/zone [COMPUTE_ZONE]

**List GCP insatnces**

    gcloud compute instances list

**Connect to GCP compute instance using ssh**

    gcloud compute ssh --project [PROJECT_ID] --zone [ZONE] [INSTANCE_NAME]

**Transfer file to GCP instance using SCP**

    scp -i ~/.ssh/my-ssh-key [LOCAL_FILE_PATH] [USERNAME]@[IP_ADDRESS]:~
    
    
**List the disks that are attached to a instance**

    sudo lsblk

**Elavate to Sudo user**

    sudo -i
    
    
**To copy a remote directory, ~/narnia, from example-instance to the ~/wardrobe directory of your local host, run:**

    $ gcloud compute scp --recurse example-instance:~/narnia ~/wardrobe
    
**Conversely, files from your local computer can be copied to a virtual machine:**    

    $ gcloud compute scp ~/localtest.txt ~/localtest2.txt example-instance:~/narnia
    

