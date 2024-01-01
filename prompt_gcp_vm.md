# Instructions for Creating a PostgreSQL Server VM and Firewall Rule

## Create a PostgreSQL Server VM (tested in Duet AI)

To create a Ubuntu VM named `postgress-server-vm`, use the following `gcloud` command:


```bash
# prompt : gcloud command to create a ubuntu vm named postgress-server-vm
gcloud compute instances create postgress-server-vm \
  --image-family=ubuntu-2004-lts \
  --image-project=ubuntu-os-cloud \
  --zone=us-central1-a

# prompt : gcloud command create a fire wall named postgress-server which allos port 5432
gcloud compute firewall-rules create postgress-server --allow tcp:5432

# Adding Tags to the VM
gcloud compute instances add-tags postgress-server-vm --tags=postgress-server

```

## Create a MySQL Server VM (tested in Duet AI)

```bash
gcloud compute instances create mysql-server-vm \
    --image-family=ubuntu-2204-lts \
    --image-project=ubuntu-os-cloud
    --zone=us-central1-a

# prompt : gcloud command create a fire wall named allow-mysql-access which allows port 3306
gcloud compute firewall-rules create allow-mysql-access --allow tcp:3306

# Adding Tags to the VM
gcloud compute instances add-tags mysql-server-vm --tags=allow-mysql-access
```
