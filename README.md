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

## Part 2: AWS
```hcl
resource "type" "name" {

}
# type -- tye of resource. eg; aws_vpc
# name -- the internal name to reference in terraform template
```

- The `provider block` configures the specified provider, in this case aws. A provider is a plugin that Terraform uses to create and manage your resources.
- The `profile` attribute in the aws provider block refers Terraform to the AWS credentials stored in your AWS configuration file, which you created when you configured the AWS CLI

```hcl
$ terraform fmt             # Terraform will print out the names of the files it modified, if any.

$ terraform show            # show current state of resource
```

- Create a `variables.tf` file to store variables in it. You can pass the file to `main.tf` or directly from CLI to pass values to it

```hcl
$ terraform apply -var "instance_name=Another web server"
```

- `Outputs`: Use outputs to give out infrastructure outputs after creation for easy query
- Create `outputs.tf` file and paster this
```hcl
```
```hcl
$ terraform output
```

## Part 3: Using Modules
- check directory: `learn-modules`

- Do not include `providers` in modules. Proceed and just create your resources. 

- Edit