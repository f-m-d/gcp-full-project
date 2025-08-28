# GCP Full Project

## Description
A Python-based project with IaaC Automation (As Terraform/OpenTofu, Infrastracture Manager aka old Deployment Manager and Cloud Foundation Toolkit open source templates per Terraform)

## Reference links
- [Rapid cloud foundation buildout and workload deployment using Terraform](https://cloud.google.com/blog/products/devops-sre/using-the-cloud-foundation-toolkit-with-terraform/)

- [Progetti e moduli Terraform per Google Cloud](https://cloud.google.com/docs/terraform/blueprints/terraform-blueprints?hl=it)




## Free products and their limitations
Source: https://cloud.google.com/free/docs/free-cloud-features




## Scaffold

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

| Step | Procedure |
|----|---|
Install Terraform | Install from the official website
Init Terraform | 
