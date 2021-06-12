# Rancher Terraform

This terraform is to spin up a single node Rancher VM on Linode with docker. The rke directory contains a basic cluster.yml that needs to be edited and run with `rke up` to setup a K8 cluster using RKE.

## Requirements
- terraform 0.13 or newer

## Usage
1. Clone the repo and cd into it
2. Create the variables_override.tf
```bash
cp variables_override.tf.example variables_override.tf
```
3. Create the terraform.tfvars with your Linode token (you can skip this step, terraform will prompt for it if this file is not populated)
```bash
cp terraform.tfvars.example terraform.tfvars
vi terraform.tfvars
```
4. Configure the variables_override.tf
```bash
vi variables_override.tf
```
5. Terraform init, plan and apply like normal