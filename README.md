# GCP Full Project

## Description
A Python-based project with IaaC Automation (As Terraform/OpenTofu, Infrastracture Manager aka old Deployment Manager and Cloud Foundation Toolkit open source templates per Terraform)

## Reference links
- [Rapid cloud foundation buildout and workload deployment using Terraform](https://cloud.google.com/blog/products/devops-sre/using-the-cloud-foundation-toolkit-with-terraform/)

- [Projects and modules of Terraform for Google Cloud](https://cloud.google.com/docs/terraform/blueprints/terraform-blueprints?hl=it)




## Free products and their limitations
Source: https://cloud.google.com/free/docs/free-cloud-features

The list of free-tier usage limits that can be used:
https://cloud.google.com/free/docs/free-cloud-features#free-tier-usage-limits

| Product                            | Limitations                                                                                                      |
|------------------------------------|------------------------------------------------------------------------------------------------------------------|
| **App Engine**                     | 28 hours per day of F1 instances, 9 hours per day of B1 instances, 1 GB of outbound data transfer per day       |
| **Application Integration**        | Up to 400 integration executions, up to 20 GiB of data processed per month, first 2 connection nodes for Google services |
| **Artifact Registry**              | 0.5 GB storage per month                                                                                          |
| **AutoML Natural Language**        | 5000 prediction units per month                                                                                    |
| **AutoML Tables**                  | 6 node hours for training and prediction                                                                           |
| **AutoML Translation**             | 500,000 translated characters per month                                                                             |
| **BigQuery**                       | 1 TB of querying per month, 10 GB of storage                                                                      |
| **Cloud Build**                    | 2,500 build-minutes per month for e2-standard-2 machine type                                                       |
| **Cloud Deploy**                   | First active delivery pipeline (per billing account)                                                              |
| **Cloud Key Management Service**   | 100 free active key versions per month, 10,000 free cryptographic operations per month                           |
| **Cloud Logging and Cloud Monitoring** | Free monthly logging and metrics allotments                                                                        |
| **Cloud Natural Language API**     | 5,000 units per month                                                                                             |
| **Cloud Run**                       | 2 million requests per month, 360,000 GB-seconds of memory, 180,000 vCPU-seconds of compute time, 1 GB of outbound data transfer from North America per month |
| **Cloud Run functions**            | 2 million invocations per month (includes both background and HTTP invocations), 400,000 GB-seconds, 200,000 GHz-seconds of compute time, 5 GB of outbound data transfer per month |
| **Cloud Shell**                    | Free access to Cloud Shell, including 5 GB of persistent disk storage                                            |
| **Cloud Source Repositories**      | Up to 5 users, 50 GB of storage, 50 GB of outbound data transfer                                                  |
| **Cloud Storage**                  | 5 GB-months of regional storage (US regions only), 5,000 Class A operations, 50,000 Class B operations, 100 GB of outbound data transfer from North America to all region destinations (excluding China and Australia) per month |
| **Cloud Vision**                   | 1,000 units per month                                                                                             |
| **Compute Engine**                 | 1 non-preemptible e2-micro VM instance per month in one of the following US regions: Oregon, Iowa, South Carolina, 30 GB-months standard persistent disk, 1 GB of outbound data transfer from North America |
| **Firestore**                       | 1 GB of storage per project, 50,000 reads, 20,000 writes, 20,000 deletes per day, per project                     |
| **Google Kubernetes Engine**       | No cluster management fee for one Autopilot or Zonal cluster per Cloud Billing account, no fee for GKE Enterprise for the first 90 days |
| **Google Maps Platform**           | See the Pricing page for more details                                                                              |
| **Pub/Sub**                        | 10 GB of messages per month                                                                                       |
| **reCAPTCHA**                      | 10,000 assessments.create or siteverify calls per month for SKU ID F553-86ED-15F4, 1 million assessments.create or siteverify calls per month for SKU IDs A1ED-4B1C-A692 and 922B-4FA3-9210 |
| **Secret Manager**                 | 6 active secret versions per month, 10,000 access operations per month, 3 secret rotation notifications per month  |
| **Speech-to-Text**                 | 60 minutes per month                                                                                                |
| **Video Intelligence API**         | 1,000 units per month                                                                                             |
| **Web Risk**                       | 100,000 uris.search calls per month, 100 uris.submit calls per month                                              |
| **Workflows**                      | 5,000 internal steps per month, 2,000 external HTTP calls per month                                                 |

> --



# Scaffold

| Action | Steps |
|----|----|
| **Architecture** | A general overview of the architecture, GCP and Python, even a general idea about it
| **Google Cloud Pricing Calculator** | Calculate in advance how much will it cost
| **Create enviroment** | Terraform/OpenTofu folder structure and templates of all elements, in order to recreate all elements from scratch. Valorization trough value files is required for dinamic approach for recreation.
| **Dedicated pipeline** | A Github pipeline to validate the Terraform/OpenTofu files will be created. Also, validation of Python code will be added (see old Python DevOps projects). Create a task for each DevOps phase (build, test etc.)
| **Python application** | A python-based GUI where I can see the GCP services as tabs or clicking buttons. A future improvement will be to create a mini-game about all GCP services.
| **Project-phase** | A template where a project, quota, alarms and budgeting are created
| **Application-phase** | Python application developed and containerized, it will interact with DB products of GCP. To choose about a "gcloud" container or a Python SDK. The application will be replicated (Cloud Run or manually on VMs).
| **IAM-phase** | A dedicated Service Account will be used for each GCP service. Adeguate groups and roles will be assigned to users/service accounts. If not enough, custom roles will be created.
| **Database-phase** | Create databases where the Python app will interact. Use each database service accordingly at its usage purpose and costs.
| **LoadBalancer-phase** | Check what can be done in order to load balance the application. A Load Balancer or Cloud Run configuration, it depends on which architectural structure.
---


## Step 0 - Preparation
Tutorial link di Terraform for GCP: https://developer.hashicorp.com/terraform/tutorials/gcp-get-started

GCP Objects in Terraform: https://registry.terraform.io/providers/hashicorp/google/latest/docs

| Step | Procedure |
|----|---|
Install gcloud CLI | Link: https://cloud.google.com/sdk/docs/install or update the components with **gcloud components update** command, if the CLI is already installed.
Create GCP credentials file | A credential file can be created with **gcloud auth application-default login** command (more info [at this link](https://cloud.google.com/docs/authentication/application-default-credentials))
Log in with your GCP account | Launch the command: **gcloud init**
Install Terraform | Install from the official website
Install the auto-complete package | Launch the command: **terraform -install-autocomplete**
Go to "0 - Setup" folder | Enter in the "0 - Steup" folder
Init Terraform | Launch the command: **terraform init**
Format Terraform config | Launch the command: **terraform fmt**
Validate Terraform config | Launch the command: **terraform validate**
Plan Terraform config| Launch the command: **terraform plan**
Apply Terraform config| Launch the command: **terraform apply**
Show created elements | Launch the command **terraform status**
Destroy Terraform config? | Launch the command: **terraform destroy**

