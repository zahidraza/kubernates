**List GCP insatnces**

`gcloud compute instances list`

**Connect to GCP compute instance using ssh**

`gcloud compute ssh --project [PROJECT_ID] --zone [ZONE] [INSTANCE_NAME]`

**Transfer file to GCP instance using SCP**

`scp -i ~/.ssh/my-ssh-key [LOCAL_FILE_PATH] [USERNAME]@[IP_ADDRESS]:~`
