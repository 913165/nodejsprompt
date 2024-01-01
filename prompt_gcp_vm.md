# Instructions for Creating a PostgreSQL Server VM and Firewall Rule

## Create a PostgreSQL Server VM

To create a Ubuntu VM named `postgress-server-vm`, use the following `gcloud` command:

```bash
gcloud compute instances create postgress-server-vm \
  --image-family=ubuntu-2004-lts \
  --image-project=ubuntu-os-cloud \
  --zone=us-central1-a

# Create a Firewall Rule for PostgreSQL
gcloud compute firewall-rules create postgress-server --allow tcp:5432

# Adding Tags to the VM
gcloud compute instances add-tags postgress-server-vm --tags=postgress-server
