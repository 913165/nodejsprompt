## Instructions for Creating a PostgreSQL Server VM and Firewall Rule

### Create a PostgreSQL Server VM (tested in Duet AI)

```
# gcloud command to create a ubuntu vm named postgress-server-vm with tags allow-postgress-fw in uscentral 1 region
gcloud compute instances create postgress-server-vm \
  --image-family=ubuntu-2004-lts \
  --image-project=ubuntu-os-cloud \
  --zone=us-central1-a \
  --tags=allow-postgress-fw
# prompt : gcloud command create a fire wall named  allow-postgress-fw which allos port 5432
gcloud compute firewall-rules create postgress-server -- allow-postgress-fw

# Adding Tags to the VM
gcloud compute instances add-tags postgress-server-vm --tags=postgress-server
```
