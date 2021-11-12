# Terrraform-deep-dive
A deep dive on terraform and how to automate infrastructure on cloud platforms

## Part 1: Nginx webserver

## Set up
- File location: `./nginx-webserver`
```bash
$ terraform init            # Initialize
$ terraform plan            # What terraform will do in our infrasture before it does it
$ terraform validate
$ terraform apply           # Provision the resource(s)
$ terraform destroy         # To stop resources, eg docker container
```

## Introduction
```hcl
resource "type" "name" {

}
# type -- tye of resource. eg; aws_vpc
# name -- the internal name to reference in terraform template
```
