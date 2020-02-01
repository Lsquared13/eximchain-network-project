# Project: Eximchain Main Network

The infrastructure for running the backbone of the main Eximchain network and allowing users to connect

* Uses [Terraform](https://www.terraform.io/) configurations to launch a blockchain network globally in any combination of AWS regions with a single `terraform apply`
* Uses [Packer](http://packer.io/) to build AWS AMIs loaded with [quorum](https://github.com/jpmorganchase/quorum) derived blockchain software and scripts to run the necessary software and bootstrap the network
* Adapted to run [Eximchain Network Software](https://github.com/Eximchain/go-ethereum) and used in [Terraform Cloud](https://www.terraform.io/docs/cloud/index.html) to run the backbone of the main Eximchain network
* Uses additional software and [Terraform](https://www.terraform.io/) configurations for running individual nodes and transaction executors, which could serve individual requests from the public
* Includes associated DevOps procedures for maintaining and updating the network

## Repositories

### Main Network Backbone

* [Terraform Infrastructure](https://github.com/Lsquared13/terraform-aws-quorum-cluster)
* [Main Network Software](https://github.com/Lsquared13/go-ethereum)

### Individual Node

* [Terraform Infrastructure](https://github.com/Lsquared13/terraform-aws-eximchain-node)

### Transaction Executor

* [Terraform Infrastructure](https://github.com/Lsquared13/terraform-aws-eximchain-tx-executor)
* [Software](https://github.com/Lsquared13/eximchain-transaction-executor)

## DevOps Docs

* [Main Network Deployment](https://github.com/Lsquared13/eximchain-notes-public/blob/master/devops/deployment.md)
* [Main Network Health Check](https://github.com/Lsquared13/eximchain-notes-public/blob/master/devops/health-check.md)
* [Main Network Node Removal](https://github.com/Lsquared13/eximchain-notes-public/blob/master/devops/node-removal.md)
* [Dev Account Cleanup](https://github.com/Lsquared13/eximchain-notes-public/blob/master/devops/clean-dev.md)
