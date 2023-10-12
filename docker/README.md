# Terraform: Docker and nginx locally

To run this locally use the following commands:

Start docker:
open -a Docker

Run nginx with terraform (main.tf):
terraform init
terraform apply
Navigate to <localhost:8000> or type docker ps

Tear down the container:
terraform destroy
