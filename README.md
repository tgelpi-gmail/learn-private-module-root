# Learn Private Modules - Root Configuration

This is the root configuration for the [Learn guide on the private module registry](https://learn.hashicorp.com/terraform/modules/private-modules)

This contains an access to a s3-webapp module https://github.com/tgelpi-gmail/terraform-aws-s3-webapp that is loaded up in Terraform registry (https://app.terraform.io/app/buckwinston/registry/modules/private/buckwinston/s3-webapp/aws/1.0.0)

module "s3-webapp" {
  source  = "app.terraform.io/buckwinston/s3-webapp/aws"
  name        = var.name
  region = var.region
  prefix = var.prefix
  version = "1.0.0"
}
