## Terraform Basics. Installing Terraform.

[/] Install Terraform binary

[/] Install Docker Desktop for Windows

[/] Initialize a Terraform + Docker project

[/] Provision NGINX server container using Docker

[/] Verify existence of NGINX container ( achieve "Welcome to NGINX" message)

[/] Destroy Docker NGINX container

## Questions, comments, concerns, etc:

### Infrastructure as Code with Terraform - What is Terraform doing?

Terraform can be used to build, change, and version infrastructure. This allows the ability to manage existing service providers like AWS or GCP or custom solutions. Terraform works by using configuration files to define parts required to run an application or datacenter. Terraform creates a plan to describe what needs to happen to reach a desired state, then performs the build as described in the plan.

Main features of Terraform:

#### Infrastructure as Code
- Infrastructure as code is a high-level configuration syntax that works as a versioned map of the datacenter and can be shared and re-used. You treat the versioned maps as any other code.

#### Execution Plans
- This is the planning step. The plan created shows what Terraform will do when you run an apply. You can see everything that is about to happen.

#### Resource Graph
- A graph showing all creation and modifications of non-dependent resources.

#### Change Automation
 - Using execution plan and resource graph, the map of what Terraform will change in what order helps avoid any possible human errors.

In this test, I asked Terraform to use docker locally to start up a container with NGINX.

terraform init - Terraform downloads execute map and readies to talk to Docker

terraform apply - Terraform will talk to Docker and perform actions as described in execute map.

terraform destroy - Terraform will destroy the instance that was created


### Advantages of Terraform - What kinds of problems does Terraform solve?

Terraform can help manage different environments which similar configurations.
